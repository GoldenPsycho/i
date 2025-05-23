# 📋 ШАБЛОН Регламента резервного копирования для заполнения игроком

---

## **ООО "СтальПрогресс"**  
### **Отдел бухгалтерии**  
### **Регламент резервного копирования бухгалтерских данных**

---

### 1. Цель документа

Обеспечить сохранность критически важных бухгалтерских данных, минимизировать потери информации при сбоях, обеспечить возможность оперативного восстановления работы отдела.

---

### 2. Объекты резервного копирования

- Базы данных 1С:Бухгалтерия
- Документы налоговой отчётности
- Архив расчётных ведомостей
- Договоры с контрагентами

---

### 3. Методики резервного копирования

> Выберите основную методику резервного копирования:
- [ ] Полный бэкап
- [ ] Инкрементальный бэкап
- [ ] Дифференциальный бэкап
- [ ] Реверсивный инкрементальный бэкап
- [ ] Синтетический полный бэкап
- [ ] Смарт-бэкап
- [ ] Непрерывная защита данных (CDP)

> Выберите дополнительную методику (опционально):
- [ ] Полный бэкап
- [ ] Синтетический полный бэкап
- [ ] Инкрементальный бэкап
- [ ] Нет

---

### 4. Параметры восстановления

| Параметр                          | Значение (заполняется игроком) |
|------------------------------------|-------------------------------|
| Максимальный период простоя (RTO) | __________ часов |
| Максимально допустимая потеря данных (RPO) | __________ часов изменений |

---

### 5. Покрываемые риски

Выберите риски, которые покрываются регламентом:
- [x] Потеря данных из-за аппаратных сбоев
- [x] Потеря данных из-за ошибок пользователя
- [x] Потеря данных из-за вирусной атаки
- [x] Потеря данных из-за катастроф (пожар, затопление)

*(можно убрать галочку, если игрок что-то забудет покрыть)*

---

### 6. Средства реализации

> Укажите компоненты инфраструктуры (игрок выбирает):

- Сервер хранения данных:  
  - [ ] Новый сервер  
  - [ ] Апгрейд существующего сервера  
  - [ ] Использование текущего оборудования

- Хранилище данных:
  - [ ] HDD RAID 1
  - [ ] SSD RAID 10
  - [ ] Облачное хранилище

- Программное обеспечение для резервного копирования:
  - [ ] Veeam
  - [ ] Acronis
  - [ ] Nakivo
  - [ ] Другое: __________

---

### 7. Расписание резервного копирования

| Операция                          | Время и частота (игрок заполняет) |
|------------------------------------|-------------------------------|
| Инкрементальные/Реверсивные копии  | __________ (например: каждые 3 часа) |
| Полный/Синтетический полный бэкап | __________ (например: раз в неделю ночью) |

---

### 8. Ответственные лица

| Должность              | Ответственный (заполняется игроком) |
|-------------------------|-------------------------------------|
| Настройка резервирования| __________ |
| Мониторинг состояния    | __________ |
| Контроль полноты данных | __________ |

---

### 9. Контроль исполнения

- [x] Ежедневная проверка успешности бэкапов
- [x] Еженедельная проверка полноты резервирования
- [x] Ежеквартальное тестовое восстановление данных
- [x] **Отправка статусов резервного копирования на почту руководителю ИБ**

*(этот пункт теперь выделен — и это важный чекбокс в сценарии!)*

---

# 📋 Пояснение

Все поля в **подчёркнутых зонах** и **чекбоксы** —  
это то, что игрок **должен заполнить, выбрать или утвердить сам**.

**Ошибки или пропуски в этих местах будут потом влиять:**
- На развитие инцидентов
- На успешность восстановления
- На отношения с другими подразделениями

---
