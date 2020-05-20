# Javascript/Static HTML Boilerplate Docker

Build and run Javascript/Static HTML via docker.

```
 docker build -t js-build .

 docker run -p 5001:80 --rm -v /path/to/valoume/:/usr/share/nginx/html js-build

```
