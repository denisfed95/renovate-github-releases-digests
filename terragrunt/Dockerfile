FROM ubuntu:22.04

# renovate: datasource=github-releases depName=gruntwork-io/terragrunt versioning=semver
ARG TERRAGRUNT_VERSION="v0.42.4"
ARG TERRAGRUNT_CHECKSUM="433320f86ec6da3539e2785c9bb41820f5e3337a994b47650a06a17890953592"

RUN curl -Lo /usr/local/bin/terragrunt "https://github.com/gruntwork-io/terragrunt/releases/download/${TERRAGRUNT_VERSION}/terragrunt_linux_amd64" \
   && echo "$TERRAGRUNT_CHECKSUM  /usr/local/bin/terragrunt" | sha256sum -c \
   && chmod +x /usr/local/bin/terragrunt
RUN /usr/local/bin/terragrunt --version
