FROM ubuntu:22.04

# renovate: datasource=github-releases depName=terraform-docs/terraform-docs versioning=semver
ARG TERRAFORM_DOCS_VERSION="v0.15.0"
ARG TERRAFORM_DOCS_CHECKSUM="e0b399d9dc2eb97853a7e12f1ae678e7160cae4c811646ce70169a8d611f6cf9"
RUN curl -LO https://github.com/terraform-docs/terraform-docs/releases/download/${TERRAFORM_DOCS_VERSION}/terraform-docs-${TERRAFORM_DOCS_VERSION}-linux-amd64.tar.gz