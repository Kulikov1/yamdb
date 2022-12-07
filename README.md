[![Django-app workflow](https://github.com/Kulikov1/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)](https://github.com/Kulikov1/yamdb_final/actions/workflows/yamdb_workflow.yml)
# api_yamdb

## Описание.

Данный проект позволяет делать обзоры и давать оценку различным произведенияя, оставлять комментарии.

## Установка.
Установка Docker

Выполните установку docker для вашей операционной системы согласно инструкции на официальном сайте https://docs.docker.com/desktop/

Клонировать репозиторий и перейти в него в командной строке:
git clone https://github.com/Kulikov1/yamdb_final.git
cd yamdb_final



## Шаблон env файла
SECRET_KEY - Секретный ключ проекта Django

Данные БД Postgres:

DB_ENGINE - движок postgres

DB_NAME - имя БД

POSTGRES_USER - пользователь БД

POSTGRES_PASSWORD - пароль БД

DB_HOST - название сервиса (контейнера)

DB_PORT - порт для подключения к БД

## Примеры запросов.

"Регистрация нового пользователя": "http://127.0.0.1:8000/api/v1/auth/signup/"

"Получение JWT-токена": "http://127.0.0.1:8000/api/v1/auth/token/"

"Обращение к категориям": "http://127.0.0.1:8000/api/v1/categories/"

"Обращение к жанрам": "http://127.0.0.1:8000/api/v1/genres/"

"Обращение к произведениям": "http://127.0.0.1:8000/api/v1/titles/"

"Обращение к отзывам": "http://127.0.0.1:8000/api/v1/titles/{title_id}/reviews/"

"Обращение к комментариям": "http://127.0.0.1:8000/api/v1/titles/{title_id}/reviews/{review_id}/comments/"

