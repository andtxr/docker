FROM php:7.2-fpm
RUN apt-get update & apt-get install -y \
        libmcrypt-dev \
        libxml2-dev \
    && docker-php-ext-install pdo \
    && docker-php-ext-install pdo_mysql \
    && docker-php-ext-install mbstring \
    && docker-php-ext-install tokenizer \
    && docker-php-ext-install openssl \
    && docker-php-ext-install soap \
    && docker-php-ext-install -j$(nproc) iconv mcrypt \
