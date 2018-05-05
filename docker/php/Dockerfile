FROM php:7.2-fpm

WORKDIR /var/www

RUN apt-get update 
RUN apt-get install -y zlib1g-dev zip curl git

RUN pecl install xdebug
RUN docker-php-ext-enable xdebug

RUN docker-php-ext-install zip
RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install mbstring

RUN apt-get autoremove

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin/ --filename=composer && chmod +sx /usr/local/bin/composer