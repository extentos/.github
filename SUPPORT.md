# Support

Extentos is pre-1.0. Bug reports and feedback go in the GitHub issue tracker of the
component you hit. There is no SLA, but every issue is read.

## Where to file

| What broke | Where |
|---|---|
| Android SDK (`com.extentos:glasses`) | [extentos/android-glasses/issues](https://github.com/extentos/android-glasses/issues) |
| iOS SDK (`Extentos` Swift package) | [extentos/swift-glasses/issues](https://github.com/extentos/swift-glasses/issues) |
| MCP server, agent scaffolding, browser simulator, docs site | [extentos/mcp-server/issues](https://github.com/extentos/mcp-server/issues) |
| Security vulnerability | **Private only.** See [SECURITY.md](https://github.com/extentos/.github/blob/main/SECURITY.md) |
| Billing, account, or sales | [extentos.com/contact](https://extentos.com/contact) |

Not sure which one? File it anywhere above and it will get moved.

## Try these first

Most reports are answered by output you can generate yourself in under a minute:

```bash
npx @extentos/mcp-server@latest whoami   # versions, install id, tier, auth state
npx @extentos/mcp-server@latest status   # consent, telemetry, config dir
```

If the bug happened at runtime, ask your AI agent to read the structured event log:

```text
Run getEventLog with filter "errors" and limit 50 on session <sessionId>,
read the trace, and tell me where it broke.
```

Every capability call emits a request and a result event with a stable id, so the
trace usually names the failing layer on its own. If your agent still can't place it,
paste both the trace and the agent's analysis into the issue. That is the most
actionable bug report there is.

Full self-service guide, including the component triage table:
[extentos.com/docs/resources/support](https://extentos.com/docs/resources/support)

## Please redact

Event logs and Logcat dumps can contain live credentials. Strip Meta Client Tokens,
Extentos auth tokens, and AI provider keys before pasting into a public issue.
