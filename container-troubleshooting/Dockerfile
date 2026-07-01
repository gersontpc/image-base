FROM velero/velero:release-1.17-dev AS velero

ENV VELERO_VERSION=1.17.0

RUN apk update && \
    apk add --no-cache \
    alpine \
        && wget https://github.com/vmware-tanzu/velero/archive/refs/tags/v${VELERO_VERSION}.zip \
        && unzip v${VELERO_VERSION}.zip

FROM alpine:3.22

LABEL MANTAINER="gerson.tpc@outlook.com"

COPY --from=velero --chmod=0755 ./velero /usr/local/bin/velero

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