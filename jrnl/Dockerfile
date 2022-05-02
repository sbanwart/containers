FROM registry.fedoraproject.org/fedora-minimal:35

LABEL maintainer="sbanwart@acm.org"
LABEL version="2.8.4"
LABEL description="A container for running the jrnl tool. https://jrnl.sh/"

RUN microdnf update -y && \
    microdnf install -y python3-pip && \
    pip3 install --no-cache-dir jrnl==2.8.4 && \
    microdnf clean all && \
    rm -rf /var/cache/yum

RUN useradd jrnl

USER jrnl

ENTRYPOINT [ "jrnl" ]
