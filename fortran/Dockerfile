FROM alpine:latest
RUN  apk add --no-cache build-base gfortran &&  mkdir /src
COPY src/main.f90 /src
WORKDIR /src
RUN gfortran main.f90 -o main
CMD ["./main"]