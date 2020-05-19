FROM alpine:latest
RUN  apk add --no-cache lua-dev &&  mkdir /src
COPY src/main.lua /src
WORKDIR /src
CMD ["lua","./main.lua"]