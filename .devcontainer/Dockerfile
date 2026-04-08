FROM mcr.microsoft.com/devcontainers/base:debian-12

RUN apt-get update && apt-get install -y \
    curl git build-essential ca-certificates \
    && rm -rf /var/lib/apt/lists/*

COPY --from=ghcr.io/astral-sh/uv:latest /uv /uvx /usr/local/bin/
RUN uv python install 3.13

USER vscode

RUN curl -fsSL https://bun.sh/install | bash

ENV BUN_INSTALL="/home/vscode/.bun"
ENV PATH="$BUN_INSTALL/bin:$PATH"

RUN echo "export PROMPT_COMMAND='history -a'" >> /home/vscode/.bashrc
