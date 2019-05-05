FROM php:7.1-fpm-alpine

RUN php -i | grep curl && php -m | grep curl
RUN apk update && apk upgrade
RUN apk add --no-cache \
        			libmcrypt-dev \
        			libltdl \
              libxml2-dev \
              libpng-dev \
              libxslt-dev \
              icu-dev
RUN docker-php-ext-install bcmath \
  mcrypt \
  opcache \
  pdo_mysql \
  soap \
  xml \
  zip \
  xsl \
  intl

RUN apk add freetype-dev libjpeg-turbo-dev libpng-dev
RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/
RUN docker-php-ext-install gd
