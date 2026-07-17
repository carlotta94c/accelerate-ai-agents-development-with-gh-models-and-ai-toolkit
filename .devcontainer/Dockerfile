FROM mcr.microsoft.com/devcontainers/python:1-3.12-bullseye

# The bullseye base image ships a preconfigured Yarn APT repo whose signing key
# (NO_PUBKEY 62D54FD4003F6525) is stale, which breaks `apt-get update` (and any
# dev container feature that runs it, e.g. docker-in-docker). Refresh the key so
# the repo verifies correctly during feature installation.
RUN set -eux; \
    apt-get update -o Dir::Etc::sourcelist="sources.list" \
        -o Dir::Etc::sourceparts="-" -o APT::Get::List-Cleanup="0" || true; \
    if [ -f /etc/apt/sources.list.d/yarn.list ]; then \
        rm -f /etc/apt/sources.list.d/yarn.list; \
    fi; \
    rm -rf /var/lib/apt/lists/*
