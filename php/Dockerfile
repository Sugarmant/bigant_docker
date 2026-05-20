FROM php:7.4-fpm

RUN apt-get update && apt-get install -y \
    git \
    curl \
    unzip \
    libzip-dev \
    libpng-dev \
    libjpeg-dev \
    libfreetype6-dev

RUN docker-php-ext-install pdo pdo_mysql zip

RUN docker-php-ext-configure gd \
    --with-freetype \
    --with-jpeg

RUN docker-php-ext-install gd

RUN pecl install redis \
    && docker-php-ext-enable redis
