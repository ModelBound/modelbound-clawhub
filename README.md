# ModelBound for OpenClaw

Pull your team's curated skills, rules, and knowledge from [ModelBound](https://modelbound.co) directly into OpenClaw — without leaving your terminal.

## What you get

- **Team skills on tap.** Search and pull `SKILL.md` files curated by your team.
- **Always-fresh context.** ModelBound is the source of truth — your IDE and OpenClaw stay in sync.
- **Lean MCP surface.** A handful of meta-tools instead of 50+, so OpenClaw's context stays small.

## Install

```bash
clawhub skill install modelbound/modelbound
```

Then set your API key (one-time):

```bash
export MODELBOUND_API_KEY=mb_...
# Optional: scope to a specific team
export MODELBOUND_TEAM_ID=team_...
```

Get a key at <https://modelbound.co/api-keys>.

## How it works

The skill connects OpenClaw to ModelBound's hosted MCP server at `https://mcp.modelbound.co`. The agent calls `modelbound.listTools` first, picks the right tool for the task, and routes through `modelbound.callTool`. See `skills/modelbound/SKILL.md` for the full agent workflow.

## Links

- Docs: <https://modelbound.co/connect/mcp>
- Source of truth model: <https://modelbound.co/guides/cursor-extension>
- Issues: <https://github.com/ModelBound/modelbound-clawhub/issues>

## License

MIT
