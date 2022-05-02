FROM registry.fedoraproject.org/fedora-minimal:35

LABEL maintainer="sbanwart@acm.org"
LABEL version="3.1.0"
LABEL description="A container for running the HTTPie tool. https://httpie.org"

RUN microdnf update -y && \
    microdnf install -y python3-pip && \
    pip3 install --no-cache-dir httpie==3.1.0 && \
    microdnf clean all && \
    rm -rf /var/cache/yum

RUN useradd httpie

USER httpie

ENTRYPOINT [ "http" ]
CMD ["--help"]
