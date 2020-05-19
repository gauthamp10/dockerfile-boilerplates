FROM alpine:latest
RUN  apk add --no-cache binutils gcc musl musl-dev go &&  mkdir /src
COPY src/main.go /src
WORKDIR /src
CMD ["go","run","./main.go"]