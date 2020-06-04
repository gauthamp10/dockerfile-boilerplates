FROM alpine:latest

ARG VCS_REF
ARG BUILD_DATE

# Sensible Defaults for Memory Consumption
ARG MIN_MEM=2G
ARG MAX_MEM=2G

# This env var will force the JVM to terminate if more memory is allocated than specified here
ENV _JAVA_OPTIONS="-Xms${MIN_MEM} -Xmx${MAX_MEM}"

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

WORKDIR /app

# Since USER only affects RUN, CMD and ENTRYPOINT 
# And not WORKDIR, we have to modify ownership of the workdir
RUN chown nobody. /app

# Copy as Nobody
COPY --chown=nobody app/app.java /app
USER nobody

RUN javac app.java
CMD ["java", "app"]
