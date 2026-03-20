FROM node:22-bookworm-slim AS dev

RUN apt-get update && apt-get install -y --no-install-recommends \
    git curl bash ca-certificates wget \
    && wget -qO /usr/local/bin/ttyd https://github.com/tsl0922/ttyd/releases/download/1.7.7/ttyd.x86_64 \
    && chmod +x /usr/local/bin/ttyd \
    && rm -rf /var/lib/apt/lists/*

RUN npm install -g @anthropic-ai/claude-code

WORKDIR /workspace

EXPOSE 7681

CMD ["ttyd", "-W", "bash"]
