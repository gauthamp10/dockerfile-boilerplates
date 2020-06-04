FROM alpine:latest
ARG VCS_REF
ARG BUILD_DATE

# Setting resource quota
ARG MIN_MEM=1G
ARG MAX_MEM=1G

RUN addgroup -S dockergroup && adduser -S dockeruser -G dockergroup
RUN  mkdir /script

LABEL maintainer="Gautham Prakash <github.com/gauthamp10>"
LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.vcs-url="https://github.com/gauthamp10/dockerfile-boilerplates"
LABEL org.label-schema.vcs-ref=$VCS_REF

USER dockeruser

COPY script/main.sh /script
WORKDIR /script
CMD ["sh","./main.sh"]