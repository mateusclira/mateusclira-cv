# gerar a imagem utilizando php + apache, devido a ser uma imagem unica
# caso for usar o nginx ele somente serve para exibir arquivos html, caso for precisar do php
# vc devera ciar um outro container do php-fm e víncular com o nginx
# tutorial https://www.nanoshots.com.br/2017/01/docker-containerizado-php7-fpm-nginx-e.html

FROM php:7.4-apache

RUN apt-get update
RUN a2enmod rewrite

WORKDIR /var/www/html

# copia para pastas onde o workdir está apontando
COPY myresume .

# sobrescrever o arquivo de configuração
COPY conf /etc/apache2/sites-enabled/

EXPOSE 80/tcp
CMD ["apache2-foreground"]