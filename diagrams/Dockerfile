FROM registry.fedoraproject.org/fedora-minimal:32

LABEL maintainer="sbanwart@acm.org"
LABEL version="0.16.0"
LABEL description="A container for running the Diagrams drawing tool. https://diagrams.mingrammer.com/"

RUN microdnf install -y graphviz python3-pip && \
    pip install --no-cache-dir diagrams==0.16.0 && \
    microdnf clean all && \
    rm -rf /var/cache/yum && \
    mkdir -p /data

WORKDIR /data

ENTRYPOINT [ "python3" ]
