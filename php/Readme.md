# PHP Boilerplate Docker

Build and run PHP web app via docker

```
docker build -t php .

docker run -p 5001:80 --rm -v /path/to/volume/ :/var/www/html/ php
```
