FROM ubuntu:22.04

# renovate: datasource=github-releases depName=mikefarah/yq versioning=semver
ARG YQ_VERSION="v4.54.1"
ARG YQ_CHECKSUM="504fc38780cc46be8444ea1b72fb55919fc0bfb0"

RUN curl -Lo /usr/local/bin/yq "https://github.com/mikefarah/yq/releases/download/${YQ_VERSION}/yq_linux_amd64" \
   && echo "$YQ_CHECKSUM  /usr/local/bin/yq" | sha256sum -c \
   && chmod +x /usr/local/bin/yq
RUN /usr/local/bin/yq --version