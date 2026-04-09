# Eversince

Eversince is a creative agent that works across image, video, audio, and motion graphics. It plans, generates, and iterates. It orchestrates the latest AI models with craft specializations, does agentic video editing, and delivers standalone assets or 1080p and 4K exported videos. It can generate from scratch or build on your own assets, and works for one-off tasks or as a creative employee in any agent-to-agent workflow.

## Install

### Claude Code

```
/plugin marketplace add eversince-ai/plugin
/plugin install eversince@eversince-ai-plugin
```

### Codex

```
Install plugin from the repo https://github.com/eversince-ai/plugin
```

### OpenClaw

```
openclaw plugins install eversince --marketplace eversince-ai/plugin
```

### Other agents (Gemini CLI, Cursor, etc.)

Clone or copy the `skills/eversince/` directory into your agent's skills directory.

## Quick start

1. Get an API key at [eversince.ai/app/settings](https://eversince.ai/app/settings)
2. Create a project:

```bash
curl -X POST https://eversince.ai/api/v1/projects \
  -H "Authorization: Bearer $EVERSINCE_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"brief": "Your creative brief here", "mode": "autonomous"}'
```

3. Poll `GET /projects/:id` until `status` is `idle`
4. Get the result from `assembled_url` (rendered video) or `GET /projects/:id/assets` (individual files)

## Files

- [`skills/eversince/SKILL.md`](skills/eversince/SKILL.md) — Main skill. Setup, workflow, project options, modes, credits, error handling.
- [`skills/eversince/references/api-reference.md`](skills/eversince/references/api-reference.md) — Complete endpoint catalog with request/response shapes.
- [`skills/eversince/references/advanced-patterns.md`](skills/eversince/references/advanced-patterns.md) — Long-term projects, parallel projects, variations, project discovery.

## Links

- [eversince.ai](https://eversince.ai)
- [docs.eversince.ai](https://docs.eversince.ai)
- [support@eversince.ai](mailto:support@eversince.ai)
