FROM alpine:latest
RUN  apk add --no-cache elixir &&  mkdir /src
COPY src/main.exs /src
WORKDIR /src
CMD ["elixir","./main.exs"]