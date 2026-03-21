# Claude Code - Bunnyshell Template

Bunnyshell environment template for [Claude Code](https://github.com/anthropics/claude-code), Anthropic's agentic coding CLI.

## What's Included

- **Claude Code** pre-installed globally via npm
- **ttyd** web terminal for browser-based access
- Persistent `/workspace` volume (5Gi)
- IP whitelisting via Bunnyshell security
- Basic HTTP authentication for the web terminal

## Access

- **Web Terminal**: `https://terminal-<env.base_domain>/` (requires basic auth)
- **Shell**: `bns exec <COMPONENT_ID> --tty --stdin`

## Environment Variables

| Variable | Description |
|----------|-------------|
| `ANTHROPIC_API_KEY` | Your Anthropic API key |
| `TTYD_USER` | Web terminal username (default: `admin`) |
| `TTYD_PASS` | Web terminal password (default: `changeme`) |

## Deploy

```bash
bns environments create \
  --from-path bunnyshell.yaml \
  --name "claude-code" \
  --project <PROJECT_ID> \
  --k8s <CLUSTER_ID>

bns environments deploy --id <ENV_ID>
```
