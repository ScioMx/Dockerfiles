# Based on PHP FPM Docker container

FROM php:fpm

MAINTAINER docker@sciodev.com

RUN apt-get update && apt-get install -y git libssl-dev wget

RUN   docker-php-ext-install zip \
	 && docker-php-ext-install mbstring


# Composer

ENV COMPOSER_VERSION 1.0.0-alpha10
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer --version=${COMPOSER_VERSION}


# Deployer

RUN wget http://deployer.org/deployer.phar
RUN mv deployer.phar /usr/local/bin/dep
RUN chmod +x /usr/local/bin/dep
