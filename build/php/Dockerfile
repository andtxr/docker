FROM php:7.2.2-fpm
RUN apt-get update && apt-get install -y \
    libxml2-dev \
    libmcrypt-dev \
    && pecl install xdebug-2.6.0 \
    && pecl install mcrypt-1.0.1 \
    && docker-php-ext-enable xdebug mcrypt \
    && docker-php-ext-install pdo pdo_mysql \
    && docker-php-ext-install tokenizer \
    && docker-php-ext-install soap