# ZapahUspeha

Команда "Запас успеха" представляет andriod-приложение и свой API для чата.  

## API

В папке backend лежит RESTfull API на языке Java (Spring Framework), с использованием базы данных PostgreSQL и Docker.

### Spring Framework

Сервер реализует запросы, указанные в ТЗ, и дополняет их, а также реализует другие запросы, такие как: регистрация пользователя, выход из аккаунта, создание новых диалогов. 
API хранит файлы, отправляемые в сообщении и предоставляет ссылку на них для загрузки. Также, сервер полностью синхронизирован и обрабатывает большинство ошибок.

### PostgreSQL

База данных содержит всего 3 таблицы: Пользователь(User), Сообщение(Message) и Диалог(Dialog). Первая хранит все характеристики пользователя, нужные для поиска нужного диалога и создания токена. Message хранит информацию о сообщении, а также ссылку на файл. Dialog хранит все чаты приложения, а также даёт возможность найти чаты определённого пользователя и сообщения чата с каким-либо пользователем

## Android-приложение

Приложение написано с использованием Android Studio на языке Kotlin, а также использует уникальный дизайн.

### WebSockets

Для чаттинга активно используются сокеты, синхронизирующие сообщения в чате для двух сторон
