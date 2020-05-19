FROM alpine:latest
RUN  apk add --no-cache build-base &&  mkdir /src
COPY src/main.cpp /src
WORKDIR /src
RUN g++ -o main main.cpp
CMD ["./main"]