FROM alpine:latest
RUN  apk add --no-cache rust &&  mkdir /src
COPY src/main.rs /src
WORKDIR /src
RUN rustc main.rs
CMD ["./main"]