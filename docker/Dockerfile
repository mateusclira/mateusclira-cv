# tutorial https://www.nanoshots.com.br/2017/01/docker-containerizado-php7-fpm-nginx-e.html

FROM php:7.4-apache

RUN apt-get update
RUN a2enmod rewrite

WORKDIR /var/www/html

COPY myresume .

EXPOSE 80/tcp
CMD ["apache2-foreground"]