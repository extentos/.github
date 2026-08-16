# Security policy

**Do not report security issues in a public issue tracker.**

Email **hello@extentos.com** with the subject prefix `[SECURITY]`.

## What to include

- Affected component (MCP server, Android SDK, iOS SDK, backend, simulator UI)
- Affected version
- Reproduction steps
- Impact assessment (data exposure, privilege escalation, and so on)
- Whether you have shared this with anyone else

## What to expect

Acknowledgment within 7 days. Patch timeline depends on severity:

- **Critical** (RCE, auth bypass, mass data exposure): patch within 14 days,
  coordinated disclosure thereafter
- **High** (PII exposure, single-user data leak, persistent XSS): patch within 30 days
- **Medium / Low**: patched in the next minor release

## Supported versions

Only the current published release of each SDK receives security patches. Android and
iOS ship in lockstep on one shared core, so a fix lands on both at the same version.

## Architecture notes for researchers

The SDK is built to keep blast radius small, which is worth knowing before you dig:

- `RealMetaTransport`, the production glasses path, does not connect to the Extentos
  backend at all.
- Handler-code input and output payloads, which may contain end-user data, never reach
  Extentos servers.
- For the managed AI gateway, Extentos relays the call on its own key. Conversation
  content is not stored, only token-usage metadata.

The areas most worth review are the MCP server and the simulator/gateway backend.

Full data-handling detail: [extentos.com/docs/resources/security](https://extentos.com/docs/resources/security)
