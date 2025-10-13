FROM alpine:latest

LABEL MANTAINER="gerson.tpc@outlook.com"

# Install dependencies
RUN apk update && \
    apk add --no-cache \
    busybox-extras \
    curl \
    jq \
    yq \
    bash \
    git \
    linux-headers \
    wget \
    aws-cli \
    tcpdump \
    vim \
    net-tools \
    iputils \
    bind-tools \
    shadow \
    procps \
    lsof \
    strace \
    gcompat \
    coreutils

WORKDIR /