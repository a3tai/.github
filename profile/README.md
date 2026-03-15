# Agent Three

A production-grade agent runtime built by the engineers who usually say no.

## What we build

The gap in the market isn't capability; it's governance. Every agent platform today is powerful and ungoverned: token burns, persona drift, tool misuse, infinite loops, no audit trail, no blast radius control, no replay. Enterprise security teams reject these tools by default.

A3T is the runtime they say yes to. Every agent run is a workflow — cancellable, observable, auditable. No hardcoded models, keys, or prompts in code. The `agent_runs` table is source of truth. Four trust primitives underpin everything: bounded execution, deterministic replay, verifiable outputs, and secure isolation.

## Tech

`Next · Go · gRPC · PostgreSQL · Swift · Wails · Kubernetes`

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
| [a3tai/desktop](https://github.com/a3tai/desktop) | Wails v2 desktop app — local gateway, command palette, voice/STT, session history. |
| [a3tai/chatapp](https://github.com/a3tai/chatapp) | iOS client — SwiftUI, Face ID, voice, glass morphism. Dark terminal-meets-native. |

→ [a3t.ai](https://a3t.ai)
