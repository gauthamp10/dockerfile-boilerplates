FROM ubuntu:latest
ARG DEBIAN_FRONTEND=noninteractive
ARG VCS_REF
ARG BUILD_DATE

LABEL maintainer="Gautham Prakash <github.com/gauthamp10>"
LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.vcs-url="https://github.com/gauthamp10/dockerfile-boilerplates"
LABEL org.label-schema.vcs-ref=$VCS_REF

RUN  apt-get update &&  \
     export DEBIAN_FRONTEND=noninteractive && \
     ln -fs /usr/share/zoneinfo/America/New_York /etc/localtime && \
     apt-get install -y tzdata && \
     dpkg-reconfigure --frontend noninteractive tzdata && \
     apt-get install -y gcc gobjc gnustep gnustep-devel && \
     apt-get clean && apt-get autoremove && \
     mkdir src;

COPY src/main.m /src
WORKDIR /src

RUN gcc main.m \
    -I `gnustep-config --variable=GNUSTEP_SYSTEM_HEADERS` \
    -L `gnustep-config --variable=GNUSTEP_SYSTEM_LIBRARIES` \
    -lgnustep-base -fconstant-string-class=NSConstantString \
    -D_NATIVE_OBJC_EXCEPTIONS -o main -lobjc;

CMD ["./main"]