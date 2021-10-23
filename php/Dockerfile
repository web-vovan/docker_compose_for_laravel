FROM php:fpm

RUN ln -snf /usr/share/zoneinfo/Europe/Moscow /etc/localtime && echo Europe/Moscow > /etc/timezone

RUN apt-get update && apt-get install -y \
    curl \
    wget \
    git \
    mc \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    libmcrypt-dev \
    libpng-dev \
    libxrender1 \
    libfontconfig \
    libzip-dev
    
RUN docker-php-ext-install pdo pdo_mysql zip pcntl gd exif

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www

CMD ["php-fpm", "-R"]