FROM alpine
LABEL version="1.0.0" description="Disponibilizando site com NGINX" maintainer="Mateus Lira - mateus@mateusclira.tech"

RUN apk update

RUN apk add nginx

COPY myresume /usr/share/nginx/html
COPY nginx/default.conf /etc/nginx/conf.d/default.conf

EXPOSE 80/tcp

WORKDIR /usr/share/nginx/html

ENTRYPOINT ["/usr/sbin/nginx"]

CMD ["-g" ,"daemon off;"]