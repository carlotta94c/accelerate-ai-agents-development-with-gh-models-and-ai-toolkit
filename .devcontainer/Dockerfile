FROM mcr.microsoft.com/devcontainers/python:1-3.12-bullseye

# The upstream base image can inherit a stale Yarn apt source whose signing key
# is unavailable during feature installation. Removing it keeps apt-get update
# working for devcontainer features such as docker-in-docker.
RUN rm -f /etc/apt/sources.list.d/yarn.list \
    /usr/share/keyrings/yarn.gpg