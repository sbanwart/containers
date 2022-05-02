FROM registry.fedoraproject.org/fedora-minimal:35

LABEL maintainer="sbanwart@acm.org"
LABEL version="1.6.9"
LABEL description="A container for running the curlie HTTP tool. https://curlie.io"

RUN microdnf update -y && \
    microdnf install -y shadow-utils
        
RUN curl -Lo curlie.rpm https://github.com/rs/curlie/releases/download/v1.6.9/curlie_1.6.9_linux_amd64.rpm && \
    rpm -i curlie.rpm && \
    mkdir -p /data

RUN useradd curlie

WORKDIR /data

USER curlie

ENTRYPOINT [ "curlie" ]
CMD ["--help"]
