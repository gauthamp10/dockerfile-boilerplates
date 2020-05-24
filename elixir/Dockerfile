FROM elixir:1.10.3-alpine

RUN  mkdir /src;

COPY src/main.exs /src
WORKDIR /src
ENTRYPOINT [ "elixir" ]
CMD ["./main.exs"]