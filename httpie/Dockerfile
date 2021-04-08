FROM registry.fedoraproject.org/fedora-minimal:33

LABEL maintainer="sbanwart@acm.org"
LABEL version="2.4.0"
LABEL description="A container for running the HTTPie tool. https://httpie.org"

RUN microdnf install -y python3-pip && \
    pip3 install --no-cache-dir httpie==2.4.0 && \
    microdnf clean all && \
    rm -rf /var/cache/yum

RUN useradd httpie

USER httpie

ENTRYPOINT [ "http" ]
CMD ["--help"]
