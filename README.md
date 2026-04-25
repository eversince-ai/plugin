# Eversince

Eversince is a creative agent that plans and executes across image, video, audio, and motion graphics. It lives in a purpose-built environment for creative work, orchestrates the latest AI models, has craft specializations, does agentic video editing, and delivers standalone assets or timeline-assembled videos. Works for one-off tasks or as a creative employee in any agent-to-agent workflow.

## Install

### Claude Code

```
/plugin marketplace add eversince-ai/plugin
/plugin install eversince@eversince-ai-plugin
```

### OpenClaw

```
openclaw plugins install eversince --marketplace eversince-ai/plugin
```

### Other agents (Gemini CLI, Cursor, etc.)

Clone or copy the `skills/eversince/` directory into your agent's skills directory.

## MCP server

Also available as a hosted MCP server at `https://mcp.eversince.ai/mcp`. Connect from any MCP-compatible client — see [eversince-ai/mcp](https://github.com/eversince-ai/mcp) for connection details.

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
