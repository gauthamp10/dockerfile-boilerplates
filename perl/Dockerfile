FROM alpine:latest
RUN  apk add --no-cache perl &&  mkdir /src
COPY src/main.pl /src
WORKDIR /src
CMD ["perl","./main.pl"]