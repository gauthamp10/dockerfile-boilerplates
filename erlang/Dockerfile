FROM erlang:23.0.1-alpine

ARG VCS_REF
ARG BUILD_DATE

# Setting resource quota
ARG MIN_MEM=2G
ARG MAX_MEM=2G

LABEL maintainer="Gautham Prakash <github.com/gauthamp10>"
LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.vcs-url="https://github.com/gauthamp10/dockerfile-boilerplates"
LABEL org.label-schema.vcs-ref=$VCS_REF

RUN addgroup -S dockergroup && adduser -S dockeruser -G dockergroup
RUN  mkdir /src

USER dockeruser
COPY src/main.erl /src
WORKDIR /src
USER root
RUN [ "erlc","main.erl"]
USER dockeruser
CMD ["erl","-noshell","-s","main","start","-s","init","stop"]