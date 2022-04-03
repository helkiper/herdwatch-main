FROM php:7.4.0-fpm

RUN apt-get update && apt-get install -y \
        curl \
        wget \
        git \
    && docker-php-ext-install -j$(nproc) iconv ctype json mysqli pdo_mysql  \
    && curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www

CMD ["php-fpm"]
