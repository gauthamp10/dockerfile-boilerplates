FROM alpine:latest

ARG VCS_REF
ARG BUILD_DATE

RUN  apk add --no-cache build-base &&  mkdir /src

LABEL maintainer="Gautham Prakash <github.com/gauthamp10>"
LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.vcs-url="https://github.com/gauthamp10/dockerfile-boilerplates"
LABEL org.label-schema.vcs-ref=$VCS_REF

COPY src/main.c /src
WORKDIR /src
RUN gcc -o main main.c
CMD ["./main"]