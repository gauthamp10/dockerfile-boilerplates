FROM alpine:latest
RUN  apk add --no-cache build-base &&  mkdir /src
COPY src/main.c /src
WORKDIR /src
RUN gcc -o main main.c
CMD ["./main"]