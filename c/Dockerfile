FROM alpine:latest

ARG VCS_REF
ARG BUILD_DATE

# Setting resource quota
ARG MIN_MEM=2G
ARG MAX_MEM=2G

RUN addgroup -S dockergroup && adduser -S dockeruser -G dockergroup
RUN  apk add --no-cache build-base &&  mkdir /src

LABEL maintainer="Gautham Prakash <github.com/gauthamp10>"
LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.vcs-url="https://github.com/gauthamp10/dockerfile-boilerplates"
LABEL org.label-schema.vcs-ref=$VCS_REF

USER dockeruser
COPY src/main.c /src
WORKDIR /src
USER root
RUN gcc -o main main.c
CMD ["./main"]