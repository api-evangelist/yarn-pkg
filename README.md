# Yarn

Yarn is an open-source JavaScript package manager and project manager. Originally created at Facebook in 2016, Yarn is now a fully independent community-governed project. The current generation — Yarn Berry, currently v4 — lives at [yarnpkg/berry](https://github.com/yarnpkg/berry) and is written in TypeScript under the BSD-2-Clause license.

Yarn was the first package manager designed specifically around workspaces and introduced Plug'n'Play (a node_modules-free module resolution strategy), Zero-Installs (committable caches for instant clones), Constraints (a cross-workspace policy DSL), a rich protocol system, and a first-class plugin API.

This repository is the API Evangelist catalog entry for Yarn. It captures the Yarn surface area in `apis.yml` along with supporting artifacts.

## Surfaces Profiled

- **Yarn CLI** — `yarn install`, `add`, `remove`, `up`, `run`, `exec`, `dlx`, `info`, `why`, `pack`, `rebuild`, `dedupe`, `node`, `bin`, `search`, `upgrade-interactive`, `stage`
- **Yarn Workspaces** — `yarn workspace`, `yarn workspaces foreach`, `yarn workspaces focus`, `yarn workspaces list`
- **Yarn Plug'n'Play (PnP)** — node_modules-free dependency resolution via a single `.pnp.cjs` manifest, plus a Rust implementation (`pnp-rs`)
- **Yarn Zero-Installs** — commit the cache so clones bootstrap with no `yarn install`
- **Yarn Constraints** — JavaScript and Prolog DSL for cross-workspace policy enforcement
- **Yarn Protocols** — `npm:`, `git:`, `github:`, `file:`, `link:`, `portal:`, `patch:`, `exec:`, `workspace:`, and `http(s):`
- **Yarn Plugin API** — register commands, resolvers, fetchers, linkers, and lifecycle hooks via `@yarnpkg/core`
- **Yarn Version (Release Workflow)** — deferred per-workspace version decisions applied at release time
- **Yarn Patch** — `yarn patch` / `yarn patch-commit` for first-class dependency patching
- **Yarn DLX** — ephemeral package execution (Yarn's npx replacement)

## Key Properties

- **License:** BSD-2-Clause
- **Governance:** independent community project, GOVERNANCE.md in `yarnpkg/berry`
- **Language:** TypeScript (~85%), with Rust for `pnp-rs`
- **Distribution:** Corepack (recommended), or `npm install -g yarn`
- **Pin to project:** the `packageManager` field in `package.json`, or `yarn set version stable`
- **Configuration:** `.yarnrc.yml`
- **Manifest:** `package.json`
- **Lockfile:** `yarn.lock` (text-based, deterministic)

## Ecosystem Packages

| Package | Purpose |
|---|---|
| `@yarnpkg/core` | Programmatic API used by the CLI and plugins |
| `@yarnpkg/cli` | Command-line interface built on `@yarnpkg/core` |
| `@yarnpkg/pnp` | Plug'n'Play hook generation |
| `@yarnpkg/fslib` | Type-safe filesystem abstraction |
| `@yarnpkg/shell` | Portable bash-like shell interpreter for `package.json` scripts |
| `@yarnpkg/sdks` | Editor SDKs (VS Code, Vim, etc.) for PnP integration |

## Default Plugins (selected)

- `plugin-npm` — npm registry resolution
- `plugin-pnp` — Plug'n'Play installation
- `plugin-workspace-tools` — monorepo coordination
- `plugin-npm-cli` — `yarn npm publish` / login / audit / tag / whoami
- `plugin-constraints` — `yarn constraints` enforcement
- `plugin-typescript` — automatic `@types/*` co-installation
- `plugin-interactive-tools` — `yarn upgrade-interactive`, `yarn search`
- `plugin-stage` — stage Yarn files to version control

## Artifacts

- [`apis.yml`](apis.yml) — APIs.json v0.16 catalog entry
- [`vocabulary/yarn-pkg-vocabulary.yml`](vocabulary/yarn-pkg-vocabulary.yml) — Yarn vocabulary
- [`json-ld/yarn-pkg-context.jsonld`](json-ld/yarn-pkg-context.jsonld) — JSON-LD context for Yarn concepts
- [`json-schema/yarn-pkg-workspace-schema.json`](json-schema/yarn-pkg-workspace-schema.json) — JSON Schema for a Yarn workspace `package.json`

## References

- Homepage: <https://yarnpkg.com>
- Getting started: <https://yarnpkg.com/getting-started>
- Install: <https://yarnpkg.com/getting-started/install>
- CLI reference: <https://yarnpkg.com/cli>
- Programmatic API: <https://yarnpkg.com/api>
- Migration guide: <https://yarnpkg.com/migration/guide>
- GitHub: <https://github.com/yarnpkg/berry>
- RFCs: <https://github.com/yarnpkg/rfcs>
- Discord: <https://discord.gg/yarnpkg>
- Open Collective: <https://opencollective.com/yarnpkg>

## License

This catalog entry's content is published under the API Evangelist editorial license. Yarn itself is licensed under [BSD-2-Clause](https://github.com/yarnpkg/berry/blob/master/LICENSE.md).
