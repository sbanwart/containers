FROM fedora:31

LABEL maintainer="sbanwart@acm.org"
LABEL version="0.7.4"
LABEL description="A container for running the Diagrams drawing tool. https://diagrams.mingrammer.com/"

RUN dnf install graphviz && \
    pip install diagrams \
    mkdir -p /data

WORKDIR /data

ENTRYPOINT [ "python3" ]
