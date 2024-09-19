FROM ubuntu:22.04

# renovate: datasource=github-releases depName=terraform-docs/terraform-docs versioning=semver
ARG TERRAFORM_DOCS_VERSION="v0.19.0"
ARG TERRAFORM_DOCS_CHECKSUM="af31cc618e8f4763da3323de4040927d849041de"
RUN curl -LO https://github.com/terraform-docs/terraform-docs/releases/download/${TERRAFORM_DOCS_VERSION}/terraform-docs-${TERRAFORM_DOCS_VERSION}-linux-amd64.tar.gz