FROM ubuntu:22.04

# renovate: datasource=github-releases depName=gruntwork-io/terragrunt versioning=semver
ARG TERRAGRUNT_VERSION="v0.99.5"
ARG TERRAGRUNT_CHECKSUM="9be8baedaced8cac02803593b00c3dac01c0cb79"

RUN curl -Lo /usr/local/bin/terragrunt "https://github.com/gruntwork-io/terragrunt/releases/download/${TERRAGRUNT_VERSION}/terragrunt_linux_amd64" \
   && echo "$TERRAGRUNT_CHECKSUM  /usr/local/bin/terragrunt" | sha256sum -c \
   && chmod +x /usr/local/bin/terragrunt
RUN /usr/local/bin/terragrunt --version
