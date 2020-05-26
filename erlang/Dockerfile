FROM erlang:23.0.1-alpine
ARG VCS_REF
ARG BUILD_DATE

LABEL maintainer="Gautham Prakash <github.com/gauthamp10>"
LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.vcs-url="https://github.com/gauthamp10/dockerfile-boilerplates"
LABEL org.label-schema.vcs-ref=$VCS_REF

RUN  mkdir /src
COPY src/main.erl /src
WORKDIR /src
RUN [ "erlc","main.erl"]
CMD ["erl","-noshell","-s","main","start","-s","init","stop"]