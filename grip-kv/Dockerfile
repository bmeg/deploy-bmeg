FROM golang:1.12.7-alpine

RUN apk add make git bash build-base

# install grip
RUN mkdir -p /go/src/github.com/bmeg
WORKDIR /go/src/github.com/bmeg
ENV GOPATH=/go
ENV PATH="/go/bin:${PATH}"
RUN git clone https://github.com/bmeg/grip && \
  cd grip && \
  git checkout grids && \
  make
WORKDIR /opt
