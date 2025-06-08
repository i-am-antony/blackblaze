# Web-BBC

Проект BlackBlaze — микросервисная система на базе Spring Boot, Apache HTTPD и PostgreSQL, разворачиваемая через Docker Compose.

## Запуск

1. Скопируйте `.env` и настройте переменные окружения.
2. Запустите команду:
   ```
   docker-compose up --build
   ```
3. Приложение будет доступно на портах 80 и 443.

## Структура

- `core` — основной сервис Spring Boot
- `cdn` — сервис статики на Apache HTTPD
- `proxy` — обратный прокси (nginx или другой)
- `psql` — база данных PostgreSQL

## Примечания

- Для HTTPS настройте сертификаты в proxy.
- Для разработки используйте volume для папки `db`.
