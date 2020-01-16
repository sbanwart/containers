FROM alpine:latest

LABEL maintainer="sbanwart@acm.org"
LABEL version="2.0.0"
LABEL description="A container for running the HTTPie tool. https://httpie.org"

RUN apk add --no-cache python3 && \
    pip3 install --upgrade pip setuptools httpie && \
    rm -r /root/.cache

ENTRYPOINT [ "http" ]
CMD ["--help"]
