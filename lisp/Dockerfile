FROM ubuntu:latest
ARG VCS_REF
ARG BUILD_DATE

LABEL maintainer="Gautham Prakash <github.com/gauthamp10>"
LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.vcs-url="https://github.com/gauthamp10/dockerfile-boilerplates"
LABEL org.label-schema.vcs-ref=$VCS_REF

RUN  apt-get update && \ 
     apt-get install -y clisp && \
     apt-get clean && \
     mkdir /src;
     
COPY src/main.lsp /src
WORKDIR /src
CMD ["clisp","./main.lsp"]