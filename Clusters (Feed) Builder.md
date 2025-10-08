
# 1) Коротко

Мы пересобираем кластеры **только когда это нужно**: если накопилась **новизна** (инсайты, ещё ни разу не участвовавшие в кластеризации пользователя), если прошло слишком много **времени** с последней сборки, и только для **активных** пользователей. Новизна считается дёшево по формуле `Σ(current_seq − HWM)`. Планировщик раз в 30–60с отбирает кандидатов, воркеры пересчитывают кластеры «целиком на окне» (например, 30–60 дней embeddings), поднимают `cluster_version`, сдвигают HWM и инвалидируют кэш фида по версии.

---

# 2) Контекст и компоненты

- **API-Gateway → Aggregator gRPC** — синхронные ручки для клиента.
    
- **Feed Builder** — фоновая подсистема: Планировщик + Воркеры.
    
- **Clusterizer** — сервис кластеризации по embeddings (не инкрементальный).
    
- **Insights DB (PG)** — все инсайты: `(channel_id, seq, ts, embedding, …)`.
    
- **Clusters DB** — кластеры пользователя по `cluster_version`.
    
- **MongoDB** — кэш сгенерированного фида (ключ — `cluster_version`).
    
- **Redis** — быстрые счётчики/кандидаты/локи (ускоритель, не «истина»).
    

---

# 3) Триггеры запуска 

1. **Новизна:** `pending_insights_count(u) ≥ N(plan)`
    
2. **Время:** `now − last_clustered_at(u) ≥ T(plan)`
    
3. **Активность:** `now − last_active_at(u) ≤ A(plan)`
    

- **Cooldown:** не ставим пользователя в очередь чаще, чем `cooldown(plan)`.
    

`pending_insights_count(u)` = **сколько инсайтов у пользователя ещё ни разу не участвовали в кластеризации**.

---

# 4) Как считаем новизну

По каждому каналу `c`:

- `current_seq[c]` — сколько всего инсайтов пришло
    
- `HWM[u,c]` — до какого `seq` уже кластеризовали для пользователя `u` в канале `c`
    

Тогда:

```
pending_in_channel(u,c) = current_seq[c] − HWM[u,c]
pending_insights_count(u) = Σ_{c∈subscriptions(u)} pending_in_channel(u,c)
```

> При появлении нового инсайта мы **только** увеличиваем `current_seq[c]`

---

# 5) Модели данных и БД

## PostgreSQL

- `channels(channel_id PK, current_seq BIGINT, last_insight_ts TIMESTAMPTZ)`
    
- `insights(insight_id PK, channel_id, seq BIGINT, ts, embedding …)` + `UNIQUE(channel_id, seq)`
    
- `subscriptions(user_id, channel_id, PRIMARY KEY(user_id, channel_id))`
    
- `user_cluster_hwm(user_id, channel_id, last_seq BIGINT, PRIMARY KEY(user_id, channel_id))`
    
- `user_stats(user_id PK, pending_insights_count BIGINT, last_clustered_at, last_active_at, cluster_version, plan)`
    

## Redis 

- `H ch:{c} -> current_seq, last_ts` 
    
- `H hwm:{u}:{c} -> last_seq` 
    
- `H us:{u} -> pending, last_clustered_at, last_active_at, cluster_version, plan, last_enqueued_at`
    
- `Z dirty:channels` — каналы с новыми инсайтами (score=timestamp)
    
- `SETNX lock:user:{u}` — лок на обработку
    
- `SET enq:user:{u} EX 300` — дедуп постановки задач
    

## Clusters DB

- `user_id, cluster_version, clusters[], updated_at`
    

## MongoDB (кэш фида)

- `{user_id, cluster_version, built_at, ttl, feed_payload}`
    

---

# 6) Планировщик — как отбирает кандидатов 

**Поток новизны (через dirty):**

1. Забираем до `MAX_DIRTY_CHANNELS_PER_TICK` каналов из `dirty:channels`.
    
2. Батчами получаем их подписчиков из `subscriptions`.
    
3. Для каждого пользователя считаем `pending = Σ(current_seq − HWM)` (через Redis; при отсутствии — из PG).
    
4. Фильтруем: активность + (pending≥N или время≥T) + cooldown.
    
5. Дедуп → ставим задачy `cluster_update{user_id}` воркерам.
    
**Обслуживание dirty:** обработанные элементы `ZREM`, новые придут сами.

> Если **Redis недоступен**, используем деград-режим: берём каналы из PG по `last_insight_ts`, подписчиков из `subscriptions`, считаем `pending` из PG. Плюс поток «по времени» — так же из PG. Лимитируем объёмы.

---

# 7) Воркер — что делает при обработке

1. Берёт задачу, ставит `lock:user:{u}`.
    
2. Пересчитывает `pending(u)` на сейчас:
    
    - **Если `pending==0` и триггер был «по времени»** → можно **пропустить** (версию не менять), либо «освежить ранжирование» без поднятия версии — по продуктовой политике.
        
    - **Если `pending>0`**:
        
        1. Формируем датасет **embeddings**: все инсайты из подписок за окно (напр., 30–60 дней) + новизна.
            
        2. Отправляем embeddings в **Clusterizer** (полный пересчёт).
            
        3. Сохраняем кластеры в Clusters DB.
            
        4. **`cluster_version++`**.
            
        5. **Сдвигаем HWM:** `HWM[u,c] = current_seq[c]` (по задействованным каналам).
            
        6. Обновляем `last_clustered_at = now`, инвалидируем кэш Mongo по версии.
            
3. Снимаем лок, чистим `enq:user:{u}`.
    
4. Логируем/метрики: длительность, размер датасета, bumped_version, ошибки/ретраи.
    

---

# 8) Типичные потоки

**A. Пришёл инсайт** → `insights.insert` → `channels.current_seq++` → `ZADD dirty:channels channel_id` → _всё_.  
**B. Тик планировщика** → отбор кандидатов (dirty + по времени) → постановка задач с дедупом.  
**C. Воркер** → пересборка по embeddings → `cluster_version++` (если была новизна) → HWM = current_seq → инвалидация кэша.  
**D. Чтение фида** → проверка `cluster_version` и TTL в Mongo → либо отдаём кэш, либо собираем через LLM API и обновляем.

---


# 9) Redis down

- Переключаемся в **DB-mode**: оба потока (новизна и время) читают из PG, лимитируя объёмы.
    
- После восстановления Redis:
    
    - реконструируем `dirty:channels` по `channels.last_insight_ts ≥ t0`;
        
    - ленивым прогревом возвращаем `HWM`/`us` в Redis.
        
- Redis — ускоритель, **не** источник истины.
    

