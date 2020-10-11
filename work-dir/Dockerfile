ARG GO_VERSION=1.13

FROM golang:${GO_VERSION}

RUN GOPATH=/dlv go get -u github.com/go-delve/delve/cmd/dlv

WORKDIR /development

ENV PATH=$PATH:/dlv/bin
