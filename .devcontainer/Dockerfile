FROM mcr.microsoft.com/devcontainers/python:3.12
ENV PIP_NO_CACHE_DIR=1 \
    PIP_DISABLE_PIP_VERSION_CHECK=1

# System deps for scientific/python wheels
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        build-essential \
        git \
        curl \
    && rm -rf /var/lib/apt/lists/*

COPY requirements.txt /tmp/requirements.txt
RUN pip install -r /tmp/requirements.txt \
    && rm -rf /root/.cache/pip /home/vscode/.cache/pip /tmp/pip-*

WORKDIR /workspaces/llm-text-embeddings
