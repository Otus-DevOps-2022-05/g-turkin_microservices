# g-turkin_microservices
g-turkin microservices repository

# Выполнено ДЗ № 16 Gitlab CI. Построение процесса непрерывной интеграции

 - [X] Основное ДЗ
 - [ ] Задание со *

## В процессе сделано:
- развернут Gitlab CI на локальной машине используя docker-compose
- в gitlab создана гурппа homework и  проект example
- создан пайплайн при помощи файла .gitlab-ci.yml
- поднят раннер при помощи докер
- в пайплайн добавлен окружение dev, beta, production и динамический
- в пайплайн добавлен stage: review, stage, production

## Как запустить проект:
 - Запустить команду git push gitlab gitlab-ci-1

## Как проверить работоспособность:
 - Перейти по ссылке http://192.168.20.22/homework/example/-/pipelines

## PR checklist
 - [X] Выставил label с номером домашнего задания
 - [X] Выставил label с темой домашнего задания

# Выполнено ДЗ № 15 Практика работы с основными типами Docker сетей. Декларативное описание Docker инфраструктуры при помощи Docker Compose.

 - [X] Основное ДЗ
 - [ ] Задание со *

## В процессе сделано:
 - сеть Docker none, host && bridge
 - docker-compose и параметры через .env
 - базовое имя проекта образуется из названия папки где запускается docker-compose, поменять моно добавив COMPOSE_PROJECT_NAME в переменную .env

## Как запустить проект:
 - запустить команду "docker-compose ps" в директории src

## Как проверить работоспособность:
 - перейти по ссылке http://localhost:9292

## PR checklist
 - [X] Выставил label с номером домашнего задания
 - [X] Выставил label с темой домашнего задания

# Выполнено ДЗ № 14 Разбиение приложения на несколько микросервисов. Выбор базового образа. Подключение volume к контейнеру.

 - [X] Основное ДЗ
 - [ ] Задание со *

## В процессе сделано:
 - собран Docker-образы для сервисного приложения
 - оптимизирован Docker-образ

## Как запустить проект:
 - docker kill $(docker ps -q)
 - docker run -d --network=reddit --network-alias=post_db --network-alias=comment_db -v reddit_db:/data/db mongo:latest
 - docker run -d --network=reddit --network-alias=post turkin/post:1.0
 - docker run -d --network=reddit --network-alias=comment turkin/comment:1.0
 - docker run -d --network=reddit -p 9292:9292 turkin/ui:2.0

## Как проверить работоспособность:
 - Перейти по ссылке http://localhost:929

## PR checklist
 - [X] Выставил label с номером домашнего задания
 - [X] Выставил label с темой домашнего задания


# Выполнено ДЗ № 13 Запуск VM с установленным Docker Engine при помощи Docker Machine. Написание Dockerfile и сборка образа с тестовым приложением. Сохранение образа на DockerHub.

 - [X] Основное ДЗ
 - [ ] Задание со *

## В процессе сделано:
 - написал Dockerfile 
 - собрал образа с тестовым приложением
 - сохранил образ на DockerHub

## Как запустить проект:
 - запустить команду "docker run --name reddit -d -p 9292:9292 turkin/otus-reddit:1.0"

## Как проверить работоспособность:
 - перейти по ссылке http://<your-ip>:9292

## PR checklist
 - [X] Выставил label с номером домашнего задания
 - [X] Выставил label с темой домашнего задания


# Выполнено ДЗ № 12 Установка Docker, запуск контейнера на локальной машине, выполнение команд внутри контейнера, создание образа контейнера на основе запущенного.

 - [X] Основное ДЗ
 - [ ] Задание со *

## В процессе сделано:
 - установил docker
 - запуск контейнера на локальной машине
 - выполнение команд внутри контейнера
 - создание образа контейнера

## Как запустить проект:
 - запустить команду "docker run -it ubuntu:18.04 /bin/bash"

## Как проверить работоспособность:
 - запустить команду "docker ps -a"

## PR checklist
 - [X] Выставил label с номером домашнего задания
 - [X] Выставил label с темой домашнего задания
