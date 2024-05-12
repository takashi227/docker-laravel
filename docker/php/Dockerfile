FROM php:8.3-fpm

# install composer
ENV COMPOSER_ALLOW_SUPERUSER=1 \ COMPOSER_HOME=/opt/composer
COPY --from=composer:2.7.6 /usr/bin/composer /usr/bin/composer

# apt-get update & install
RUN apt-get update && \
  apt-get -y install --no-install-recommends git unzip libzip-dev libicu-dev libonig-dev && \
  apt-get clean && \
  rm -rf /var/lib/apt/lists/* && \
  docker-php-ext-install intl pdo_mysql zip bcmath

COPY ./php.ini /usr/local/etc/php/php.ini

WORKDIR /var/www/html