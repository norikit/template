# Using this template

This repo is the **norikit project scaffold**. It encodes the standard structure every
norikit project shares (see the ecosystem docs:
[`norikit/ai-docs/`](https://github.com/norikit/norikit/tree/main/ai-docs)). Start a new
tool by filling in the placeholders below — **don't** copy another project's product code.

> Read [`norikit/ai-docs/new-project.md`](https://github.com/norikit/norikit/blob/main/ai-docs/new-project.md)
> alongside this — it's the full bootstrap checklist; this file is just the placeholder map.

## Placeholders to replace

Search the repo for these tokens and replace every occurrence:

| Token | Meaning | Example |
|---|---|---|
| `{{PROJECT}}` | the tool's name, `nori…` motif, lowercase | `noribar` |
| `{{TAGLINE}}` | one-line description of what it is | `a macOS menu-bar replacement` |
| `{{ECOSYSTEM_ROLE}}` | one sentence on how it fits norikit | `…driven by native animated SF Symbols` |
| `{{STATUS}}` | shields.io status text | `work%20in%20progress` |
| `{{DATE}}` | today, `YYYY-MM-DD` | `2026-05-31` |
| `{{OS_FLOOR}}` | minimum OS you support | `macOS 13` |

## What to do, in order

1. Replace the tokens above.
2. Add hero art at `assets/hero-light.svg` + `assets/hero-dark.svg` (or remove the
   `<picture>` block from `README.md` until you have it).
3. Fill `ai-docs/decisions.md` with your real day-one decisions (platform, stack, OS floor,
   UI/config approach if applicable, noriglaze integration). Leave the `D#`/`Q#` scheme.
4. Choose your stack and add its **build manifest** at the repo root, a **lint config**, and
   wire them into `.github/workflows/ci.yml` and `.github/dependabot.yml` where marked
   `# TEMPLATE:`. CI is graceful — it stays green until you do.
5. Put product code under `Sources/`, tests under `Tests/` (see their READMEs).
6. Capture your first work as task folders under `tasks/`.
7. **Delete this file** (`TEMPLATE.md`) — it's scaffolding, not project docs.

## Standing rules you inherit (don't drop these)

- **Keep `ai-docs/` current in the same change** that alters reality.
- **Never commit to `main`. Always branch, always PR.**
- **AGPL-3.0.**

These live in `CLAUDE.md`; keep them there.
