FROM alpine:latest

LABEL maintainer="sbanwart@acm.org"
LABEL version="2.2"
LABEL description="A container for running the jrnl tool. https://jrnl.sh/"

RUN apk add --no-cache build-base libffi-dev openssl-dev python3 python3-dev && \
    pip3 install --upgrade pip && \
    pip3 install jrnl && \
    rm -r /root/.cache

ENTRYPOINT [ "jrnl" ]

