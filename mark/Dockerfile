FROM ubuntu:22.04

# renovate: datasource=github-releases depName=kovetskiy/mark versioning=loose
ARG MARK_VERSION="8.4"
ARG MARK_CHECKSUM="a8243205e5513c575bc09ff21d167bb454975618eed23e43bd1b4b4af3991836"

RUN curl -Lo /usr/local/bin/mark "https://github.com/kovetskiy/mark/releases/download/${MARK_VERSION}/mark_${MARK_VERSION}_Linux_x86_64.tar.gz" \
   && echo "$MARK_CHECKSUM  /usr/local/bin/mark" | sha256sum -c \
   && chmod +x /usr/local/bin/mark
RUN /usr/local/bin/mark --version
