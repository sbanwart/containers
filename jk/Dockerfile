FROM fedora:latest

LABEL maintainer="sbanwart@acm.org"
LABEL version="0.2.9"
LABEL description="A container for running the jk templating tool. https://jkcfg.github.io"

RUN curl -Lo jk https://github.com/jkcfg/jk/releases/download/0.2.9/jk-linux-amd64 && \
    chmod +x jk && \
    mv jk /usr/bin/ && \
    mkdir -p /data

WORKDIR /data

ENTRYPOINT [ "jk" ]
CMD ["help"]
