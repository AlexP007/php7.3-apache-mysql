FROM php:7.3-apache

MAINTAINER AlexP007

# Php extensions.
RUN apt-get update && apt-get install -y \
    git zip unzip pkg-config libpq-dev libxml2-dev libxslt1-dev libzip-dev libpng-dev libonig-dev libfreetype6-dev libjpeg62-turbo-dev libxml2-dev \
    && docker-php-ext-install -j$(nproc) pdo_mysql mysqli gd zip exif soap mbstring pcntl sockets xsl\
    && apt-get clean && apt-get autoclean

# Configuration.
ADD ./php.ini /usr/local/etc/php/conf.d/php.ini

RUN apachectl start

WORKDIR /var/www/html

EXPOSE 80