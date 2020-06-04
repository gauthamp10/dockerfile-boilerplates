FROM ubuntu:latest
ARG VCS_REF
ARG BUILD_DATE

# Setting resource quota
ARG MIN_MEM=2G
ARG MAX_MEM=2G

RUN  apt-get update &&  \
     apt-get install -y wget && \ 
     wget 'https://julialang-s3.julialang.org/bin/linux/x64/1.4/julia-1.4.1-linux-x86_64.tar.gz' && \   
     tar -xvzf julia-1.4.1-linux-x86_64.tar.gz && \
     cp -r julia-1.4.1 /opt/ && \
     ln -s /opt/julia-1.4.1/bin/julia /usr/local/bin/julia && \
     rm -rf julia-1.4.1*.tar.gz && \
     rm -rf julia-1.4.1 && \
     apt-get clean && \
     apt-get autoremove && \
     mkdir /src;

LABEL maintainer="Gautham Prakash <github.com/gauthamp10>"
LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.vcs-url="https://github.com/gauthamp10/dockerfile-boilerplates"
LABEL org.label-schema.vcs-ref=$VCS_REF

COPY src/main.jl /src
WORKDIR /src
CMD ["julia","./main.jl"]