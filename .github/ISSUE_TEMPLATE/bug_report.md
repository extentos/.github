---
name: Bug report
about: Something in the Extentos SDK didn't work as expected
labels: bug
---

<!--
Not a bug? Missing capability or DX friction → use the "Feedback / question" template.
Security issue → do NOT file publicly. Email hello@extentos.com with subject prefix [SECURITY].
Billing or account → https://extentos.com/contact

Before filing, two commands resolve most reports on their own:
  npx @extentos/mcp-server@latest whoami
  ask your agent: "Run getEventLog with filter errors on session <sessionId>"
-->

**What happened**

<!-- What did you (or your agent) try to do, and what went wrong? -->

**Expected behavior**

**Install state**

<!-- Paste the output of `npx @extentos/mcp-server@latest whoami`. This one block
     covers MCP + library versions, install id, tier, and auth state. -->

```
```

**Setup**

- Platform: <!-- Android API level, or iOS version + device model -->
- Transport: <!-- real glasses (RealMeta) / browser simulator / local sim (LocalSim) -->
- Agent host: <!-- Claude Code / Cursor / Windsurf / Cline / other, or none -->

**Steps to reproduce**

1.

**Logs**

<!-- getEventLog output if a simulator session was involved, otherwise Logcat
     (Android) / os_log (iOS). Please redact tokens and credentials. A Meta
     Client Token or an Extentos auth token in a public issue is a live secret. -->

```
```

**If this involves real hardware**

- Ray-Ban Meta variant: <!-- Gen 1 / Gen 2 / Display -->
- Bluetooth pairing state before the bug:
- Does it also repro on the simulator? <!-- yes / no / didn't try -->
