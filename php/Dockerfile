FROM php:7.4-apache
COPY app/ /var/www/html
EXPOSE 80
CMD (! pidof php) || sudo kill -9 $(pidof php)

