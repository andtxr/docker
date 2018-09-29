FROM php:7.2.10-fpm

RUN pecl install xdebug-2.6.0 \
    && docker-php-ext-enable xdebug;

RUN apt-get update && apt-get install -y \
    git \
    && docker-php-ext-install pdo pdo_mysql \
    && docker-php-ext-install tokenizer \
    && docker-php-ext-install soap \
    && docker-php-ext-install mbstring \
    && docker-php-ext-install openssl \
    && docker-php-ext-install xml \
    && docker-php-ext-install ctype \
    && docker-php-ext-install curl \
    && docker-php-ext-install json \
    && docker-php-ext-enable pdo pdo_mysql tokenizer soap mbstring openssl xml ctype curl json;