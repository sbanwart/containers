FROM registry.fedoraproject.org/fedora-minimal:34

LABEL maintainer="sbanwart@acm.org"
LABEL version="0.20.0"
LABEL description="A container for running the Diagrams drawing tool. https://diagrams.mingrammer.com/"

RUN microdnf install -y graphviz python3-pip && \
    pip install --no-cache-dir diagrams==0.20.0 && \
    microdnf clean all && \
    rm -rf /var/cache/yum && \
    mkdir -p /data

RUN useradd diagrams

WORKDIR /data

USER diagrams

ENTRYPOINT [ "python3" ]
