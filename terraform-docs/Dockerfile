FROM ubuntu:22.04

# renovate: datasource=github-releases depName=terraform-docs/terraform-docs versioning=semver
ARG TERRAFORM_DOCS_VERSION="v0.24.0"
ARG TERRAFORM_DOCS_CHECKSUM="9d4455198941806aa02ec14369de030cda2c2b59"
RUN curl -LO https://github.com/terraform-docs/terraform-docs/releases/download/${TERRAFORM_DOCS_VERSION}/terraform-docs-${TERRAFORM_DOCS_VERSION}-linux-amd64.tar.gz