# Yarn

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
