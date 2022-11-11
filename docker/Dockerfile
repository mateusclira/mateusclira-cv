FROM alpine

RUN apk update

RUN apk add nginx

COPY myresume /usr/share/nginx/html

COPY default.conf /etc/nginx/conf.d/default.conf

WORKDIR /usr/share/nginx/html

EXPOSE 80/tcp

CMD ["-g" ,"daemon off;"]