FROM registry.fedoraproject.org/fedora-minimal:33

LABEL maintainer="sbanwart@acm.org"
LABEL version="1.6.0"
LABEL description="A container for running the curlie HTTP tool. https://curlie.io"

RUN curl -Lo curlie.rpm https://github.com/rs/curlie/releases/download/v1.6.0/curlie_1.6.0_linux_amd64.rpm && \
    rpm -i curlie.rpm && \
    mkdir -p /data

RUN useradd curlie

WORKDIR /data

USER curlie

ENTRYPOINT [ "curlie" ]
CMD ["--help"]
