FROM composer:2.4 AS composer

COPY php/composer.json php/composer.lock* ./

RUN composer install --no-dev --optimize-autoloader --no-scripts

FROM php:8.1-fpm-alpine

COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/local/bin/
RUN install-php-extensions pdo pdo_mysql

COPY php/conf.d/xdebug.ini /usr/local/etc/php/

COPY --from=composer /app/vendor /var/www/html/vendor

COPY app /app


RUN mkdir -p /app/.env
RUN docker-php-ext-install mysqli
COPY .env.example /app/.env/.env

WORKDIR /var/www/html

EXPOSE 9000
