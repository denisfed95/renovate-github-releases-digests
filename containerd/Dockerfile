FROM debian:bullseye-slim
RUN apt-get update \
  && apt-get install -y curl \
  && rm -Rf /var/lib/apt/lists/*

# https://github.com/containerd/containerd/releases
# - publishes individual ${file}.sha256sum files
# renovate: datasource=github-releases depName=containerd/containerd versioning=semver
ARG CONTAINERD_VERSION="v1.5.3"
ARG CONTAINERD_CHECKSUM="0e8719f54c6dc6571fc1170da75a85e86c17636b"

RUN curl -o /tmp/container.tgz -L "https://github.com/containerd/containerd/releases/download/${CONTAINERD_VERSION}/containerd-$(echo ${CONTAINERD_VERSION} | sed 's/^v//g')-linux-amd64.tar.gz" \
  && echo "$CONTAINERD_CHECKSUM  /tmp/container.tgz" | sha256sum -c \
  && tar -C /usr/local -xvvzf /tmp/container.tgz \
  && rm -f /tmp/container.tgz

RUN /usr/local/bin/containerd --version
