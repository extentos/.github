# Extentos

**Add smart-glasses capabilities to any iOS or Android app.**

[![Android SDK](https://img.shields.io/maven-central/v/com.extentos/glasses?label=Android%20SDK&color=3b82f6)](https://github.com/extentos/android-glasses)
[![iOS SDK](https://img.shields.io/github/v/tag/extentos/swift-glasses?label=iOS%20SDK&color=3b82f6&sort=semver)](https://github.com/extentos/swift-glasses)
[![MCP server](https://img.shields.io/npm/v/%40extentos%2Fmcp-server?label=MCP%20server&color=3b82f6)](https://github.com/extentos/mcp-server)
[![Docs](https://img.shields.io/badge/docs-extentos.com-3b82f6)](https://extentos.com/docs)

Your app gains camera capture, voice triggers, live transcription, audio playback
and on-glasses display. Native Android and iOS SDKs do the work on device.

Your AI coding agent does the integration, through the Extentos MCP server. A
browser simulator runs the same SDK code as production, so you build and test the
whole flow before touching hardware.

Works with Meta smart glasses today (Ray-Ban Meta, Oakley Meta, Meta Ray-Ban
Display), with a multi-vendor architecture by design.

## Quick start

```bash
claude mcp add extentos -- npx -y @extentos/mcp-server@latest
```

Then ask your agent to add glasses features to your app. It discovers the SDK
surface, scaffolds the connection module, and verifies the result in the
simulator. Any MCP client works (Cursor, Cline, Codex); see
[mcp-server](https://github.com/extentos/mcp-server) for the JSON config.

## Where things live

| Component | Where |
|---|---|
| **Android SDK** | [`com.extentos:glasses`](https://central.sonatype.com/artifact/com.extentos/glasses) on Maven Central · [install & issues](https://github.com/extentos/android-glasses) |
| **iOS SDK** | [`swift-glasses`](https://github.com/extentos/swift-glasses) Swift package · lockstep version, one shared Rust core |
| **MCP server** | [`@extentos/mcp-server`](https://www.npmjs.com/package/@extentos/mcp-server) on npm · [releases & issues](https://github.com/extentos/mcp-server) |
| **Browser simulator** | [How it works](https://extentos.com/docs/concepts/transport-vs-app) |
| **Documentation** | [extentos.com/docs](https://extentos.com/docs) |

## Learn more

- [Getting started](https://extentos.com/docs/getting-started)
- [The smart-glasses ecosystem](https://extentos.com/docs/ecosystem), a maintained platform-by-platform reference: capabilities, distribution reality, and what you can actually ship, every claim cited to vendor documentation
- [Extentos vs. building on Meta DAT directly](https://extentos.com/docs/concepts/vs-meta-dat)
