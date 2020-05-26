FROM alpine:latest
ARG VCS_REF
ARG BUILD_DATE

LABEL maintainer="Gautham Prakash <github.com/gauthamp10>"
LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.vcs-url="https://github.com/gauthamp10/dockerfile-boilerplates"
LABEL org.label-schema.vcs-ref=$VCS_REF

RUN  apk add --no-cache build-base perl ncurses-libs ghc &&  mkdir /src
COPY src/main.hs /src
WORKDIR /src
RUN ghc -o main main.hs
CMD ["./main"]