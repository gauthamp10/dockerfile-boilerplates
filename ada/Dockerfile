FROM ubuntu:latest
RUN  apt-get update && apt-get install -y gcc gnat && \  
     mkdir /src

COPY src/main.ads /src
WORKDIR /src
RUN gnatmake -o main main.ads
CMD ["./main"]