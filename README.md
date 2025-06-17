### Hexlet tests and linter status:
[![Actions Status](https://github.com/AlexMaster001/devops-for-programmers-project-74/actions/workflows/hexlet-check.yml/badge.svg)](https://github.com/AlexMaster001/devops-for-programmers-project-74/actions)
[![ci](https://github.com/AlexMaster001/devops-for-programmers-project-74/actions/workflows/push.yml/badge.svg)](https://github.com/AlexMaster001/devops-for-programmers-project-74/actions/workflows/push.yml)

Упаковано с помощью Docker Compose
Описание
Этот проект является частью курса DevOps для программистов на Hexlet.
В рамках курса студенты учатся создавать Docker-образ приложения js-fastify-blog, соответствующего 12-факторной архитектуре, которая минимизирует различия между средами разработки и продакшена.

Для настройки среды используются Docker , Docker Compose и Make . CI/CD используется для запуска тестов и публикации образа в репозитории Docker Hub .

Требования
Docker
Docker Compose (версия 1.27.0 или выше)
Make
Настройка
Клонирование репозитория
bash


1
2
git clone https://github.com/AlexMaster001/devops-for-programmers-project-74.git 
cd devops-for-programmers-project-74
Создание файла .env
bash


1
make ensure-env
⚠️ Убедитесь, что вы отредактировали переменные в .env, если они не совпадают с вашей конфигурацией. 

Запуск окружения
bash


1
make compose-setup
Запуск приложения
Разработка
bash


1
make compose-dev
После запуска приложение будет доступно по адресу: https://localhost

Тестирование
bash


1
make compose-test
Тесты проверяют работу API, миграции базы данных и логику CRUD-операций над статьями.

Работа с Docker Hub
Использование готового образа
bash


1
docker run --rm -it -p 8080:8080 -e NODE_ENV=development alexkirsanov/devops-for-programmers-project-74 make dev
Приложение станет доступным по адресу: http://localhost:8080
