FROM ubuntu:22.04

# renovate: datasource=github-releases depName=mikefarah/yq versioning=semver
ARG YQ_VERSION="v4.53.6"
ARG YQ_CHECKSUM="c14f446382944492701b16c1ddb48bb9dbe683e3"

RUN curl -Lo /usr/local/bin/yq "https://github.com/mikefarah/yq/releases/download/${YQ_VERSION}/yq_linux_amd64" \
   && echo "$YQ_CHECKSUM  /usr/local/bin/yq" | sha256sum -c \
   && chmod +x /usr/local/bin/yq
RUN /usr/local/bin/yq --version