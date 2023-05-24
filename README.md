
# api_yamdb

Описание: REST API для YaMDb Создан на основе библиотеки Django REST Framework (DRF)

YaMDb - это платформа для сбора отзывов и оценок по различным категориям.

Технологии Python 3.7

Django 3.2.15


### шаблон наполнения env-файла
DB_ENGINE

DB_NAME

POSTGRES_USER

POSTGRES_PASSWORD

DB_HOST

DB_PORT

### команды для запуска приложения в контейнерах
docker-compose exec web python manage.py migrate 

docker-compose exec web python manage.py createsuperuser

docker-compose exec web python manage.py collectstatic --no-input 

### Примеры запросов
Основные эндпоинты для аутентификации нового пользователя

Для аутентификации применены JWT-токены.

Создание JWT-токена:
http://127.0.0.1:8000/api/v1/jwt/create/

Токен необходимо передавать в заголовке каждого запроса, в поле Authorization. Перед самим токеном должно стоять ключевое слово Bearer и пробел.

Основные эндпоинты API
http://127.0.0.1:8000/api/v1/categories/
http://127.0.0.1:8000/api/v1/genres/
http://127.0.0.1:8000/api/v1/titles/

пример POST запроса на (http://127.0.0.1:8000/api/v1/categories/):

{
  "name": "string",
  
  "slug": "string"
}

### Статус работы workflow

![example workflow](https://github.com/OlesyaSim/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)

