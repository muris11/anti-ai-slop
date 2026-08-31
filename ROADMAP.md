# Roadmap

Tracked changes and releases for anti-ai-slop.

## v2.0.2 — bilingual README split + security polish

- Split the README into two standalone documents, each with a crossing language link:
  - `README.md` — English.
  - `README.id.md` — Bahasa Indonesia.
  - Both link to each other at the top (`[English](README.md)` / `[Bahasa Indonesia](README.id.md)`) and carry the full badge row.
- Cleaned the license sections in both READMEs to link `LICENSE` with the "do whatever you want" wording (EN and ID).
- Rewrote `SECURITY.md` to match the `anti-ai-slop` repo identity and be a complete, accurate security boundary document.
- Version bumped to v2.0.2 across package, plugin, CLI, READMEs, and guide.

## v2.0.1 — polish release

- Polished the public **README** to a professional standard: clean badge row, feature summary, install matrix, skills reference, usage modes, roadmap, FAQ, and contributing — bilingual (EN / ID).
- Finalized the **LICENSE** as a clean, complete MIT license (standard terms, no drift from the canonical text).
- Verified all 17 skills carry valid `name` + `description` frontmatter so the skills.sh crawler parses them cleanly; the repo is ready to be listed at `skills.sh/muris11/anti-ai-slop` (it appears once a user runs `npx skills add muris11/anti-ai-slop`).
- Version bumped to v2.0.1 across package, plugin, CLI, README, and guide.

## v2.0.0 — master taxonomy

- Added the **master taxonomy** (`antislop-master`): a P0–P6 severity-tiered catalog of ~180 indicators across color, typography, layout, components, copy, motion, UX states, authenticity, code, and platform. This is the canonical audit source for the whole system.
- Added nine focused skills, each mapping back to master catalog codes:
  - `antislop-layout` — hero, sections, symmetry, grids, spacing rhythm.
  - `antislop-dashboard` — metric cards, charts, tables, complete states.
  - `antislop-forms` — forms, validation, empty/loading/error/offline states.
  - `antislop-motion` — animation with a UX reason, reduced-motion.
  - `antislop-nav` — navigation, headers, footers, real IA, no dead links.
  - `antislop-authenticity` — evidence, product intent, no fake data.
  - `antislop-designsystem` — tokens, spacing scale, theme parity, hierarchy.
  - `antislop-imagery` — illustrations, backgrounds, icons, media tied to product.
  - `antislop-mobile` — mobile + Flutter/native reflow, tap targets, platform intent.
- Reframed the core filter on the root cause (`no hierarchy + no specificity + no restraint + no opinion`) and pointed it to `antislop-master`.
- Updated the picker CLI to offer and point to all skills. Version bumped to v2.0.0.

## v1.0.0 — initial public release

- Shipped the core filter (`antislop`) with rules R-01 → R-38 in three tiers: Hard Gate, Purpose-Gate, Quality Locks.
- Added the Liveliness Toolkit (ENERGY / RHYTHM / MOTION dials) and the Design Read.
- Added the Delivery Gate: a PASS/FAIL report in four blocks run before shipping.
- Added additive skills, one per concern:
  - `antislop-ui` — UI / visual rules.
  - `antislop-copywriting` — copy & text rules.
  - `antislop-human` — accessibility, with the contrast checker (`contrast-check.py`) and MCP server (`contrast-mcp.py`).
  - `antislop-layoutmobile` — mobile layout rules.
  - `antislop-code` — code comment hygiene.
  - `slop` — one-shot loader for the whole family.
- Built the packaging so the repo is installable in multiple ways:
  - An npm picker CLI (`antislop-ai`) that installs into Claude Code, Codex, Antigravity, OpenCode, Cursor, Gemini CLI, and Hermes, and writes the agent entry pointer.
  - A Claude Code marketplace plugin (`.claude-plugin/`).
  - An Antigravity plugin (`plugin.json` + `rules/antislop.md` pointer).
  - A `skills.sh`-readable skills directory.
  - A single-file manual path (`antislop.md`).
- Wrote this guide (`guide.md`) and the bilingual README (EN / ID).

## Planned

- Cross-agent plugin consolidation: one plugin manifest usable by more agents at once.
- More rules as new AI slop patterns are catalogued.
- Optional DESIGN.md template to make the "direction" step easier.

See the repo's issues and PRs for the live tracker.
