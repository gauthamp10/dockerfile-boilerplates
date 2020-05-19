FROM alpine:latest

RUN apk update && \
    apk fetch openjdk8 && \
    apk add --no-cache openjdk8 && \
    mkdir app;

ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
ENV PATH="$JAVA_HOME/bin:${PATH}"

COPY app/app.java /app
WORKDIR /app
RUN javac app.java
CMD ["java", "app"]
