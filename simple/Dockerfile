FROM golang:latest

RUN go get github.com/dexidp/dex && \
    cd $GOPATH/src/github.com/dexidp/dex && \
    make
