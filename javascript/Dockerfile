FROM nginx:alpine
COPY /script /usr/share/nginx/html/
CMD (! pidof nginx) || sudo kill -9 $(pidof nginx)