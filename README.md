# CPA Accordion

Visual context management for AI agents at the HTTP proxy layer.

CPA Accordion is a new project built from [Accordion](https://github.com/a-Fig/Accordion).
It adapts Accordion's pi-based context management to run as a plugin in the HTTP
proxy, with the existing UI and dashboard embedded in the CPA plugin management
interface through an iframe.

## First milestone

Edit the context sent to the model across multiple turns, with session affinity
handled separately from context editing.

The goal is to keep Accordion's visual approach to inspecting, folding, and
restoring context while moving the integration out of pi's extension hooks and
into the proxy.

## Status

Early development. The repository currently contains the original pi-based
implementation. Proxy-side context editing and the CPA iframe integration are
planned, not yet implemented.

Setup instructions will be added when the new integration is ready.

## Origins

Forked from Accordion, with this new direction being developed together with
Aditya (Aadi).

The [original README](docs/reference/README.original.md) is preserved as an
upstream reference, not as setup instructions for CPA Accordion.

## License

[MIT](LICENSE)
