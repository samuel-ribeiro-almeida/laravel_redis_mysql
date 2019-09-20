Image Docker:
samuelribeiroalmeida/laravel_redis_mysql:latest

Command to composer install
curl -s https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin  --filename=composer


$ docker exec -it app bash

$ composer install
$ cp .env.example .env
$ php artisan key:generate
$ php artisan config:cache
$ php artisan migrate


#config .env
....
DB_CONNECTION=mysql
DB_HOST=db
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=root

BROADCAST_DRIVER=log
CACHE_DRIVER=file
QUEUE_CONNECTION=sync
SESSION_DRIVER=file
SESSION_LIFETIME=120

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
....
