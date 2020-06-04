FROM elixir:1.10.3-alpine

ARG VCS_REF
ARG BUILD_DATE

LABEL maintainer="Gautham Prakash <github.com/gauthamp10>"
LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.vcs-url="https://github.com/gauthamp10/dockerfile-boilerplates"
LABEL org.label-schema.vcs-ref=$VCS_REF

RUN addgroup -S dockergroup && adduser -S dockeruser -G dockergroup
RUN  mkdir /src;

USER dockeruser
COPY src/main.exs /src
WORKDIR /src
ENTRYPOINT [ "elixir" ]
CMD ["./main.exs"]