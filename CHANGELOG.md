# Changelog

All notable changes to **anti-ai-slop** are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.1.0] — 2026-09-01

### Added

- Published the interactive picker to npm as **`anti-ai-slop`** (bin `anti-ai-slop`, public access). `npx anti-ai-slop` is now a real one-command install for all seven agents.
- Confirmed the publish-ready package (23 files: `index.mjs`, `lib/`, all 17 skills, and the two contrast helpers).
- Added a visual identity: logo, hero banner, and tier/flow diagrams.

### Changed

- Version bumped to v2.1.0 across package, plugin, CLI, READMEs, and guide to keep the repo in sync with the published package.

## [2.0.3] — 2026-09-01

### Added

- `CONTRIBUTING.md` (how to add an indicator, fix the installer, and submit).
- `.gitattributes` to normalize line endings (LF) across all files.
- GitHub Actions CI (`.github/workflows/ci.yml`): validates JSON manifests, verifies every skill has `name` + `description` frontmatter, and runs the installer smoke test on push and PR.
- GitHub issue and pull-request templates.
- Root `npm test` / `npm run check` scripts and a `publishConfig` to the CLI package so the picker is ready to publish as `anti-ai-slop`.

## [2.0.2] — 2026-09-01

### Changed

- Split the README into two standalone documents, each with a crossing language link:
  - `README.md` — English.
  - `README.id.md` — Bahasa Indonesia.
- Cleaned the license sections in both READMEs.
- Rewrote `SECURITY.md` to match the `anti-ai-slop` repo identity and be a complete, accurate security boundary document.

## [2.0.1] — 2026-09-01

### Changed

- Polished the public README to a professional standard: badge row, feature summary, install matrix, skills reference, usage modes, roadmap, FAQ, and contributing — bilingual (EN / ID).
- Finalized the LICENSE as a clean, complete MIT license.
- Verified all 17 skills carry valid `name` + `description` frontmatter so the skills.sh crawler parses them cleanly.

## [2.0.0] — 2026-09-01

### Added

- The **master taxonomy** (`antislop-master`): a P0–P6 severity-tiered catalog of ~180 indicators across color, typography, layout, components, copy, motion, UX states, authenticity, code, and platform.
- Nine focused skills, each mapping back to master catalog codes:
  - `antislop-layout` — hero, sections, symmetry, grids, spacing rhythm.
  - `antislop-dashboard` — metric cards, charts, tables, complete states.
  - `antislop-forms` — forms, validation, empty/loading/error/offline states.
  - `antislop-motion` — animation with a UX reason, reduced-motion.
  - `antislop-nav` — navigation, headers, footers, real IA, no dead links.
  - `antislop-authenticity` — evidence, product intent, no fake data.
  - `antislop-designsystem` — tokens, spacing scale, theme parity, hierarchy.
  - `antislop-imagery` — illustrations, backgrounds, icons, media tied to product.
  - `antislop-mobile` — mobile + Flutter/native reflow, tap targets, platform intent.

### Changed

- Reframed the core filter on the root cause (`no hierarchy + no specificity + no restraint + no opinion`) and pointed it to `antislop-master`.
- Updated the picker CLI to offer and point to all skills.

## [1.0.0] — 2026-08-31

### Added

- The core filter (`antislop`) with rules R-01 → R-38 in three tiers: Hard Gate, Purpose-Gate, Quality Locks.
- The Liveliness Toolkit (ENERGY / RHYTHM / MOTION dials) and the Design Read.
- The Delivery Gate: a PASS/FAIL report in four blocks run before shipping.
- Additive skills, one per concern:
  - `antislop-ui` — UI / visual rules.
  - `antislop-copywriting` — copy & text rules.
  - `antislop-human` — accessibility, with the contrast checker and MCP server.
  - `antislop-layoutmobile` — mobile layout rules.
  - `antislop-code` — code comment hygiene.
  - `slop` — one-shot loader for the whole family.
- Multi-way packaging: an npm picker CLI, a Claude Code marketplace plugin, an Antigravity plugin, a skills.sh-readable directory, and a single-file manual path.

[2.1.0]: https://github.com/muris11/anti-ai-slop/compare/v2.0.3...v2.1.0
[2.0.3]: https://github.com/muris11/anti-ai-slop/compare/v2.0.2...v2.0.3
[2.0.2]: https://github.com/muris11/anti-ai-slop/compare/v2.0.1...v2.0.2
[2.0.1]: https://github.com/muris11/anti-ai-slop/compare/v2.0.0...v2.0.1
[2.0.0]: https://github.com/muris11/anti-ai-slop/compare/v1.0.0...v2.0.0
[1.0.0]: https://github.com/muris11/anti-ai-slop/releases/tag/v1.0.0
