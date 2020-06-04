FROM ubuntu:latest

ARG VCS_REF
ARG BUILD_DATE

RUN apt-get update && \
    apt-get install clang libicu-dev -y && \
    apt-get install -y wget && \
    apt-get install -y libncurses5 && \
    wget 'https://swift.org/builds/swift-5.2.3-release/ubuntu1804/swift-5.2.3-RELEASE/swift-5.2.3-RELEASE-ubuntu18.04.tar.gz' && \
    mkdir ~/swift && tar -xvzf swift-5.2.3-RELEASE-ubuntu18.04.tar.gz -C ~/swift && \
    ln -s ~/swift/swift-5.2.3-RELEASE-ubuntu18.04/usr/bin/swift /usr/local/bin/swift && \
    rm -rf swift-5.2*.deb && \
    apt-get clean && apt-get autoremove;

LABEL maintainer="Gautham Prakash <github.com/gauthamp10>"
LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.vcs-url="https://github.com/gauthamp10/dockerfile-boilerplates"
LABEL org.label-schema.vcs-ref=$VCS_REF

RUN mkdir src
COPY src/main.swift /src
WORKDIR /src
CMD ["swift","./main.swift"]