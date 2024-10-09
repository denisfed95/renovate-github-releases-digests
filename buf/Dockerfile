FROM alpine:3.14.0
RUN apk --no-cache add curl

# https://github.com/bufbuild/buf/releases
# - publishes sha256.txt describing all assets
# renovate: datasource=github-releases depName=bufbuild/buf versioning=semver
ARG BUF_VERSION="v1.45.0"
ARG BUF_CHECKSUM="bee67191e0a207d52b6c7f0ac9d3d1210898d2f9"

RUN curl -o /usr/local/bin/buf -L "https://github.com/bufbuild/buf/releases/download/${BUF_VERSION}/buf-Linux-x86_64" \
  && echo "$BUF_CHECKSUM  /usr/local/bin/buf" | sha256sum -c \
  && chmod +x /usr/local/bin/buf
RUN /usr/local/bin/buf --version

