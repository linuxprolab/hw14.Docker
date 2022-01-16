# Домашнее задание 14. Docker, docker-compose, dockerfile 
1. Основное задание.
Создайте свой кастомный образ nginx на базе alpine. После запуска nginx должен
отдавать кастомную страницу (достаточно изменить дефолтную страницу nginx)
Определите разницу между контейнером и образом
Вывод опишите в домашнем задании.
Ответьте на вопрос: Можно ли в контейнере собрать ядро?
Собранный образ необходимо запушить в docker hub и дать ссылку на ваш
репозиторий.
2. Задание со зведочкой.
Создайте кастомные образы nginx и php, объедините их в docker-compose.
После запуска nginx должен показывать php info.
Все собранные образы должны быть в docker hub
## Проверка
1. Основное задание
- Склонировать репозиторий:
```
git clone https://github.com/linuxprolab/hw14.git
cd hw14/hw14.1
```
- Выполнить команды:
```
docker build -t linuxprolab/minimalnginx .
docker login docker.io
docker push linuxprolab/minimalnginx
```
- Запустить контейнера из registry:
```
docker run -it -p 8080:80 linuxprolab/minimalnginx
```
- Определите разницу между контейнером и образом.
Можно. Достаточно установить нужные тулзы. Или взять готовый образ.
https://hub.docker.com/r/naftulikay/ubuntu-kernel-build
2. Задание со зведочкой 
- In progress...
