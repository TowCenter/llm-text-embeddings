FROM mcr.microsoft.com/devcontainers/python:3.12

# System deps for scientific/python wheels
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        build-essential \
        git \
        curl \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /workspaces/llm-text-embeddings
