FROM fedora:31

LABEL maintainer="sbanwart@acm.org"
LABEL version="0.7.4"
LABEL description="A container for running the Diagrams drawing tool. https://diagrams.mingrammer.com/"

RUN dnf install -y graphviz python3-pip && \
    pip install diagrams && \
    dnf clean all && \
    rm -r /root/.cache && \
    mkdir -p /data

WORKDIR /data

ENTRYPOINT [ "python3" ]
