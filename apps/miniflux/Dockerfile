ARG VERSION
FROM ghcr.io/miniflux/miniflux:${VERSION} as upstream
FROM ghcr.io/elfhosted/alpine:rolling@sha256:6947c0e498db6537c7dc500a5521a42c0d799e0e69da2d6c3ca0182cc81ffff2 
COPY --from=upstream /usr/bin/miniflux /usr/bin/miniflux

ENV LISTEN_ADDR 0.0.0.0:8080
CMD ["/usr/bin/miniflux"]
