FROM php:8-fpm-alpine

RUN docker-php-ext-install mysqli pdo pdo_mysql
COPY --from=composer:latest /usr/bin/composer /usr/local/bin/composer

RUN docker-php-ext-enable mysqli

CMD [ "php-fpm" ]