FROM php:7.2-fpm AS base

RUN set -eux; \
    pecl install redis-5.3.4 \
    && docker-php-ext-enable redis; \
    docker-php-ext-install pdo pdo_mysql pdo_pgsql; \
    mkdir -p /app

WORKDIR /app

EXPOSE 9000
ENTRYPOINT ["php-fpm"]
