FROM ubuntu:22.04

# renovate: datasource=github-releases depName=kovetskiy/mark versioning=loose
ARG MARK_VERSION="8.10"
ARG MARK_CHECKSUM="3dd6d0ab998b035dfd885af8efc798ac474484af"

RUN curl -Lo /usr/local/bin/mark "https://github.com/kovetskiy/mark/releases/download/${MARK_VERSION}/mark_${MARK_VERSION}_Linux_x86_64.tar.gz" \
   && echo "$MARK_CHECKSUM  /usr/local/bin/mark" | sha256sum -c \
   && chmod +x /usr/local/bin/mark
RUN /usr/local/bin/mark --version
