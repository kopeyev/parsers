FROM registry.altlinux.org/alt/alt:p11
USER root
RUN apt-get update && apt-get install -y \
    python3-module-requests \
    python3-module-selenium

ARG UID=501
ARG GID=501

RUN groupadd -g $GID -o parser
RUN useradd -o -u $UID -g $GID -m -s /bin/bash parser

USER parser

WORKDIR /mnt/parsers
