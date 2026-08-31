# Roadmap

Tracked changes and releases for anti-ai-slop.

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
