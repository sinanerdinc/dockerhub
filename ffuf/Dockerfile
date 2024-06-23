FROM alpine:latest

RUN apk update && apk add --no-cache \
    git \
    go \
    && rm -rf /var/cache/apk/*

RUN mkdir -p /go/src/github.com/ffuf
RUN git clone https://github.com/ffuf/ffuf.git /go/src/github.com/ffuf
WORKDIR /go/src/github.com/ffuf
RUN go install github.com/ffuf/ffuf/v2@latest
ENV PATH="/root/go/bin:${PATH}"

ENTRYPOINT ["ffuf"]
