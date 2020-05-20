FROM ubuntu:latest
RUN  apt-get update && apt-get install -y wget && \
     apt-get install -y libx11-dev && \
     wget 'https://www2.cs.arizona.edu/icon/ftp/binaries/unix/linux-x64-v951.tgz' && \
     tar xvf linux-x64-v951.tgz && \
     cp -r icon-v951 /opt/ && \
     ln -s /opt/icon-v951/bin/icont /usr/bin/icont && \
     rm -rf linux-x64*.tgz && \
     rm -rf icon-v951 && \
     apt-get clean && \
     mkdir /src;

COPY src/main.icn /src
WORKDIR /src
RUN icont main.icn
CMD ["./main"]