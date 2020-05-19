FROM alpine:latest
RUN  apk add --no-cache erlang &&  mkdir /src
COPY src/main.erl /src
WORKDIR /src
RUN erlc main.erl
CMD ["erl","-noshell","-s","main","start","-s","init","stop"]