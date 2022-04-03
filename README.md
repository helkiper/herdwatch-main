##Для запуска:
- в `/etc/hosts` добавить строку `127.0.0.1       server`
- Склонировать репозитории `server` и `client` в папку services
- composer install и в `server`, и в `client`
- `docker-compose up -d`
- в контейнере `server` создать БД (`docker exec main_php-server_1 php bin/console doctrine:database:create --if-not-exists`) и накатить миграции (`docker exec main_php-server_1 php bin/console doctrine:migrations:migrate`)
