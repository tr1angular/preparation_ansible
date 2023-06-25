FROM php:8.0-apache
ENV PORT 8080
RUN apt-get update && docker-php-ext-install mysqli pdo pdo_mysql
CMD sed -i "s/80/$PORT/g" /etc/apache2/sites-available/000-default.conf /etc/apache2/ports.conf && docker-php-entrypoint apache2-foreground
