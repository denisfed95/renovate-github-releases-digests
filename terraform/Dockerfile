FROM ubuntu:22.04

# renovate: datasource=github-releases depName=hashicorp/terraform versioning=semver
ARG TERRAFORM_VERSION="v1.3.5"
ARG TERRAFORM_CHECKSUM="ac28037216c3bc41de2c22724e863d883320a770056969b8d211ca8af3d477cf"

RUN export TERRAFORM_FIXED_VERSION=$(echo ${TERRAFORM_VERSION} | sed 's/v//'); \
    && curl -LO /usr/local/bin/terraform https://releases.hashicorp.com/terraform/${TERRAFORM_FIXED_VERSION}/terraform_${TERRAFORM_FIXED_VERSION}_linux_amd64.zip \
    && echo "$TERRAFORM_CHECKSUM  /usr/local/bin/terraform" | sha256sum -c \
    && chmod +x /usr/local/bin/terraform
RUN /usr/local/bin/terraform --version