# О проекте
Этот проект явлется реализацией тестового задания на backend позицию в AFO.

Проект представлят из себя простенький интерфейс для CRUD операций над системой из моделей Пользователя и Банковских реквизитов (one-to-many).

Стек: Flask+, SQLAlchemy, PostgreSQL, Alembic, Docker & docker-compose

# Содержание
1. [Установка и запуск](#установка-и-запуск)
2. [Глобальные переменные](#глобальные-переменные)

# Установка и запуск
Проект писался с использованием Python 3.12.3 и тестировался под Arch Linux (6.9.1-arch1-1).

1. Скопируйте репозиторий с помощью `git clone https://github.com/makashinmi/ss-test.git`
2. Перейдите в директорию свежескачанного репозитория: `cd ss-test`
3. Убедитесь, что у вас установлены Docker и docker-compose: `echo " $(docker --version) | $(docker-comopose --version)"`
4. Соберите проект, используя `docker-compose build`\* 
5. Запустите проект командой `docker-compose up`\*

\* Возможно, понадобятся права суперпользователя: `sudo docker-compose build`

# Глобальные переменные
- **SECRET_KEY** -- Ключ, необходимый для защиты Flask сессий на клиентской стороне

- **DB_USER** и **DB_PASSWORD** -- Данные для авторизации в базу данных
- **DB_DOMAIN** и **DB_PORT** -- Адрес и порт, на которых обслуживается база данных
- **DB_NAME** -- Название базы данных

- **SQLALCHEMY_DATABASE_URI** -- Переменная, указывающая SQLAlchemy на точку назначения обслуживания базы данных. Составляется из переменных `DB\_...`
