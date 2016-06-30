# Composer with PHP PostgreSQL driver
#
# VERSION 0.1.0

FROM composer/composer:1.0.0-beta1
MAINTAINER Thomas Barthelemy <thomasb@webridge.asia>

RUN apt-get update -q && \
    apt-get install --no-install-recommends php5-pgsql -qy && \
    apt-get clean && rm -rf /tmp/* /var/lib/apt/lists/* /var/tmp/*

RUN echo 'extension = /usr/lib/php5/20131226/pdo_pgsql.so' >> /usr/local/etc/php/php.ini