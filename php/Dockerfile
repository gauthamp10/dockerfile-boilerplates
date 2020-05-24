FROM php:7.4-apache
RUN apt-get update && apt-get install -y wget && \
    wget 'https://phar.phpunit.de/phpunit-6.5.phar' && \
    chmod +x phpunit-6.5.phar && \
    mv phpunit-6.5.phar /usr/local/bin/phpunit && \
    phpunit --version && rm -rf pharun*.phar;
RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" && \
    php -r "if (hash_file('sha384', 'composer-setup.php') === 'e0012edf3e80b6978849f5eff0d4b4e4c79ff1609dd1e613307e16318854d24ae64f26d17af3ef0bf7cfb710ca74755a') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;" && \
    php composer-setup.php && \
    php -r "unlink('composer-setup.php');"

RUN bash composer require phpunit/phpunit --dev

COPY app/ /var/www/html
EXPOSE 80
