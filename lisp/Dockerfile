FROM ubuntu:latest
#Build args
ARG VCS_REF
ARG BUILD_DATE
# Setting resource quota
ARG MIN_MEM=2G
ARG MAX_MEM=2G

RUN  apt-get update && \ 
     apt-get install -y clisp && \
     apt-get clean && \
     mkdir /src;
#Adding Labels of build
LABEL maintainer="Gautham Prakash <github.com/gauthamp10>"
LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.vcs-url="https://github.com/gauthamp10/dockerfile-boilerplates"
LABEL org.label-schema.vcs-ref=$VCS_REF

COPY src/main.lsp /src
WORKDIR /src
#Execution
CMD ["clisp","./main.lsp"]