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

## Active repos

| repo | what it is |
|------|-----------|
| [a3tai/core](https://github.com/a3tai/core) | Multi-tenant auth + agent runtime. Go, Ory stack, Temporal, gRPC. Runs on EKS. |
| [a3tai/desktop](https://github.com/a3tai/desktop) | Wails v2 desktop app — local gateway, command palette, voice/STT, session history. |
| [a3tai/chatapp](https://github.com/a3tai/chatapp) | iOS client — SwiftUI, Face ID, voice, glass morphism. Dark terminal-meets-native. |

→ [a3t.ai](https://a3t.ai)
