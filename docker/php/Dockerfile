FROM php:7.0-apache

#composer install
WORKDIR /usr/bin
RUN curl -s http://getcomposer.org/installer | php && ln -s /usr/bin/composer.phar /usr/bin/composer
RUN apt-get update \
    && apt-get install -y \
    git \
    zip \
    unzip \
    vim

RUN apt-get update \
    && apt-get install -y libpq-dev \
    && docker-php-ext-install pdo_mysql pdo_pgsql

#apache setting
COPY ./default.conf /etc/apache2/sites-available/000-default.conf

WORKDIR /etc/apache2/mods-enabled
RUN ln -s ../mods-available/rewrite.load

WORKDIR /var/www/html