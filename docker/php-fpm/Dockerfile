FROM php:7.3-fpm-alpine

RUN apk update && apk --update add tzdata
RUN apk update && apk --update add php7-bcmath libxml2-dev
RUN docker-php-ext-install bcmath ctype json mbstring pdo_mysql mysqli tokenizer xml
RUN mkdir -p /var/log/fpm \
    && ln -fns /dev/stdout /var/log/fpm/access.log \
    && ln -fns /dev/stderr /var/log/fpm/access.log
RUN curl -sS https://getcomposer.org/installer | php && mv composer.phar /usr/local/bin/composer
CMD [ "php-fpm", "-F", "-O" ]
