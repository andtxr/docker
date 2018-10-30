FROM php:7.2.10-fpm

RUN apt-get update && apt-get install -y \
    git \
    libxml2-dev \
    libcurl4-openssl-dev \
    zlib1g-dev \
    && pecl install xdebug-2.6.0 \
    && docker-php-ext-install zip \
    && docker-php-ext-install pdo pdo_mysql \
    && docker-php-ext-install tokenizer \
    && docker-php-ext-install soap \
    && docker-php-ext-install mbstring \
    && docker-php-ext-install xml \
    && docker-php-ext-install ctype \
    && docker-php-ext-install curl \
    && docker-php-ext-install json \
    && docker-php-ext-enable xdebug zip pdo pdo_mysql tokenizer soap mbstring xml ctype curl json;

RUN cd ~ \
    && curl -sS https://getcomposer.org/installer -o composer-setup.php \
    && php composer-setup.php --install-dir=/usr/local/bin --filename=composer;

RUN curl -sL https://deb.nodesource.com/setup_8.x | bash - \
    && apt install nodejs;
