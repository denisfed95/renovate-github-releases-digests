FROM alpine:3.14.0
RUN apk --no-cache add curl

# https://github.com/bufbuild/buf/releases
# - publishes sha256.txt describing all assets
# renovate: datasource=github-releases depName=bufbuild/buf versioning=semver
ARG BUF_VERSION="v0.56.0"
ARG BUF_CHECKSUM="66d1594abcdd9ff9014af789f23f3f3a6b81ae1d"

RUN curl -o /usr/local/bin/buf -L "https://github.com/bufbuild/buf/releases/download/${BUF_VERSION}/buf-Linux-x86_64" \
  && echo "$BUF_CHECKSUM  /usr/local/bin/buf" | sha256sum -c \
  && chmod +x /usr/local/bin/buf
RUN /usr/local/bin/buf --version

