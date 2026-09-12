FROM ubuntu:22.04

# renovate: datasource=github-releases depName=hashicorp/terraform versioning=semver
ARG TERRAFORM_VERSION="v1.16.2"
ARG TERRAFORM_CHECKSUM="82e042fb6372443813f6759056308d6adc642fa1"

RUN export TERRAFORM_FIXED_VERSION=$(echo ${TERRAFORM_VERSION} | sed 's/v//'); \
    && curl -LO /usr/local/bin/terraform https://releases.hashicorp.com/terraform/${TERRAFORM_FIXED_VERSION}/terraform_${TERRAFORM_FIXED_VERSION}_linux_amd64.zip \
    && echo "$TERRAFORM_CHECKSUM  /usr/local/bin/terraform" | sha256sum -c \
    && chmod +x /usr/local/bin/terraform
RUN /usr/local/bin/terraform --version