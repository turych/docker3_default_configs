FROM php:7.1-fpm
RUN apt-get update
RUN apt-get install -y libfreetype6-dev libjpeg-dev libpng-dev libgif-dev
RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/
RUN docker-php-ext-install mbstring exif gd pdo pdo_mysql mysqli