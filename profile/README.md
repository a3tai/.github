# Agent Three

A production-grade agent runtime built by the engineers who usually say no.

## What we build

The gap in the market isn't capability — it's governance. Every agent platform today is powerful and ungoverned: token burns, persona drift, tool misuse, infinite loops, no audit trail, no blast radius control, no replay. Enterprise security teams reject these tools by default.

A3T is the runtime they say yes to. Every agent run is a Temporal workflow — cancellable, observable, auditable. Configuration is DB-driven; no hardcoded models, keys, or prompts in code. The `agent_runs` table is source of truth. Four trust primitives underpin everything: bounded execution, deterministic replay, verifiable outputs, and secure isolation.

On top of the core runtime: an LLM gateway (Bifrost, OpenAI-compatible) that routes to any provider with cost tracking and guardrails; a Sites platform that deploys AI-generated sites end-to-end via `SiteBuildWorkflow → SiteDeployWorkflow → SiteTestWorkflow`; and native clients for desktop and iOS that connect back through a self-hosted gateway.

## Tech

`Go · Temporal · Ory (Kratos/Hydra/Keto) · gRPC · PostgreSQL · Swift · Wails · Kubernetes · Cloudflare Tunnels`

## Trust primitives

```
bounded execution   token budgets, loop detection, hard timeouts
deterministic replay event-sourced runs, fully replayable
verifiable outputs  schema validation, postconditions enforced
secure isolation    sandbox per agent, least-privilege tool grants, full audit log
```

## Open source

| repo | what it is |
|------|-----------|
| [a3tai/openclaw-go](https://github.com/a3tai/openclaw-go) | Go SDK for the OpenClaw gateway protocol. |
| [a3tai/bspec](https://github.com/a3tai/bspec) | Behavioral spec framework. |
| [a3tai/mcp-pdf-reader](https://github.com/a3tai/mcp-pdf-reader) | MCP server for PDF ingestion. |

→ [a3t.ai](https://a3t.ai)
