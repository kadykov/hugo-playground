# Use a Microsoft base image with common dev tools pre-installed
FROM mcr.microsoft.com/devcontainers/base:ubuntu-24.04

# Install system dependencies using apt-get
USER root

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get install -y --no-install-recommends \
    git \
    hugo \
    just \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Switch back to vscode user provided by base image
USER vscode

RUN mkdir -p /home/vscode/.vscode-server/data/User/globalStorage
