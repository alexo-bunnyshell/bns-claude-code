FROM node:22-bookworm-slim AS dev

RUN apt-get update && apt-get install -y --no-install-recommends \
    git curl bash ttyd ca-certificates \
    && rm -rf /var/lib/apt/lists/*

RUN npm install -g @anthropic-ai/claude-code

WORKDIR /workspace

EXPOSE 7681

CMD ["ttyd", "-W", "bash"]
