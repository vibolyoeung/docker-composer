# Composer with PHP PostgreSQL driver
#
# VERSION 0.1.0

FROM composer:1.5.2
MAINTAINER Vibol YOEUNG <vibol.yoeung@webridge.asia>
    
RUN echo 'deb http://packages.dotdeb.org jessie all' >> /etc/apt/sources.list && \
    echo 'deb-src http://packages.dotdeb.org jessie all' >> /etc/apt/sources.list && \
    wget https://www.dotdeb.org/dotdeb.gpg && \
    apt-key add dotdeb.gpg && \
    apt-get update -q && \
    apt-get install --no-install-recommends php7.0-pgsql -qy && \
    apt-get clean && rm -rf /tmp/* /var/lib/apt/lists/* /var/tmp/*

RUN cp /etc/php/7.0/mods-available/pdo_pgsql.ini /usr/local/etc/php/conf.d/pdo_pgsql.ini
RUN mkdir -p /usr/local/lib/php/extensions/no-debug-non-zts-20151012/
RUN cp /usr/lib/php/20151012/pdo_pgsql.so /usr/local/lib/php/extensions/no-debug-non-zts-20151012/pdo_pgsql.so
