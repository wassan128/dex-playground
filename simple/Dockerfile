FROM golang:1.13-alpine

RUN apk --update add wget && \
    mkdir -p /tmp/src && \
    cd /tmp/src && \
    wget https://github.com/dexidp/dex/archive/v2.21.0.tar.gz && \
    tar -zxvf v2.21.0.tar.gz && \
    cd dex-2.21.0 && \
    make release-binary

