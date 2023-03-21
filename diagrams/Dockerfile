FROM registry.fedoraproject.org/fedora-minimal:37

LABEL maintainer="sbanwart@acm.org"
LABEL version="0.23.3"
LABEL description="A container for running the Diagrams drawing tool. https://diagrams.mingrammer.com/"

RUN microdnf update -y && \
    microdnf install -y graphviz python3-pip shadow-utils && \
    pip install --no-cache-dir diagrams==0.23.3 && \
    microdnf clean all && \
    rm -rf /var/cache/yum && \
    mkdir -p /data

RUN useradd diagrams

WORKDIR /data

USER diagrams

ENTRYPOINT [ "python3" ]
