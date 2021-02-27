FROM phpdockerio/php72-fpm:latest
WORKDIR "/var/www/html/poliscan/web"

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

# Install selected extensions and other stuff
RUN apt-get update \
    && apt-get -y --no-install-recommends install  php7.2-pgsql php7.2-bcmath php7.2-gd php-imagick php7.2-intl php7.2-tidy php7.2-xmlrpc php7.2-xsl php7.2-mcrypt \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

# Install git
RUN apt-get update \
    && apt-get -y install git \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*
