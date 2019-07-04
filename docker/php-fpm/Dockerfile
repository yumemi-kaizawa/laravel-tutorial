FROM php:7.3-fpm-alpine

RUN apk update && apk --update add tzdata
RUN docker-php-ext-install pdo_mysql mysqli mbstring
RUN mkdir -p /var/log/fpm \
    && ln -fns /dev/stdout /var/log/fpm/access.log \
    && ln -fns /dev/stderr /var/log/fpm/access.log
CMD [ "php-fpm", "-F", "-O" ]
