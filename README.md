[![Django-app workflow](https://github.com/Kulikov1/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)](https://github.com/Kulikov1/yamdb_final/actions/workflows/yamdb_workflow.yml)
# api_yamdb

## Описание.

Данный проект позволяет делать обзоры и давать оценку различным произведенияя, оставлять комментарии.

## Установка.
Установка Docker

Выполните установку docker для вашей операционной системы согласно инструкции на официальном сайте https://docs.docker.com/desktop/

- Запустите Docker Desktop

## Запуск контейнеров:

### 1. Клонируйте проект и перейдите в него:
```sh
git clone https://github.com/Kulikov1/yamdb_final.git
```
```sh
cd yamdb_final
```
### 2. Разверните проект:
```sh
docker-compose up -d
```

## Шаблон env файла
SECRET_KEY - Секретный ключ проекта Django

Данные БД Postgres:

DB_ENGINE - движок postgres

DB_NAME - имя БД

POSTGRES_USER - пользователь БД

POSTGRES_PASSWORD - пароль БД

DB_HOST - название сервиса (контейнера)

DB_PORT - порт для подключения к БД

## Примеры запросов:

### 1.`post` Добавление новой категории эндпоинт `api/v1/categories/`:
>Права доступа: Администратор.
```sh
{
    "name": "string",
    "slug": "string"
}
```
Пример успешного ответа:
```sh
{
    "name": "string",
    "slug": "string"
}
```
### 2.`get` Получение списка всех жанров эндпоинт `api/v1/genre/`:
>Права доступа: Доступно без токена.
Пример успешного ответа:
```sh
[
    {
        "count": 0,
        "next": "string",
        "previous": "string",
        "results": []
    }
]
```
### 3. `post` Добавление произведения эндпоинт `api/v1/titles/`:
>Права доступа: Администратор.
```sh
{
    "name": "string",
    "year": 0,
    "description": "string",
    "genre": [
        "string"
    ],
    "category": "string"
}
```
Пример успешного ответа:
```sh
{
    "id": 0,
    "name": "string",
    "year": 0,
    "rating": 0,
    "description": "string",
    "genre": [
        {}
    ],
    "category": {
        "name": "string",
        "slug": "string"
    }
}
```
### 4. `post` Добавление нового отзыва эндпоинт `api/v1/titles/{title_id}/reviews/`:
>Права доступа: Аутентифицированные пользователи.
```sh
{
    "text": "string",
    "score": 1
}
```
Пример успешного ответа:
```sh
{
    "id": 0,
    "text": "string",
    "author": "string",
    "score": 1,
    "pub_date": "2019-08-24T14:15:22Z"
}
```
### 5. `post` Добавление комментария к отзыву эндпоинт `api/v1/titles/{title_id}/reviews/{review_id}/comments/`:
>Права доступа: Аутентифицированные пользователи.
```sh
{
    "text": "string"
}
```
Пример успешного ответа:
```sh
{
    "id": 0,
    "text": "string",
    "author": "string",
    "pub_date": "2019-08-24T14:15:22Z"
}
```
### 6. `get` Получение списка всех пользователей эндпоинт `api/v1/users/`:
>Права доступа: Администратор.
Пример успешного ответа:
```sh
[
    {
        "count": 0,
        "next": "string",
        "previous": "string",
        "results": [
            {
                "username": "string",
                "email": "user@example.com",
                "first_name": "string",
                "last_name": "string",
                "bio": "string",
                "role": "user"
            }
        ]
    }
]
```
### 7. `post` Регистрация нового пользователя эндпоинт `api/v1/auth/signup/`:
>Права доступа: Доступно без токена.
```sh
{
    "email": "string",
    "username": "string"
}
```
Пример успешного ответа:
```sh
{
    "email": "string",
    "username": "string"
}
```
