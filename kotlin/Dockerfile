FROM alpine:latest
ARG VCS_REF
ARG BUILD_DATE

LABEL maintainer="Gautham Prakash <github.com/gauthamp10>"
LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.vcs-url="https://github.com/gauthamp10/dockerfile-boilerplates"
LABEL org.label-schema.vcs-ref=$VCS_REF

RUN apk add --update bash && \
    apk fetch openjdk8 && \
    apk add --no-cache openjdk8;

RUN apk add --no-cache build-base wget && \
    cd /usr/lib && \
    wget 'https://github.com/JetBrains/kotlin/releases/download/v1.3.72/kotlin-compiler-1.3.72.zip' && \
    unzip kotlin-compiler-*.zip && \
    rm kotlin-compiler-*.zip && \
    rm -f kotlinc/bin/*.bat;

ENV PATH $PATH:/usr/lib/kotlinc/bin

RUN mkdir app
COPY app/app.kt /app
WORKDIR /app
RUN kotlinc app.kt -include-runtime -d app.jar
CMD ["java","-jar","./app.jar"]
