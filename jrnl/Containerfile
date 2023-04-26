FROM registry.fedoraproject.org/fedora-minimal:37

LABEL maintainer="sbanwart@acm.org"
LABEL version="3.3"
LABEL description="A container for running the jrnl tool. https://jrnl.sh/"

RUN microdnf update -y && \
    microdnf install -y python3-pip shadow-utils && \
    pip3 install --no-cache-dir jrnl==3.3 && \
    microdnf clean all && \
    rm -rf /var/cache/yum

RUN useradd jrnl

USER jrnl

ENTRYPOINT [ "jrnl" ]
