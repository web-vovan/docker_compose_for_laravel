FROM php:8-fpm-alpine

RUN apk add \
    bash \
    curl \
    zip \
    unzip \
    libzip-dev \
    libpng-dev \
    jpeg-dev \
    freetype-dev \
    zlib-dev \
    git \
    ffmpeg \
    mysql-client
    
RUN docker-php-ext-install pdo pdo_mysql zip pcntl gd exif

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www