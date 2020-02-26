FROM php:7.4.3-apache

RUN apt-get update; \
    apt-get upgrade; \
    apt-get -y install libzip-dev unzip;

RUN docker-php-ext-install zip;

WORKDIR /usr/local/lib

RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
RUN php composer-setup.php
RUN php -r "unlink('composer-setup.php');"

WORKDIR /usr/local/bin

RUN echo 'php /usr/local/lib/composer.phar $@' > composer
RUN chmod 755 composer

RUN composer global require "laravel/lumen-installer"

WORKDIR /var/www/html

# RUN /root/.composer/vendor/bin/lumen new site
