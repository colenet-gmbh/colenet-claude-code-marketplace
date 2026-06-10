# colenet Claude Code Marketplace

The official [Claude Code](https://docs.claude.com/en/docs/claude-code) plugin
marketplace of [colenet GmbH](https://www.colenet.de) — a specialist in agile
consulting, software development, and agile training.

This marketplace lists colenet's Claude Code plugins. Each plugin lives in its own
repository and is referenced here.

## Add the marketplace

```text
/plugin marketplace add colenet-gmbh/colenet-claude-code-marketplace
```

Then browse and install plugins:

```text
/plugin
```

## Available plugins

| Plugin | Repository | Description |
|--------|-----------|-------------|
| `colenet-agile` | [`colenet-claude-code-plugin`](https://github.com/colenet-gmbh/colenet-claude-code-plugin) | Harness for agile product development in teams. Bundles colenet's best practices as skills — growing step by step. |

Install a specific plugin:

```text
/plugin install colenet-agile@colenet
```

## How this marketplace is organized

- This repository contains only `.claude-plugin/marketplace.json` (the registry) and
  this README.
- Plugins are **not** vendored here; each is referenced from its own GitHub repository
  via a `github` source. This keeps plugin development independent and lets each plugin
  version on its own.

## Adding a new plugin

1. Create and publish the plugin's own repository (with `.claude-plugin/plugin.json`).
2. Add an entry to the `plugins` array in
   [`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json), pointing at the
   plugin repo via its `github` source.
3. Add a row to the table above.

## License

MIT © colenet GmbH.
