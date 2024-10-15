ARG VERSION

FROM ghcr.io/elfhosted/alpine:rolling@sha256:6947c0e498db6537c7dc500a5521a42c0d799e0e69da2d6c3ca0182cc81ffff2

RUN apk add --no-cache aria2

ENTRYPOINT ["/usr/bin/aria2c", "--enable-rpc", "--rpc-listen-all"]
