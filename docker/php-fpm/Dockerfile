FROM php:5.6-fpm

RUN useradd -ms /bin/bash vagrant
RUN docker-php-ext-install pdo pdo_mysql
RUN pecl install xdebug-2.5.0 && docker-php-ext-enable xdebug
RUN echo "zend_extension=$(find /usr/local/lib/php/extensions/ -name xdebug.so)" > /usr/local/etc/php/conf.d/xdebug.ini \
        && echo "xdebug.remote_enable=on" >> /usr/local/etc/php/conf.d/xdebug.ini \
        && echo "xdebug.remote_autostart=off" >> /usr/local/etc/php/conf.d/xdebug.ini

USER vagrant

WORKDIR /app

COPY php-fpm.conf /etc/php-fpm.conf