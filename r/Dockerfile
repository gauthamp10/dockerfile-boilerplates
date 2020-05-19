FROM alpine:latest
RUN  apk add --no-cache R &&  mkdir /src
COPY src/script.R /src
WORKDIR /src
CMD ["Rscript","./script.R"]