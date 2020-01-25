FROM golang:1.13-alpine

RUN apk --update add --virtual build-dependencies gcc g++ make wget && \
    mkdir -p /tmp/src && \
    cd /tmp/src && \
    wget https://github.com/dexidp/dex/archive/v2.21.0.tar.gz && \
    tar -zxvf v2.21.0.tar.gz && \
    cd dex-2.21.0 && \
    make release-binary && \
    apk add --update ca-certificates openssl

ADD config.yaml /config.yaml

CMD ["./bin/dex", "serve", "/config.yaml"]
