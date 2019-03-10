FROM fedora:latest

RUN curl -Lo jk https://github.com/jkcfg/jk/releases/download/0.2.3/jk-linux-amd64 && \
    chmod +x jk && \
    mv jk /usr/bin/

ENTRYPOINT [ "jk" ]
CMD ["help"]
