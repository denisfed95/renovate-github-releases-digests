FROM ubuntu:22.04

# renovate: datasource=github-releases depName=mikefarah/yq versioning=semver
ARG YQ_VERSION="v4.54.3"
ARG YQ_CHECKSUM="f2944b823f84906a127dbd29e4c2a3e60c4e550e"

RUN curl -Lo /usr/local/bin/yq "https://github.com/mikefarah/yq/releases/download/${YQ_VERSION}/yq_linux_amd64" \
   && echo "$YQ_CHECKSUM  /usr/local/bin/yq" | sha256sum -c \
   && chmod +x /usr/local/bin/yq
RUN /usr/local/bin/yq --version