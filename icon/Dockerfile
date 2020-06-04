FROM ubuntu:latest

ARG VCS_REF
ARG BUILD_DATE

# Setting resource quota
ARG MIN_MEM=2G
ARG MAX_MEM=2G

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

LABEL maintainer="Gautham Prakash <github.com/gauthamp10>"
LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.vcs-url="https://github.com/gauthamp10/dockerfile-boilerplates"
LABEL org.label-schema.vcs-ref=$VCS_REF

COPY src/main.icn /src
WORKDIR /src
RUN icont main.icn
CMD ["./main"]