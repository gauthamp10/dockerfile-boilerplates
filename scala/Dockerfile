FROM ubuntu

ARG VCS_REF
ARG BUILD_DATE

RUN apt-get update && \
    apt-get install -y curl && \
    apt-get install -y gnupg2 && \
    apt-get clean;

RUN apt-get update && \
    apt-get install -y openjdk-8-jdk && \
    apt-get install -y ant && \
    apt-get clean;

RUN apt-get update && \
    apt-get install ca-certificates-java && \
    apt-get clean && \
    update-ca-certificates -f;


ENV JAVA_HOME /usr/lib/jvm/java-8-openjdk-amd64/
RUN export JAVA_HOME

RUN apt-get install wget && \
    wget www.scala-lang.org/files/archive/scala-2.13.2.deb && \
    dpkg -i scala*.deb && \
    rm -rf scala*.deb && \
    apt-get clean && \
    apt-get autoremove && \
    mkdir app;
    
LABEL maintainer="Gautham Prakash <github.com/gauthamp10>"
LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.vcs-url="https://github.com/gauthamp10/dockerfile-boilerplates"
LABEL org.label-schema.vcs-ref=$VCS_REF

COPY app/app.scala /app
WORKDIR /app
RUN scalac app.scala
CMD ["scala","./app.scala"]
