FROM ubuntu:22.04

# renovate: datasource=github-releases depName=mikefarah/yq versioning=semver
ARG YQ_VERSION="v4.30.5"
ARG YQ_CHECKSUM="813d7d5b16a627a1fbbd763cb508fc8f143122f8f7195c872e7367d6295a331a"

RUN curl -Lo /usr/local/bin/yq "https://github.com/mikefarah/yq/releases/download/${YQ_VERSION}/yq_linux_amd64" \
   && echo "$YQ_CHECKSUM  /usr/local/bin/yq" | sha256sum -c \
   && chmod +x /usr/local/bin/yq
RUN /usr/local/bin/yq --version