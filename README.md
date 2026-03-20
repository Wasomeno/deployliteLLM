# LiteLLM Deployment for Dokploy

## Setup

1. Copy `.env.example` to `.env`
2. Fill in `LITELLM_MASTER_KEY` (generate with `openssl rand -hex 32`)
3. Fill in `LITELLM_DB_PASSWORD` (strong password)
4. Add your provider API keys
5. Push to GitHub
6. Connect to Dokploy as Docker Compose app
7. Add domain: `litellm.yourdomain.com` → port `4000`
8. Deploy

## First-Time Setup After Deploy

1. Access `https://litellm.yourdomain.com`
2. Login with `LITELLM_MASTER_KEY`
3. Go to Admin UI to add models

## Connecting Agents

```bash
# pi.dev / Hermes Agent / generic agents
# Endpoint: https://litellm.yourdomain.com/v1
# API Key: sk-YOUR-LITELLM-MASTER-KEY
# Model: openai/gpt-4o or your configured model name
```

## Factory Droid Example Config
```json
{
  "model": "gpt-4o",
  "base_url": "https://litellm.yourdomain.com/v1",
  "api_key": "sk-YOUR-LITELLM-MASTER-KEY",
  "provider": "openai"
}
```
EOFX; __hermes_rc=$?; printf '__HERMES_FENCE_a9f7b3__'; exit $__hermes_rc
