FROM alpine:latest
ARG VCS_REF
ARG BUILD_DATE

LABEL maintainer="Gautham Prakash <github.com/gauthamp10>"
LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.vcs-url="https://github.com/gauthamp10/dockerfile-boilerplates"
LABEL org.label-schema.vcs-ref=$VCS_REF

RUN  apk add --no-cache build-base &&  mkdir /src
COPY src/main.cpp /src
WORKDIR /src
RUN g++ -o main main.cpp
CMD ["./main"]