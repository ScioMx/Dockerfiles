FROM scio/webdev-php7.0-fpm

MAINTAINER docker@sciodev.com

RUN  pecl install mongodb \
	&& pecl install xdebug-beta \
	&& docker-php-ext-enable xdebug

RUN echo "extension=mongodb.so" > $PHP_INI_DIR/conf.d/mongodb.ini
