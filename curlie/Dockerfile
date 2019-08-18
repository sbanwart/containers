FROM fedora:latest

LABEL maintainer="sbanwart@acm.org"
LABEL version="1.2.0"
LABEL description="A container for running the curlie HTTP tool. https://curlie.io"

RUN curl -Lo curlie.rpm https://github.com/rs/curlie/releases/download/v1.2.0/curlie_1.2.0_linux_amd64.rpm && \
    rpm -i curlie.rpm && \
    mkdir -p /data

WORKDIR /data

ENTRYPOINT [ "curlie" ]
CMD ["--help"]
