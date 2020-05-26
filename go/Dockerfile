FROM alpine:latest
ARG VCS_REF
ARG BUILD_DATE

LABEL maintainer="Gautham Prakash <github.com/gauthamp10>"
LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.vcs-url="https://github.com/gauthamp10/dockerfile-boilerplates"
LABEL org.label-schema.vcs-ref=$VCS_REF

RUN  apk add --no-cache binutils gcc musl musl-dev go &&  mkdir /src
COPY src/main.go /src
WORKDIR /src
CMD ["go","run","./main.go"]