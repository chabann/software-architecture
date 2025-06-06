# Стоимость владения системой (TCO)

## Основные категории затрат

**CAPEX (капитальные расходы):**  
- Лицензии на ПО (СУБД, системы мониторинга, Kubernetes).  
- Покупка/аренда оборудования (серверы, сетевое оборудование).  
- Разработка архитектуры и первоначальное внедрение.  

**OPEX (операционные расходы):**  
- Затраты на инфраструктуру (облачные ресурсы, виртуальные машины, хранилища, CDN).  
- Техподдержка и обслуживание.  
- Зарплаты команды (DevOps, разработчики, администраторы).  
- Энергопотребление и охлаждение (для on-premise).  
- Обновление лицензий и ПО.  

---

## Исходные данные и предположения  
- Стартовая база пользователей: 10 000 активных пользователей  
- Рост пользователей: 100% в год (примерно удваивается ежегодно)  
- Начальный объем данных: 5 ТБ  
- Рост данных: 150% в год (учитывая логи, метрики, тренировки и т.д.)  
- Использование облачной инфраструктуры (IaaS/PaaS) с оплатой по потреблению  
- Команда поддержки: 5 человек в первый год, рост на 50% к 5-му году  
- Лицензии и ПО: ежегодное продление с ростом стоимости на 5% в год  
- Примерные затраты на первый год — 20 млн рублей (включая все категории)

---

## Примерный расчет TCO

| Год  | Пользователи (тыс.) | Объем данных (ТБ) | Затраты на инфраструктуру (млн руб) | Затраты на поддержку и зарплаты (млн руб) | Лицензии и ПО (млн руб) | Общие затраты (млн руб) |
|-------|---------------------|-------------------|-------------------------------------|-------------------------------------------|-------------------------|-------------------------|
| 1     | 10                  | 5                 | 10                                  | 5                                         | 5                       | 20                      |
| 2     | 20                  | 7.5               | 15                                  | 7.5                                       | 5.25                    | 27.75                   |
| 5     | 160                 | 28.4              | 50                                  | 18                                        | 6.1                     | 74.1                    |

---

## Обоснование расчетов

- **Инфраструктура:**  
  Рост пользователей и данных требует увеличения серверных мощностей, баз данных, сетевых ресурсов и систем кэширования. Стоимость облачных ресурсов масштабируется примерно пропорционально нагрузке и объему данных.  

- **Поддержка и зарплаты:**  
  С ростом системы увеличивается нагрузка на DevOps, администраторов, инженеров поддержки и разработчиков, что отражается в росте фонда оплаты труда.  

- **Лицензии и ПО:**  
  Продление лицензий на ПО и сервисы с ежегодным ростом стоимости (инфляция, обновления).  

- **Дополнительные расходы:**  
  Обучение команды, расходы на безопасность, интеграцию с устройствами и сторонними сервисами, резервное копирование и аварийное восстановление.

