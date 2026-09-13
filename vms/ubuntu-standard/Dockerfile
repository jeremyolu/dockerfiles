FROM ubuntu:24.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update && DEBIAN_FRONTEND=noninteractive apt install -y \
    ubuntu-standard \
    sudo \
    vim \
    nano \
    nginx \
    htop \
    iproute2 \
    net-tools \
    iputils-ping \
    curl \
    wget \
    dnsutils \
    traceroute \
    procps \
    lsof \
    openssh-client \
    openssh-server \
    git \
    && apt clean \
    && rm -rf /var/lib/apt/lists/*

CMD ["bash"]