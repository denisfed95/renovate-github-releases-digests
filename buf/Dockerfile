FROM alpine:3.14.0
RUN apk --no-cache add curl

# https://github.com/bufbuild/buf/releases
# - publishes sha256.txt describing all assets
# renovate: datasource=github-releases depName=bufbuild/buf versioning=semver
ARG BUF_VERSION="v1.75.0"
ARG BUF_CHECKSUM="1a3a05a3e0fa350c4b814b7f48aa0e64e9a906bd"

RUN curl -o /usr/local/bin/buf -L "https://github.com/bufbuild/buf/releases/download/${BUF_VERSION}/buf-Linux-x86_64" \
  && echo "$BUF_CHECKSUM  /usr/local/bin/buf" | sha256sum -c \
  && chmod +x /usr/local/bin/buf
RUN /usr/local/bin/buf --version

