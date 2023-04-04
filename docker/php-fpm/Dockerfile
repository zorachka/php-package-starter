FROM php:8.1-fpm-alpine

RUN mv $PHP_INI_DIR/php.ini-development $PHP_INI_DIR/php.ini

RUN apk add gcc make autoconf libc-dev \
	&& pecl install apcu \
	&& docker-php-ext-enable apcu

WORKDIR /app
