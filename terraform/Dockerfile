FROM ubuntu:22.04

# renovate: datasource=github-releases depName=hashicorp/terraform versioning=semver
ARG TERRAFORM_VERSION="v1.16.5"
ARG TERRAFORM_CHECKSUM="ef47237fd0e03d6e93bdc510b526287f06e94c03"

RUN export TERRAFORM_FIXED_VERSION=$(echo ${TERRAFORM_VERSION} | sed 's/v//'); \
    && curl -LO /usr/local/bin/terraform https://releases.hashicorp.com/terraform/${TERRAFORM_FIXED_VERSION}/terraform_${TERRAFORM_FIXED_VERSION}_linux_amd64.zip \
    && echo "$TERRAFORM_CHECKSUM  /usr/local/bin/terraform" | sha256sum -c \
    && chmod +x /usr/local/bin/terraform
RUN /usr/local/bin/terraform --version