# docs-engine

The rendering engine behind Coder's documentation: the renderer, remark/rehype
transforms, theme, and framework-agnostic UI components, published as a set of
`@coder/*` packages.

> **Documentation content lives in [`coder/coder`](https://github.com/coder/coder)
> under `docs/`.** This repository is the engine that renders that content, not
> the content itself.

## Status

🚧 **Early scaffolding.** The repository license is being finalized; until it is
set, this is a work in progress and nothing here is published to npm.

## Packages

This is a [pnpm](https://pnpm.io) + [Turborepo](https://turbo.build) monorepo.
Planned packages:

| Package | Responsibility |
| --- | --- |
| `@coder/docs-transforms` | remark/rehype plugins and pure content transforms |
| `@coder/docs-theme` | Tailwind preset, design tokens, brand and dark-mode CSS |
| `@coder/docs-ui` | Framework-agnostic React components (injected `Link`/`Image`/router) |
| `@coder/docs-config` | Typed configuration schema and shared types |
| `@coder/docs-sources` | Versions/content providers (branches, tags, bundled) |
| `@coder/docs-next` | Fumadocs App Router adapter |

So far only `@coder/docs-config` exists, as a scaffold placeholder.

## Development

Requires Node 22+ and pnpm.

```sh
pnpm install
pnpm build      # turbo run build
pnpm typecheck  # turbo run typecheck
pnpm lint       # biome lint
```
