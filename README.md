# CPA Accordion

Visual context management for AI agents, built as a plugin for
[CliProxyAPI (CPA)](https://github.com/router-for-me/CLIProxyAPI).

CPA Accordion is a new project built from [Accordion](https://github.com/a-Fig/Accordion).
The planned CPA plugin will adapt Accordion's pi-based context management to
edit model requests handled by CPA. The existing UI and dashboard will be
embedded in CPA's plugin management interface through an iframe.

## First milestone

Edit the context sent to the model across multiple turns, with session affinity
handled separately from context editing.

The goal is to keep Accordion's visual approach to inspecting, folding, and
restoring context while moving the integration out of pi's extension hooks and
into the CPA plugin.

## Status

Early development. The repository currently contains the original pi-based
implementation. The CPA plugin, multi-turn context editing through CPA, and iframe integration are
planned, not yet implemented.

Setup instructions will be added when the new integration is ready.

The [original README](docs/reference/README.original.md) is retained as an
upstream reference, with relative links adjusted for its location. It is not
setup instructions for CPA Accordion.

## License

[MIT](LICENSE)
