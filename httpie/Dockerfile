FROM registry.fedoraproject.org/fedora-minimal:31

LABEL maintainer="sbanwart@acm.org"
LABEL version="2.1.0"
LABEL description="A container for running the HTTPie tool. https://httpie.org"

RUN microdnf install -y python3-pip && \
    pip3 install --no-cache-dir httpie==2.1.0 && \
    microdnf clean all && \
    rm -rf /var/cache/yum

ENTRYPOINT [ "http" ]
CMD ["--help"]
