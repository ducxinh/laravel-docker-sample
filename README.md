# Kozocom Laravel Template

## Versions
PHP: 8.2
NodeJS: >=18.0


## Clone source code
```bash
git clone ...
```

## Installing
```bash
cd kz-laravel-template/docker
cp .env.example .env

sudo docker compose up -d workspace nginx php-fpm mysql phpmyadmin
```

## Setup Laravel
```bash
sudo docker compose exec workspace bash

composer install
chmod -R 777 storage
cp .env.example .env
php artisan key:generate
php artisan migrate
php artisan db:seed
```

## Demo
Open browser and navigate to `http://localhost:80`
