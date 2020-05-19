FROM alpine:latest
RUN  apk add --no-cache build-base perl ncurses-libs ghc &&  mkdir /src
COPY src/main.hs /src
WORKDIR /src
RUN ghc -o main main.hs
CMD ["./main"]