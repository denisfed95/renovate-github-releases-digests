FROM ubuntu:22.04

# renovate: datasource=github-releases depName=hashicorp/terraform versioning=semver
ARG TERRAFORM_VERSION="v1.16.6"
ARG TERRAFORM_CHECKSUM="7b8f1669b95119ac6021e05c9d10eae7cf75f60b"

RUN export TERRAFORM_FIXED_VERSION=$(echo ${TERRAFORM_VERSION} | sed 's/v//'); \
    && curl -LO /usr/local/bin/terraform https://releases.hashicorp.com/terraform/${TERRAFORM_FIXED_VERSION}/terraform_${TERRAFORM_FIXED_VERSION}_linux_amd64.zip \
    && echo "$TERRAFORM_CHECKSUM  /usr/local/bin/terraform" | sha256sum -c \
    && chmod +x /usr/local/bin/terraform
RUN /usr/local/bin/terraform --version