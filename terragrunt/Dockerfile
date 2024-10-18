FROM ubuntu:22.04

# renovate: datasource=github-releases depName=gruntwork-io/terragrunt versioning=semver
ARG TERRAGRUNT_VERSION="v0.68.4"
ARG TERRAGRUNT_CHECKSUM="0604b6687a47bd33f2326c2e5c9c6ab61c6788d4"

RUN curl -Lo /usr/local/bin/terragrunt "https://github.com/gruntwork-io/terragrunt/releases/download/${TERRAGRUNT_VERSION}/terragrunt_linux_amd64" \
   && echo "$TERRAGRUNT_CHECKSUM  /usr/local/bin/terragrunt" | sha256sum -c \
   && chmod +x /usr/local/bin/terragrunt
RUN /usr/local/bin/terragrunt --version
