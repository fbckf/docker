FROM php:7.4-fpm

# 镜像信息
LABEL Author="ckf"
LABEL Version="2020.1.26"
LABEL Description="PHP 7.4."

RUN sed -i "s@http://deb.debian.org@http://mirrors.aliyun.com@g" /etc/apt/sources.list && rm -Rf /var/lib/apt/lists/* &&  cat /etc/apt/sources.list

RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libpng-dev \
        libzip-dev \
        libicu-dev \
        libxml2-dev \
    && docker-php-ext-configure gd \
    && docker-php-ext-install -j$(nproc) gd \
        && docker-php-ext-install zip \
        && docker-php-ext-install pdo_mysql \
        && docker-php-ext-install opcache \
        && docker-php-ext-install mysqli \
        && docker-php-ext-install -j$(nproc) intl \
        && docker-php-ext-install -j$(nproc) soap \
        && docker-php-ext-install xmlrpc