FROM php:8.3-fpm-alpine

WORKDIR /var/www/html
COPY . .

RUN apk update && \
    apk add --no-cache bash curl icu-dev && \
    docker-php-ext-install -j$(nproc) intl pdo pdo_mysql && \
    rm -rf /var/cache/apk/*
#RUN docker-php-ext-install -j$(nproc) zip xsl gd intl opcache exif mbstring bcmath soap pdo pdo_mysql

# INSTALL COMPOSER
COPY --from=composer/composer:latest-bin /composer /usr/bin/composer


RUN chown -R 1000:1000 /var/www/html
