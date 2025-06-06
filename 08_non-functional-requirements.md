## Нефункциональные требования

### 1. Пользовательский домен

1. Время аутентификации пользователя ≤ 1 сек при 10 тыс. RPS. Канал между пользователем и сервером должен обеспечивать минимальную пропускную способность не менее 5 Мбит/с.
2. Шифрование персональных данных. Необходимо использование AES-256, соответствие Закону о защите персональных данных
3. Защита от утечек паролей. В системе используется многофакторная авторизация (не менее двух факторов)
4. Поддержка роста количества пользователей до 5 млн. без деградации скорости авторизации
5. Uptime ≥ 99.5% времени
6. Защита от DDoS-атак. Введение автоматического ограничения запросов (Rate Limiting)

---

### 2. Социальный домен

1. Задержка при отправке сообщений не превышает 500 мс при 50 тыс. активных пользователях
2. Поддерживается работа групп до 10 тыс. участников с синхронным обновлением ленты
3. При сбое сервера восстановление данных занимает не более 2 минут
4. Система должна поддерживать горизонтальное масштабирование, позволяя добавлять новые серверы для обработки увеличивающейся нагрузки при пиковых нагрузках (например, онлайн мероприятие)

---

### 3. Тренировочный домен

1. Обработка данных с устройств проводится в режиме реального времени (задержка составляет не более 500 мс)
2. Погрешность трекинга GPS не превышает 5 метров
3. Поддерживается обработка более 1 млн. тренировок в день, хранение данных за 5 лет
4. В системе имеется возможность переключения на запасной сервис трекинга
5. В системе имеется возможность подключения упрощенной системы обработки получаемых данных при отказе ML-модели

---

### 4. Экипировочный домен

1. Загрузка каталога товаров занимает не более 2 сек при 100тыс. артикулов товаров. Канал между пользователем и сервером должен обеспечивать минимальную пропускную способность не менее 5 Мбит/с.
2. Время восстановления системы после сбоя не более 20 минут
3. Система должна поддерживать горизонтальное масштабирование, позволяя добавлять новые серверы для обработки увеличивающейся нагрузки
4. В системе реализована защита данных о платежах и заказах, соответствие стандартам PCI DSS.  

---

### 5. Маркетинговый домен

1. Для формирования / обновления пользовательских предложений за основу берется персональная истории активности
2. Локализация контента поддерживает не менее 10 регионов
3. Должна быть возможность запустить промо-акции параллельно на нескольких инстансах сервиса для распределения нагрузок
4. Система должна поддерживать ежегодный прирост количества участников акций пользователей на 20% и мгновенный на 60%

---

### 6. Интеграционный домен

1. Поддерживаются протоколы Bluetooth 5.0, ANT+, Wi-Fi Direct
2. При потере соединения с устройством более чем на 1 мин проводится синхронизации данных
3. Система поддерживает добавление интеграции с более 10 новыми моделями устройств в месяц без изменения API
4. Поддерживается автоматический переход на запасной канал связи при сбоях соединения

---

### 7. Финансовый домен

1. Операции оплаты поддерживают стандарт PCI DSS
2. Проведение транзакции занимает не более 3 сек при 1 тыс. операций / сек. Канал между пользователем и сервером должен обеспечивать минимальную пропускную способность не менее 5 Мбит/с.
3. Транзакции подтверждаются пользователем в ручном режиме
4. В системе ведется журнал событий для отслеживания истории действий

---

### 8. Административный домен

1. Система поддерживает Управление доступом на основе ролей с не менее 5 уровнями для модераторов
2. Логи администрирования хранятся не менее 1 года
3. Система поддерживает работу более 100 модераторов без конфликтов
4. Производится автоматическая блокировка подозрительных аккаунтов с последующим уведомлением администратора

---

### 9. Дополнительные сервисы (уведомления, поиск)

1. Доставка уведомления занимает не более 3 сек для 95% пользователей. Канал между пользователем и сервером должен обеспечивать минимальную пропускную способность не менее 5 Мбит/с.
2. Релевантность информационного поиска составляет более 0.9
3. Индексация данных (более 10 млн записей) в Elasticsearch должна занимать не более чем 2 часа
4. Доступно отключение отправки несущественных уведомлений при перегрузке
5. Взаимодействие сервисов между собой в части сценариев происходит через брокер сообщений
