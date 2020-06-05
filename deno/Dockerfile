FROM alpine:latest
#Enironment variables
ENV DENO_VERSION=1.0.5
ENV LANG=C.UTF-8
#Build args
ARG VCS_REF
ARG BUILD_DATE
# Setting resource quota
ARG MIN_MEM=2G
ARG MAX_MEM=2G
#Adding Labels of build
LABEL maintainer="Gautham Prakash <github.com/gauthamp10>"
LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.vcs-url="https://github.com/gauthamp10/dockerfile-boilerplates"
LABEL org.label-schema.vcs-ref=$VCS_REF


# Here we install GNU libc (aka glibc) and set C.UTF-8 locale as default and Installing Deno.

RUN apk --no-cache add ca-certificates wget\
    && wget -q -O /etc/apk/keys/sgerrand.rsa.pub https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub\
    && wget https://github.com/sgerrand/alpine-pkg-glibc/releases/download/2.31-r0/glibc-2.31-r0.apk\
    && apk add glibc-2.31-r0.apk \
    && wget https://github.com/sgerrand/alpine-pkg-glibc/releases/download/2.31-r0/glibc-bin-2.31-r0.apk\
    && wget https://github.com/sgerrand/alpine-pkg-glibc/releases/download/2.31-r0/glibc-i18n-2.31-r0.apk\
    && apk add glibc-bin-2.31-r0.apk glibc-i18n-2.31-r0.apk\
    && wget -q -O deno.zip https://github.com/denoland/deno/releases/download/v${DENO_VERSION}/deno-x86_64-unknown-linux-gnu.zip \
    && unzip deno.zip \
    && rm deno.zip \
    && chmod 777 deno \
    && mv deno /bin/deno \
    && rm "/etc/apk/keys/sgerrand.rsa.pub" \
    && /usr/glibc-compat/bin/localedef --force --inputfile POSIX --charmap UTF-8 "$LANG" || true \
    && echo "export LANG=$LANG" > /etc/profile.d/locale.sh  \
    && apk del glibc-i18n \
    && rm -rf /var/cache/apk/*\
    && rm "/root/.wget-hsts" 


RUN addgroup -g 1993 -S dockeruser \
    && adduser -u 1993 -S dockeruser -G dockeruser \
    && mkdir /src/ \
    && chown dockeruser:dockeruser /src/

ENV DENO_DIR /src/

COPY src/main.ts /src/

ENTRYPOINT ["deno"]
CMD ["run", "./src/main.ts"]