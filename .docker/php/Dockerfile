FROM php:7.1.8-apache

RUN apt-get update && \
    apt-get install nodejs && \
    apt-get install npm

MAINTAINER Paul Redmond

COPY . /var/www/html
COPY .docker/php/vhost.conf /etc/apache2/sites-available/000-default.conf

RUN chown -R www-data:www-data /var/www/html \
    && a2enmod rewrite
