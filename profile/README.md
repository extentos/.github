# Extentos

**Add smart-glasses capabilities to any iOS or Android app.**

Extentos is a development platform for smart glasses. Your existing mobile app gains glasses features — camera capture, voice triggers, live transcription, audio playback — through native Android and iOS SDKs, and your AI coding agent does the integration work through the Extentos MCP server: discover capabilities, scaffold the connection module, validate the integration, and test it end-to-end in a browser simulator before touching hardware.

Works with Meta smart glasses today — Ray-Ban Meta, Oakley Meta, and Meta Ray-Ban Display — with a multi-vendor architecture by design.

## Quick start

Give your AI coding agent the tools:

```bash
claude mcp add extentos -- npx -y @extentos/mcp-server@latest
```

Or in any MCP client (Cursor, Cline, …):

```json
{
  "mcpServers": {
    "extentos": {
      "command": "npx",
      "args": ["-y", "@extentos/mcp-server@latest"]
    }
  }
}
```

Then ask the agent to add glasses features to your app — it discovers the SDK surface, scaffolds the connection module, and verifies the result in a browser simulator that runs the same SDK code as production.

## Components

| Component | Where |
|---|---|
| MCP server | [`@extentos/mcp-server`](https://www.npmjs.com/package/@extentos/mcp-server) on npm · [releases & issues](https://github.com/extentos/mcp-server) |
| Android SDK | [`com.extentos:glasses`](https://central.sonatype.com/artifact/com.extentos/glasses) on Maven Central · [install & issues](https://github.com/extentos/android-glasses) |
| iOS SDK | [`swift-glasses`](https://github.com/extentos/swift-glasses) Swift package · lockstep version, one shared Rust core |
| Browser simulator | [How it works](https://extentos.com/docs/concepts/transport-vs-app) — the same SDK code as production with only the transport swapped |
| Documentation | [extentos.com/docs](https://extentos.com/docs) |

## Learn more

- [Getting started](https://extentos.com/docs/getting-started)
- [The smart-glasses ecosystem](https://extentos.com/docs/ecosystem) — a maintained platform-by-platform reference: capabilities, distribution reality, and what you can actually ship, with every claim cited to vendor documentation
- [Extentos vs. building on Meta DAT directly](https://extentos.com/docs/concepts/vs-meta-dat)
