# CPA Accordion

Visual context management for AI agents, built as a plugin for
[CLIProxyAPI (CPA)](https://github.com/router-for-me/CLIProxyAPI).

CPA Accordion builds on [Accordion](https://github.com/a-Fig/Accordion) to let you
inspect, fold, and restore the context sent to models through CPA.

## Planned architecture

- A native Go plugin runs inside CPA's process. The authoritative context engine
  and conductor host run in Go, with no separate core daemon.
- The existing Svelte UI and dashboard stay, embedded in CPA's management
  interface through an iframe. The TypeScript context replica stays in the UI;
  shared conformance tests will keep it aligned with the Go engine.
- Optional external conductors can connect over WebSocket. Node-based conductors
  may still need Node; the core plugin will not.

## First user-facing milestone

Edit context across multiple turns for Claude Code and Codex requests through CPA.
Session affinity is a separate responsibility: match requests to conversations
and keep each conversation's context and edits isolated. If affinity is uncertain,
pass the request through unchanged rather than risk applying another session's edits.

Carry over Accordion's folding rules and safety guarantees while replacing pi's
session hooks with request/response handling and provider-format adapters.

## Status

Early development. This repository still contains the pi-based implementation.
The Go plugin, multi-turn editing through CPA, and iframe integration are planned,
not yet implemented. Plugin runtime support and agent tool handling still need
validation; iframe authentication is tracked separately.

See the [v1 roadmap](https://github.com/aadityad12/Accordion/issues/2) for the work
breakdown and [UI integration](https://github.com/aadityad12/Accordion/issues/25)
for iframe access and authentication. Setup instructions will follow a working
integration.

The [original README](docs/reference/README.original.md) is retained as an
upstream reference, with relative links adjusted for its location. It is not
setup instructions for CPA Accordion.

## License

[MIT](LICENSE)
