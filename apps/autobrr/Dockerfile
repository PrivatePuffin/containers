ARG VERSION
FROM ghcr.io/autobrr/autobrr:v${VERSION} as upstream

FROM ghcr.io/elfhosted/alpine:rolling@sha256:6947c0e498db6537c7dc500a5521a42c0d799e0e69da2d6c3ca0182cc81ffff2 

LABEL org.opencontainers.image.source = "https://github.com/autobrr/autobrr"

ENV HOME="/config" \
XDG_CONFIG_HOME="/config" \
XDG_DATA_HOME="/config"

WORKDIR /app

VOLUME /config

COPY --from=upstream /usr/local/bin/autobrr /usr/local/bin/
COPY --from=upstream /usr/local/bin/autobrrctl /usr/local/bin/

COPY ./apps/autobrr/regbrr.sh /

EXPOSE 7474

ENTRYPOINT ["/usr/local/bin/autobrr", "--config", "/config"]