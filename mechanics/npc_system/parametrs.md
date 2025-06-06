

# 👥 **СИСТЕМА ПЕРСОНАЖЕЙ (расширенная версия)**

---

## 🎯 Основные показатели и их логика:

| Показатель                  | Изменяется? | Формула расчёта |
|:-----------------------------|:------------|:----------------|
| **Профессиональные компетенции** | ❌ Нет | `ПрофКомпетенция = БазовоеЗначение` |
| **IT-компетенции**             | ✅ Меняются | `ITКомпетенция = БазовоеЗначение + ΔИзменение (от действий игрока)` |
| **Репутация игрока**           | ✅ Меняется | `РепИгрока = 5 + Σ(ИзменениеОтДиалогов)` |
| **Межличностная репутация**     | ✅ Меняется | `МежличРепутация(A, B) = Базовая + Σ(СобытияМежду A и B)` |

---

## 📜 **Формулы подробнее**

### 1. **Профессиональные компетенции**

**Фиксированная.**  
Определяется изначально.  
**Формула:**
```text
ПрофКомпетенция = Константа
```

---
### 2. **IT-компетенции**

**Меняются** в зависимости от общения, развития событий, поручений.

**Формула изменения:**
```text
ITКомпетенция = БазовоеЗначение + Σ(ИзменениеОтИгрока)
```
где  
- `ИзменениеОтИгрока` = +1 или -1 за определённые действия/реплики (например, научили использовать менеджер паролей — +1; обесценили ИТ-безопасность — -1).

---

### 3. **Репутация игрока в глазах персонажа**

**Изменяется** динамически.

**Формула:**
```text
РепИгрока = 5 + Σ(ИзменениеОтДиалогов)
```
где  
- `ИзменениеОтДиалогов` — баллы за стиль общения, характер решений (например: поддержали идею персонажа — +1, проигнорировали — -1, унизили — -2).

---

### 4. **Межличностная репутация**

**Изменяется** между персонажами.

**Формула:**
```text
МежличРепутация(A, B) = СтартовоеЗначение + Σ(СобытияМеждуПерсонажами)
```
где  
- События типа: «работали вместе над проектом» = +1, «сорвались в ссоре» = -2.

---



# 🔥 ВАЖНО

- Все **показатели от 0 до 10**.
- **Изменения ±1–±2** за одно событие, чтобы динамика оставалась управляемой.
- Слишком большие прыжки не допускаются, нужен **ограничитель** типа:
  ```text
  Если новое значение < 0, то 0
  Если новое значение > 10, то 10
  ```
