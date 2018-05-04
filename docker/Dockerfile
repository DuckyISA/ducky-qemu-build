FROM docker.io/fedora
MAINTAINER Milos Prchlik <happz@happz.cz>

RUN    dnf update -y \
    && dnf install -y dnf-plugins-core \
    && dnf copr -y enable happz/ducky-qemu \
    && dnf install -y ducky-qemu \
    && dnf clean all

ENV PATH=/opt/ducky/bin:$PATH

ENTRYPOINT ["/opt/ducky/bin/qemu-system-ducky"]
