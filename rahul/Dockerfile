FROM php:7.4-fpm
RUN apt update && \
    apt install -y \
    nginx \
    sudo \
    vim \
    curl \
    supervisor

WORKDIR /var/www/html/

COPY rangoli-maker /var/www/html/rangoli-maker
COPY default.conf /etc/nginx/sites-enabled/default
COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf
CMD ["/usr/bin/supervisord"]