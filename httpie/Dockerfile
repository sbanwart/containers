FROM registry.fedoraproject.org/fedora-minimal:37

LABEL maintainer="sbanwart@acm.org"
LABEL version="3.2.1"
LABEL description="A container for running the HTTPie tool. https://httpie.org"

RUN microdnf update -y && \
    microdnf install -y python3-pip shadow-utils && \
    pip3 install --no-cache-dir httpie==3.2.1 && \
    microdnf clean all && \
    rm -rf /var/cache/yum

RUN useradd httpie

USER httpie

ENTRYPOINT [ "http" ]
CMD ["--help"]
