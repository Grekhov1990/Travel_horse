# Проект TravelHorse
Этот проект использует Django веб-приложение и сервис SQLite для хранения данных. Инфраструктура проекта определяется файлом docker-compose.yml.

# Структура проекта
- `app:` этот сервис представляет Django приложение, собранное из файла `Dockerfile`. Порт 8000 на локальной машине перенаправляется
на порт 8000 внутри контейнера.
- `db:` этот сервис представляет сервер SQLite, собранный из файла `Dockerfile`. Данные хранятся в томе, который связан с томом внутри 
контейнера с сервером `SQLite`.

# Запуск проекта
Чтобы запустить проект, нужно выполнить следующие команды:

1. Убедитесь, что `Docker` и `Docker Compose` установлены на вашей системе.
2. Скачайте файлы проекта на локальную машину с помощью `git clone https://github.com/Grekhov1990/Travel_Horse.git`.
3. Откройте терминал и перейдите в директорию с файлами проекта.
4. Выполните команду `docker-compose build`, чтобы собрать образы Docker.
5. Выполните команду `docker-compose up`, чтобы запустить проект.
6. Откройте браузер и перейдите по адресу http://localhost:8000, чтобы проверить работу приложения.
7. При необходимости можно остановить проект, выполнив команду `docker-compose down`.