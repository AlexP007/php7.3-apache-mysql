FROM php:7.3-apache

MAINTAINER AlexP007

# configuration
ADD ./php.ini /usr/local/etc/php/conf.d/php.ini

RUN apachectl start

WORKDIR /var/www/html

EXPOSE 80