
---

# 📋 Полный сценарий: Встреча с производством

**Отдел:** Производство
**Персонаж:** Алексей Григорьевич Савельев (начальник производственного отдела)

---

## 🧩 Этап 1: Вступление

*(Игрок приходит на встречу в кабинет Алексея Савельева. За его спиной висит оперативный график выпуска продукции.)*

**Алексей Савельев:**

> "Если по делу — слушаю. У нас каждая минута на счёту."

---

## 🧩 Этап 2: Вопрос о допустимом периоде простоя

**Игрок задаёт вопрос:**
*"Какой допустимый период простоя производственных систем, чтобы не сорвать процесс выпуска?"*

| Стиль            | Реплика игрока                                                                                         | Изменение репутации | Вес на стиль    | Реакция Алексея Савельева                                                              |
| ---------------- | ------------------------------------------------------------------------------------------------------ | ------------------- | --------------- | -------------------------------------------------------------------------------------- |
| **Дипломат**     | "Хочу понять, где граница: после какого времени простоя начинается ущерб для производственного цикла?" | +1                  | +1 дипломат     | (внимательно) "Если больше четырёх часов — срывы смен, переработки, штрафы."           |
| **Технократ**    | "Нужно зафиксировать RTO. Как долго система может быть недоступна без критических последствий?"        | +0                  | +1 технократ    | (делово) "Не больше четырёх часов. Потом начинается ручное вмешательство и хаос."      |
| **Авторитарный** | "Сколько времени допустим простой без остановки линии? Говорите конкретно."                            | -2                  | +1 авторитарный | (жёстко) "Четыре часа. А теперь позволь работать."                                     |
| **Инноватор**    | "Можно ли временно переводить заказы на резервный планшет мастера, чтобы не прерывать смену?"          | +0                  | +1 инноватор    | (с сомнением) "В теории да, но с планшетов запускать смену — рискованно. Надо думать." |

🔹 **Дополнительная реплика Алексея при дипломатичном/технократичном подходе:**

> "Если всё ляжет — не восстановим техпроцессы, пойдём вслепую. Лучше сделать копии каждые 3 часа."

---

## 🧩 Этап 3: Вопрос о критичных данных

**Игрок задаёт вопрос:**
*"Какие данные критичны для производства и обязательно должны быть защищены?"*

| Стиль            | Реплика игрока                                                                          | Изменение репутации | Вес на стиль    | Реакция Алексея Савельева                                                                           |
| ---------------- | --------------------------------------------------------------------------------------- | ------------------- | --------------- | --------------------------------------------------------------------------------------------------- |
| **Дипломат**     | "Хочу понимать, какие данные реально важны. Что нельзя потерять ни при каких условиях?" | +1                  | +1 дипломат     | (серьёзно) "Спецификации, графики смен, техкарты, отчёты MES — всё, что обеспечивает производство." |
| **Технократ**    | "Нужен список конкретных систем и баз, критичных для производственного процесса."       | +0                  | +1 технократ    | (делово) "MES, сменные задания, техпроцессы. Без них — линия встанет."                              |
| **Авторитарный** | "Что конкретно должно быть в резерве? Назовите все пункты."                             | -2                  | +1 авторитарный | (сухо) "Вот список. Но повторю: подход должен быть системный."                                      |
| **Инноватор**    | "А если зашить выгрузку сменных заданий в защищённый канал — это поможет в аварии?"     | +0                  | +1 инноватор    | (одобрительно) "Да, такая автоматизация — это круто. Главное — чтобы мастер успел это запустить."   |

🔹 **Дополнительная реплика Алексея:**

> "Если исчезнут техкарты — всё. Линия стоит. Люди ждут. Начальство кипит. Перезапуск — минимум полдня."

---

## 🧩 Этап 4: Вопрос о последствиях утраты данных

**Игрок задаёт вопрос:**
*"Какие последствия ждут производство, если потеряются важные данные?"*

| Стиль            | Реплика игрока                                                                                 | Изменение репутации | Вес на стиль    | Реакция Алексея Савельева                                                                 |
| ---------------- | ---------------------------------------------------------------------------------------------- | ------------------- | --------------- | ----------------------------------------------------------------------------------------- |
| **Дипломат**     | "Хочу предусмотреть все риски, чтобы заранее исключить простои и потери."                      | +1                  | +1 дипломат     | (вдумчиво) "Срыв смен, переработка, отказ клиента. Убытки идут сразу."                    |
| **Технократ**    | "Каковы конкретные убытки и нарушения при утрате производственных данных?"                     | +0                  | +1 технократ    | (делово) "Срыв по контракту — до миллиона убытка. И штрафы от заказчика."                 |
| **Авторитарный** | "Чётко: потери, санкции, остановки. По пунктам."                                               | -2                  | +1 авторитарный | (сдержанно) "Данные ушли — смена стоит. Контракт срываем. Крик сверху. Всё."              |
| **Инноватор**    | "А есть ли резервные источники управления — например, планшет с локальной копией техпроцесса?" | +0                  | +1 инноватор    | (в раздумьях) "Мы пробовали. Если настроить правильно — спасает, но риск ошибки высокий." |

🔹 **Дополнительная реплика Алексея:**

> "У нас был случай — файл задания повредился. Цех встал. В итоге — переработка и устный выговор всей смене."

---

## 📚 Нормативная база и аргументы от Савельева:

* **ГОСТ Р 56610-2015:** Информационная безопасность в производстве.
* **ТК РФ, ст. 91–99:** Нарушение режима труда и графика — административная ответственность.
* **Внутренние KPI:** Выполнение сменного задания и сроков.
* **Контракты с подрядчиками:** Срыв сроков — до 10% от стоимости по договору.

---



# 📋 Дополнительные реплики Алексея Савельева для игры

---

## Эти реплики могут:

* Раскрывать **технические и организационные особенности производства**,
* Подсказывать **узкие места и критичные риски**,
* Вовлекать игрока в реальные последствия простоев и срывов смен,
* Создавать **живую атмосферу цеха**.

---

## 🟦 Реплики-подсказки (при нормальном/позитивном общении)

* 💬 "Если пропадёт техкарта — станок стоит. Даже опытный наладчик не запустит наугад."
* 💬 "Мы работаем в три смены. Лучше делать резервные копии хотя бы каждые 4 часа."
* 💬 "Цеху нужен стабильный доступ к MES. Без него ни один мастер не выпустит смену."
* 💬 "Хорошо бы настроить резервный доступ к сменным заданиям с планшета начальника смены."
* 💬 "У нас было: из-за сбоя в 1С производство встало. С тех пор я требую — дублируйте всё!"

---

## 🟥 Реплики-предупреждения (если игрок грубый или слишком технарь)

* 💬 "Вы мне сейчас про скрипты и процедуры, а у меня линия стоит. Мне нужен результат, а не лекция."
* 💬 "Если сделаете копию не той базы — получите жалобу на срыв смены. Мастера разнесут ИТ."
* 💬 "Производство — это не офис. Тут сбой в 10 минут — это 100 деталей в браке."
* 💬 "Простите, но ‘ещё протестируем позже’ — это не вариант. Тут всё должно работать сейчас."

---

## 🟩 Реплики-идеи (если игрок креативит или ведёт диалог в стиле инноваций)

* 💬 "Если бы была карта запуска смен на планшете — можно было бы обойтись без основной системы в аварии."
* 💬 "Интересно, если мы зашьём техпроцессы в отдельный модуль, доступный даже при сбое MES..."
* 💬 "Можно ли сделать резервную копию всех отчётов прямо на терминале сменного мастера?"

---

## 🟥 Скрытые угрозы (если игрок раздражает или игнорирует риски)

* 💬 "Срыв смены — это не только убытки. Это срыв контракта. Это звонок от директора мне. А потом — вам."
* 💬 "Пока вы спорите, у нас линия простаивает. Каждый час простоя — минус 200 000 по KPI."
* 💬 "Если восстановим из старой копии — детали уйдут не по той спецификации. Будет скандал с ОТК."
* 💬 "Вы хотите, чтобы потом рабочим объясняли, почему они перерабатывают из-за сбоя системы?"
* 💬 "Отчёт ушёл с ошибкой из-за утраты данных — клиент уходит. Всё. Без объяснений."

---

## 📚 Что он может упомянуть при обострении разговора:

* **ГОСТ Р 56610-2015:** Стандарты по ИБ в производственных системах.
* **Контракты с клиентами:** Срыв сроков = штрафы, отзыв доверия.
* **Внутренние KPI производства:** За срыв — премий нет, переработки, внеплан.
* **Политика качества:** Нарушение стандартов — остановка производства по решению службы ОТК.

---

## 📌 Где использовать эти реплики в игре:

* При успешной беседе (дипломат, технократ, инноватор) — как награда или инсайт.
* При раздражении персонажа — как реакция на жёсткий стиль.
* Автоматически — после ключевых фраз или событий (например, обсуждение MES, техпроцессов, времени восстановления).

---


# 📋 Полное описание: Выбор метода резервного копирования для производства

## 🏩 Начальная инфраструктура (актуализированная)

* Сервер:

  * **8 ядер CPU**, **32 ГБ RAM**
  * HDD SATA 4 ТБ (RAID 1)
* Сеть: 1 Гбит/с Ethernet
* Операционная система: Windows Server Standard
* Программное обеспечение: Устаревший плановый экспорт файлов на NAS
* Мониторинг резервного копирования отсутствует
* Средний объём производственных файлов и MES-базы: \~200–250 ГБ

---

## 📋 Методы резервного копирования: Влияние + Требования + Бюджет

---

### 📦 Полный бэкап

**Как влияет:**

* Существенная нагрузка на диск в ночное время
* Производственные логи и спецификации копируются целиком

**Что нужно увеличить:**

* Хранилище: нужно минимум +4 ТБ
* ПО: требуется лицензия Acronis или аналог

**Бюджет:**

* HDD расширение: ≈ 100 000 ₽
* Acronis Standard: ≈ 60 000 ₽

**Итого:** **160 000 ₽**

---

### 📦 Инкрементальный бэкап

**Как влияет:**

* Лёгкая нагрузка
* Риск утраты при сбое одного из инкрементов

**Что нужно увеличить:**

* SSD хранилище под дельты
* ПО с проверкой целостности цепочек

**Бюджет:**

* Nakivo Essentials: ≈ 40 000 ₽
* SSD-хранилище: ≈ 70 000 ₽

**Итого:** **110 000 ₽**

---

### 📦 Дифференциальный бэкап

**Как влияет:**

* Средняя нагрузка
* Размер копии увеличивается с каждым днём

**Что нужно увеличить:**

* HDD под бэкапы

**Бюджет:**

* HDD: ≈ 50 000 ₽
* Veeam Community Edition (бесплатно)

**Итого:** **50 000 ₽**

---

### 📦 Зеркальный бэкап

**Как влияет:**

* Высокая стоимость
* Риск шифровки сразу обеих копий

**Что нужно увеличить:**

* SSD RAID массив + отдельное устройство хранения

**Бюджет:**

* RAID10 на 4×2 ТБ SSD: ≈ 240 000 ₽
* Резервный NAS/сервер: ≈ 120 000 ₽

**Итого:** **360 000 ₽**

---

### 📦 Реверсивный инкрементальный бэкап

**Как влияет:**

* Быстрое восстановление
* Высокие требования к оборудованию

**Что нужно увеличить:**

* Апгрейд CPU и RAM
* SSD RAID10

**Бюджет:**

* Увеличение CPU/RAM: ≈ 150 000 ₽
* RAID SSD: ≈ 240 000 ₽
* Veeam Essentials: ≈ 120 000 ₽

**Итого:** **510 000 ₽**

---

### 📦 Смарт-бэкап

**Как влияет:**

* Гибкая настройка с минимальной нагрузкой

**Что нужно увеличить:**

* ПО с кастомной автоматизацией и скриптами

**Бюджет:**

* Acronis Advanced или Nakivo Enterprise: ≈ 90 000 ₽
* HDD 2 ТБ: ≈ 40 000 ₽

**Итого:** **130 000 ₽**

---

### 📦 Непрерывная защита данных (CDP)

**Как влияет:**

* Постоянная нагрузка на сеть и сервер

**Что нужно увеличить:**

* Новый сервер под CDP
* Сеть 10 Гбит/с
* RAID SSD

**Бюджет:**

* Сервер CDP: ≈ 800 000 ₽
* Сетевое оборудование 10G: ≈ 300 000 ₽

**Итого:** **1 100 000 ₽**

---

### 📦 Синтетический полный бэкап

**Как влияет:**

* Умеренная нагрузка ночью

**Что нужно увеличить:**

* SSD под сборку + ПО

**Бюджет:**

* Veeam Standard: ≈ 100 000 ₽
* SSD 2 ТБ: ≈ 120 000 ₽

**Итого:** **220 000 ₽**

---

### 📦 Бесконечно-инкрементальный бэкап

**Как влияет:**

* Требует грамотной архитектуры
* Самый экономный по объёму, но сложен в поддержке

**Что нужно увеличить:**

* ПО корпоративного уровня

**Бюджет:**

* Commvault или Rubrik: ≈ 300 000 ₽
* Обслуживание

**Итого:** **300 000 ₽**

---

# 📋 Таблица итогового сравнения

| Метод                       | Требования к серверам | Диски    | ПО                | Бюджет ₽  |
| --------------------------- | --------------------- | -------- | ----------------- | --------- |
| Полный                      | Место                 | HDD +    | Acronis           | 160 000   |
| Инкрементальный             | Умеренные             | SSD +    | Nakivo            | 110 000   |
| Дифференциальный            | Лёгкие                | HDD      | Veeam (бесплатно) | 50 000    |
| Зеркальный                  | Высокие               | RAID SSD | Стандартное       | 360 000   |
| Реверсивный инкрементальный | Очень высокие         | RAID SSD | Veeam Essentials  | 510 000   |
| Смарт-бэкап                 | Средние               | HDD +    | Acronis Advanced  | 130 000   |
| CDP                         | Очень высокие         | RAID SSD | Спец. системы     | 1 100 000 |
| Синтетический полный        | Средние               | SSD      | Veeam Standard    | 220 000   |
| Бесконечно-инкрементальный  | Высокие               | HDD/SSD  | Commvault         | 300 000   |

---


# 📋 ИТОГО: Логичный выбор для производства

* 🏆 **Оптимальный выбор:**

  * **Реверсивный инкрементальный бэкап** + **Синтетический полный бэкап**

* 💬 **Почему:**

  * Быстрое восстановление
  * Минимизация потерь данных
  * Сбалансированная нагрузка на серверы
  * Учёт потоков обновления планов, заказов и оборудования

* 💸 **Оценка бюджета:**
  **\~510 000 ₽** на модернизацию серверной инфраструктуры и ПО.

---

# Составление регламента

## [https://github.com/GoldenPsycho/i/scenarios/Backup/Prod\_backup/Prod\_backup.md](https://github.com/GoldenPsycho/i/scenarios/Backup/Prod_backup/Prod_backup.md)

# 📋 Полный сценарий согласования регламента резервного копирования с ИТ по ВСЕМ методам

[https://github.com/GoldenPsycho/i/scenarios/Backup/IT\_backup\_reaction.md](https://github.com/GoldenPsycho/i/scenarios/Backup/IT_backup_reaction.md)

---

## Если руководство дало согласие

# Механика Закупок

[https://github.com/GoldenPsycho/i/mechanics/money/mony.md](https://github.com/GoldenPsycho/i/mechanics/money/mony.md)

---

---

# 📋 Этап 3: Реализация регламента резервного копирования через техника

---

## 📌 Персонаж:

**Техник отдела ИБ** —
имя: **Андрей Бойко**, 20 лет, начинающий ИБ-специалист.

**Описание:**
Компетентный, но иногда недопонимает тонкости процедур. Может недонастроить сложные вещи без контроля.

---

## 📌 1. Начальный диалог: Поручение на реализацию регламента

| Стиль игрока     | Реплика                                                                                       | Изменение репутации | Вес на стиль    | Реакция Андрея                                  |
| ---------------- | --------------------------------------------------------------------------------------------- | ------------------- | --------------- | ----------------------------------------------- |
| **Дипломат**     | "Андрей, твоя помощь очень важна. Нужно корректно внедрить регламент резервного копирования." | +1                  | +1 Дипломат     | (спокойно) "Конечно, всё сделаю в лучшем виде." |
| **Технократ**    | "Прошу строго следовать техническим параметрам регламента. Никаких отклонений."               | 0                   | +1 Технократ    | (серьёзно) "Принято. Всё по инструкции."        |
| **Авторитарный** | "Есть приказ: настроить резервирование по регламенту. Без самодеятельности."                  | -2                  | +1 Авторитарный | (напряжённо) "Как скажете..."                   |
| **Инноватор**    | "Если увидишь возможность дополнительно оптимизировать — аккуратно предложи."                 | 0                   | +1 Инноватор    |                                             |




---

## 📌 2. Дополнительная необязательная реплика

Игрок может дополнительно сказать:

💬 *"И ещё, пожалуйста, настрой автоматическую отправку отчётов о резервном копировании по производственным данным на мою почту."*

* Если игрок не скажет — отчётность по резервированию критичных производственных систем не будет настроена.
* Это усложнит своевременное выявление ошибок и может повлечь **простой оборудования** при инциденте.

---

## 📌 3. Андрей реализует настройку

**Качество настройки зависит от:**

* Уровня доверия и стиля общения с техником,
* Сложности выбранной схемы резервного копирования (CDP, бесконечно-инкрементальные — рискованные).

**Типовые ошибки:**

* Не включена база данных MES-системы,
* Отсутствуют копии логов с производственного оборудования,
* Не включены уведомления об ошибках.

---

## 📌 4. Андрей сообщает:

💬 *"Настроил резервирование по производственным системам. Всё готово к работе."*

---

## 📌 5. Действия игрока:

| Действие               | Последствия                                                                      |
| ---------------------- | -------------------------------------------------------------------------------- |
| **Проверить работу**   | Получает лог-файлы, может вовремя заметить упущения или технические сбои         |
| **Довериться технику** | Увеличивает риск незаметных сбоев → возможный простой производственного процесса |

---

## 📌 6. Проверка работы: диалог

**Игрок просит подтверждение правильности настройки резервного копирования:**

| Стиль игрока     | Реплика                                                                                | Изменение репутации | Вес на стиль    | Реакция Андрея                          |
| ---------------- | -------------------------------------------------------------------------------------- | ------------------- | --------------- | --------------------------------------- |
| **Дипломат**     | *"Андрей, можешь выслать конфигурацию резервирования по производству? Для отчёта."*    | +1                  | +1 Дипломат     | "Конечно. Сейчас всё оформлю и пришлю." |
| **Технократ**    | *"Нужно сверить конфигурации с регламентом по производству. Пришли файл."*             | 0                   | +1 Технократ    | "Хорошо. Отправлю прямо сейчас."        |
| **Авторитарный** | *"Присылай полную конфигурацию бэкапа производственных систем. Срочно."*               | -2                  | +1 Авторитарный | (напряжённо) "Отправлю... сейчас..."    |
| **Инноватор**    | *"Если увидишь, что можно улучшить резервное копирование по станкам или IoT — скажи."* | 0                   | +1 Инноватор    | "Есть пара идей! Сейчас проверю."       |

---


---

## 📌 7. Что присылает Андрей

## 📋 Конкретные примеры данных от техника по каждой методике (Производство)

---

### 📦 Полный бэкап

> **Файл:**
> `prod_backup_schedule_full.txt`
> **Содержимое:**
>
> ```
> Тип: Полный бэкап
> Данные: MES_производство, PLC_настройки, Архив_сменных_отчётов
> Периодичность: Ежедневно в 01:00
> Хранилище: PROD-Backup01
> Уведомления: Отключены
> ```

---

### 📦 Инкрементальный бэкап

> **Файл:**
> `prod_incremental_plan.json`
> **Содержимое:**
>
> ```json
> {
>   "BaseBackup": "Понедельник 01:00",
>   "Increments": [
>     "Вторник 01:00",
>     "Среда 01:00",
>     "Четверг 01:00",
>     "Пятница 01:00"
>   ],
>   "CheckedIntegrity": false
> }
> ```

---

### 📦 Дифференциальный бэкап

> **Файл:**
> `prod_diff_backup_report.csv`
> **Содержимое:**
>
> ```
> Дата полного бэкапа: Понедельник
> Дифференциалы:
> Вторник: OK
> Среда: OK
> Четверг: OK
> Пятница: OK
> Хранилище: PROD_Backup_Storage
> ```

---

### 📦 Зеркальный бэкап

> **Файл:**
> `prod_mirror_config.txt`
> **Содержимое:**
>
> ```
> Тип резервирования: Зеркалирование
> Источник: Основной сервер SCADA
> Приёмник: Сервер резервного копирования 192.168.2.55
> Метод копирования: Прямая синхронизация, без версионности
> Уведомления: Нет
> ```

---

### 📦 Реверсивный инкрементальный бэкап

> **Файл:**
> `prod_reverse_inc_config.yaml`
> **Содержимое:**
>
> ```yaml
> BaseBackup: Еженедельно в воскресенье 02:00
> ReverseIncrements:
>   - Понедельник 08:00
>   - Среда 08:00
>   - Пятница 08:00
> Проверка целостности: Да
> Хранилище: PROD_RAID_Backup
> ```

---

### 📦 Смарт-бэкап

> **Файл:**
> `prod_smart_backup_script.sh`
> **Содержимое:**
>
> ```bash
> # Полный бэкап
> 0 1 * * 0 full_prod_backup.sh
> # Инкременты
> 0 1 * * 1-6 incremental_prod_backup.sh
> # Проверка нагрузки на контроллеры
> 0 2 * * * check_plc_health.sh
> ```
>
> **Описание:**
>
> ```
> Стратегия: Полный бэкап раз в неделю + ежедневные инкременты
> Отчёты: Автоматически отправляются ИБ-руководителю
> ```

---

### 📦 CDP (Continuous Data Protection)

> **Файл:**
> `prod_cdp_activity_log.txt`
> **Содержимое:**
>
> ```
> 10:01:12 MES_операция_запись_рецепта → зафиксировано
> 10:02:45 Настройки контроллера Siemens_203 обновлены
> 10:04:10 Лог PLC_линия_3 изменён → синхронизировано
> ...
> ```

---

### 📦 Синтетический полный бэкап

> **Файл:**
> `prod_synthetic_full_assembly.log`
> **Содержимое:**
>
> ```
> 00:30 Начата сборка синтетической копии
> 00:45 Объединение данных завершено
> 01:10 Проверка на консистентность пройдена
> Хранилище: PROD_Syn_Backup01
> ```

---

### 📦 Бесконечно-инкрементальный бэкап

> **Файл:**
> `prod_forever_increment_list.txt`
> **Содержимое:**
>
> ```
> Полный бэкап создан: 01.05.2025
> Инкременты:
> 02.05.2025 - Обновление SCADA схемы
> 03.05.2025 - Изменение рецепта линии 2
> 04.05.2025 - Импорт новых параметров оборудования
> ...
> Проверка цепочки: Включена
> ```

---

## 📌 8. Сравнение с регламентом

**Игрок должен самостоятельно сверить:**

* Частоту и временные окна резервирования
* Полноту охвата производственных систем (MES, SCADA, PLC, отчёты)
* Наличие уведомлений и проверок целостности
* Соответствие методики установленному регламенту

🛠 Если не соответствует — игрок может инициировать дополнительную проверку или донастройку через диалог с техником (см. блок ниже).

---

# 📋 Пример — как это будет видно игроку:

---

**Игрок выбрал ( Дипломат ):**
*"Понимаю, что настройка сложная. Давайте вместе исправим и доведём всё до нужного уровня."*

**Андрей:**
*"Конечно! Спасибо за доверие. Сейчас всё поправлю."*

(Репутация +1, Дипломатия +1)

Через некоторое время...

**Файл:** `prod_reverse_inc_config.yaml` (обновённый)
**Содержимое:**

```yaml
BaseBackup: Еженедельно в воскресенье 02:00
ReverseIncrements:
  - Понедельник 08:00
  - Среда 08:00
  - Пятница 08:00
Проверка целостности: Да
Уведомления: Включены (email руководителю ИБ)
Хранилище: PROD_RAID_Backup
```

📅 Всё совпадает с регламентом!

---


---

## 📋 Ошибки техника при настройке резервного копирования (производство)

(в зависимости от выбранной методики)

---

### 📦 Полный бэкап

**Ошибки:**

* Настроен только на офисные документы, а не на технологические чертежи и схемы.
* Нет уведомлений об ошибке.

**Последствия:**

* В случае сбоя часть техдокументации и планов выпуска теряется.
* Производственный процесс встаёт минимум на сутки.

---

### 📦 Инкрементальный бэкап

**Ошибки:**

* Не включены логи машин и SCADA-данные.
* Нет контроля цепочек инкрементов.

**Последствия:**

* Восстановление невозможно из-за одного потерянного файла.
* Простой оборудования из-за отсутствия данных настройки.

---

### 📦 Дифференциальный бэкап

**Ошибки:**

* Дифференциалы копируются раз в 3 дня вместо ежедневного режима.
* Логика версии техпроцессов не сохраняется.

**Последствия:**

* Откат на неактуальную версию управляющих программ.
* Риск поломки или выхода продукции с браком.

---

### 📦 Зеркальный бэкап

**Ошибки:**

* Нет защиты от заражения или ошибок оператора.
* Нет журналов контроля изменений.

**Последствия:**

* Ошибка или вирус моментально дублируется на зеркало.
* Потеря всех текущих данных управления.

---

### 📦 Реверсивный инкрементальный бэкап

**Ошибки:**

* Не настроено сохранение внешних зависимостей (например, шаблонов или моделей САПР).
* Отключены уведомления.

**Последствия:**

* Восстановление возможно, но не полностью.
* Производственный участок запускается с ограничениями.

---

### 📦 Смарт-бэкап

**Ошибки:**

* Логика расписания не учитывает ночные смены.
* Уведомления отправляются на неактуальный e-mail.

**Последствия:**

* Бэкапы пропускаются, если смена работала ночью.
* Отсутствие уведомлений об ошибках → потеря данных незаметна.

---

### 📦 CDP

**Ошибки:**

* Не настроены исключения по временным файлам и буферам оборудования.
* Слабое шифрование потока.

**Последствия:**

* Быстрый рост объёма → переполнение хранилища.
* Нарушение политики ИБ по ГОСТ/ФСТЭК.

---

### 📦 Синтетический полный бэкап

**Ошибки:**

* Не выделено отдельное окно на сборку.
* Сборка идёт во время запуска линий.

**Последствия:**

* Резкое падение производительности.
* Риски остановки участка.

---

### 📦 Бесконечно-инкрементальный бэкап

**Ошибки:**

* Цепочка не обновлялась больше месяца.
* Нет ручной контрольной точки.

**Последствия:**

* Любой сбой — потеря 100% истории изменений.

---

## 📋 Как это связано с действиями игрока

| Проверил настройки | Результат                                                                |
| ------------------ | ------------------------------------------------------------------------ |
| Да                 | Ошибки найдены и устранены → инцидент не случается или легко устраняется |
| Нет                | Ошибки остаются скрытыми → серьёзный инцидент и падение репутации        |

---



