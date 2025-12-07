# Explore API v8 — Backend

## Деплой на Railway

1. Зайди на https://railway.app
2. Нажми "New Project" → "Deploy from GitHub repo" или "Empty Project"
3. Если Empty Project:
   - Нажми "Add Service" → "Empty Service"
   - В настройках сервиса нажми "Settings" → "Upload Files"
   - Загрузи все файлы из этой папки (server.js, package.json)
4. Railway автоматически определит Node.js и запустит сервер
5. Перейди во вкладку "Settings" → "Networking" → "Generate Domain"
6. Скопируй полученный URL (например: explore-v8-production.up.railway.app)
7. Этот URL нужно вставить в HTML файл фронтенда

## Переменные окружения (опционально)
- PORT — порт сервера (Railway устанавливает автоматически)

## Проверка работы
Открой в браузере: https://YOUR-RAILWAY-URL/api/content
Должен вернуться JSON с контентом приложения.

## Структура API

- GET /api/user/:id/status — статус пользователя
- POST /api/register — регистрация
- POST /api/join — присоединение по коду
- GET /api/couple/:id/chat — чат пары
- POST /api/couple/:id/chat — отправить сообщение
- GET /api/couple/:id/wishes — тайные желания
- POST /api/couple/:id/wishes — сохранить желания
- GET /api/couple/:id/tests — результаты тестов
- POST /api/couple/:id/tests — сохранить результат
- GET /api/content — весь контент приложения
