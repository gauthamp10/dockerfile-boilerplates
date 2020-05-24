FROM erlang:23.0.1-alpine
RUN  mkdir /src
COPY src/main.erl /src
WORKDIR /src
RUN [ "erlc","main.erl"]
CMD ["erl","-noshell","-s","main","start","-s","init","stop"]