FROM alpine:latest
RUN  apk add  --no-cache nodejs &&  mkdir /app
COPY app/app.js /app
WORKDIR /app
CMD ["node","./app.js"]