FROM alpine:latest
ARG VCS_REF
ARG BUILD_DATE

RUN apk update && \
    apk fetch openjdk8 && \
    apk add --no-cache openjdk8 && \
    mkdir app;

ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
ENV PATH="$JAVA_HOME/bin:${PATH}"

LABEL maintainer="Gautham Prakash <github.com/gauthamp10>"
LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.vcs-url="https://github.com/gauthamp10/dockerfile-boilerplates"
LABEL org.label-schema.vcs-ref=$VCS_REF

COPY app/app.java /app
WORKDIR /app
RUN javac app.java
CMD ["java", "app"]
