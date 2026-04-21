# Kittygram 🐈

[![Main Kittygram workflow](https://github.com/EvgeniyRudih/kittygram_final/actions/workflows/main.yml/badge.svg)](https://github.com/EvgeniyRudih/kittygram_final/actions/workflows/main.yml)

## Описание проекта
```bash
Kittygram — это социальная сеть для обмена фотографиями любимых питомцев. Пользователи могут создавать профили своих котов, делиться их фотографиями, добавлять забавные достижения и просматривать ленту питомцев других пользователей. Проект включает в себя настроенную систему CI/CD для автоматического тестирования и деплоя на удаленный сервер.
```

## Технологии (Стек)
```bash
* **Backend:** Python 3, Django, Django REST Framework, Djoser
* **Frontend:** React, Node.js
* **База данных:** PostgreSQL
* **Инфраструктура:** Docker, Docker Compose, Nginx, Gunicorn
* **CI/CD:** GitHub Actions
```

## Как развернуть проект

**1. Клонирование репозитория:**
```bash
git clone git@github.com:EvgeniyRudih/kittygram_final.git
cd kittygram_final
```
**2. Настройка окружения:**
```bash
Создайте файл .env в корневой директории проекта и заполните его по шаблону ниже.
```
**3. Запуск через Docker Compose (локально):**
```bash
# Сборка и запуск контейнеров
docker compose up -d --build

# Применение миграций базы данных
docker compose exec backend python manage.py migrate

# Сборка статики
docker compose exec backend python manage.py collectstatic --no-input
Проект будет доступен по адресу: http://localhost:9000/
```

**Шаблон заполнения .env**
```bash
Для работы проекта необходимо задать следующие переменные окружения:

Code snippet
# Настройки Django
SECRET_KEY=ваш_секретный_ключ_django
DEBUG=False
ALLOWED_HOSTS=127.0.0.1,localhost,ваш_домен

# Настройки базы данных PostgreSQL
POSTGRES_USER=kittygram_user
POSTGRES_PASSWORD=kittygram_password
POSTGRES_DB=kittygram
DB_HOST=db
DB_PORT=5432
```

**Авторы**
```bash
Backend & Инфраструктура: EvgeniyRudih

Frontend & Дизайн: Яндекс Практикум
```