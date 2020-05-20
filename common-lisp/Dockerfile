FROM ubuntu:latest

RUN  apt-get update && \ 
     apt-get install -y clisp && \
     apt-get clean && \
     mkdir /src;
     
COPY src/main.lisp /src
WORKDIR /src
CMD ["clisp","./main.lisp"]