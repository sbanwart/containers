FROM fedora:latest

RUN curl -Lo jk https://github.com/jkcfg/jk/releases/download/0.2.7/jk-linux-amd64 && \
    chmod +x jk && \
    mv jk /usr/bin/ && \
    mkdir -p /data

WORKDIR /data

ENTRYPOINT [ "jk" ]
CMD ["help"]
