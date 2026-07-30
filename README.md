# DevOps Тестовое задание
## Запуск проекта

1. Клонировать репозиторий:
```bash
git clone <url-репозитория>
cd Test
```

2. Копировать .env.example как .env
```bash
cp .env.example .env
```

3. Заполнить .env

4. Запустить проект:
```bash
docker-compose up -d
```
## Проверка работоспособности
1. Проверить работоспособность с сервера:
```bash
curl http://localhost
```
Ожидаемый ответ: Hello from Effective Mobile!
2. Через браузер: 
Перейти по адресу http://localhost. 
Ожидаемый ответ: Hello from Effective Mobile!

## Архитектура
```
Пользователь ---> порт 80 ---> Nginx ---> backend:8080 ---> Python Flask
```

Nginx выступает как reverse-proxy, принимает запросы на порту 80 и перенаправляет их на бэкенд.
Backend (Python/Flask) слушает на порту 8080 и недоступен с хоста напрямую, только через внутреннюю Docker-сеть.

## Tехнологии
- Docker и Docker Compose
- Python 3.11 и Flask
- Nginx (официальный образ)
- Git
