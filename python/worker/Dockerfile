FROM python:3.6-slim

ARG VCS_REF
ARG BUILD_DATE

# Setting resource quota
ARG MIN_MEM=2G
ARG MAX_MEM=2G

LABEL maintainer="Gautham Prakash <github.com/gauthamp10>"
LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.vcs-url="https://github.com/gauthamp10/dockerfile-boilerplates"
LABEL org.label-schema.vcs-ref=$VCS_REF

COPY ./src /src
WORKDIR /src
RUN pip install -r requirements.txt
CMD python hello_python.py