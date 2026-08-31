# Guide — Getting Started with anti-ai-slop

> New here? This guide explains what anti-ai-slop is, how to install it from zero, and how to use it. If you already know what it is, jump straight to [Install](#install). To see the full rules, read [antislop.md](antislop.md).

anti-ai-slop is a set of standard agent skills: a core filter (the `antislop` skill) plus optional skills that go deeper into UI, layout, copy, people, mobile, dashboard, motion, code comments, and more. It is a **filter, not a style guide**.

---

## What antislop does

- A core filter of **mandatory rules** in three tiers:
  - **Hard Gate** — absolute rules, never broken.
  - **Purpose-Gate** — a technique is allowed, but a reason is required.
  - **Quality Locks** — consistency rules.
- A **Liveliness Toolkit** with three dials (`ENERGY` / `RHYTHM` / `MOTION`) and a **Design Read**, so the output is alive and specific, not just "clean".
- A **Delivery Gate**: a PASS/FAIL report in four blocks, run before anything ships.
- **Additive skills**, one per concern, so an agent only loads what a task needs.

The core prevents slop but cannot invent direction. **Your** `DESIGN.md` supplies it. A sterile result means the direction was missing, not that the filter failed.

---

## Supported agents

| Agent | Skill folder | Entry pointer |
|---|---|---|
| Claude Code | `.claude/skills` | `CLAUDE.md` |
| Antigravity | `.agents/skills` | `AGENTS.md` |
| Codex | `.codex/skills` | `AGENTS.md` |
| OpenCode | `.opencode/skills` | `AGENTS.md` |
| Cursor | `.cursor/skills` | `AGENTS.md` |
| Gemini CLI | `.gemini/skills` | `GEMINI.md` |
| Hermes | `~/.hermes/skills` (global only) | `AGENTS.md` |

Every skill is a folder of the open Agent Skills standard (`<name>/SKILL.md`), so it drops into any agent that reads the standard.

---

## Install

Pick one of the paths below. **The skills directory (path 1)** is the fastest and is registered on skills.sh; **the picker (path 2)** is the only one that also writes the pointer that loads the filter into every session.

### 1. The skills directory (works now, recommended)

```bash
npx skills add muris11/anti-ai-slop
```

Add `--all` for every skill, `-g` for a global install, or `--skill <name>` for a single one. Run `--list` first to see what is available.

> `npx skills add` copies skill folders but does **not** write the agent entry pointer that loads the filter every session. If you used it, follow the note under path 2.

### 2. The interactive picker

One command, then choose which skills, where (project or global), and which agents:

```bash
npx anti-ai-slop
```

It shows the banner, lists the skills with the core locked on, asks where and which agents, then installs the folders and writes the pointer.

> **If you already used path 1** (the skills directory), run `npx anti-ai-slop`, choose the same skills and agent, and pick **Keep what is there** when it finds existing folders. That writes the pointer.

**Running from this repo instead:** `npm i` in the repo's `cli/` folder, then `npm run installer`.

### 3. The plugin (Claude Code)

Add the marketplace once, then install the plugin:

```text
/plugin marketplace add https://github.com/muris11/anti-ai-slop
/plugin install antislop@anti-ai-slop
```

### 4. The plugin (Antigravity)

The same repo is a full Antigravity plugin: a root `plugin.json`, all the skills registered as Antigravity skills, and a `rules/antislop.md` pointer that loads the filter into every session.

```bash
agy plugin install https://github.com/muris11/anti-ai-slop
```

### 5. Manual (single file, no packaging)

The core `antislop.md` alone is a complete filter you can paste into any chat window. Download it and tell your agent to read it:

```bash
curl -o antislop.md https://raw.githubusercontent.com/muris11/anti-ai-slop/main/antislop.md
```

Windows (PowerShell):

```powershell
Invoke-WebRequest -Uri https://raw.githubusercontent.com/muris11/anti-ai-slop/main/antislop.md -OutFile antislop.md
```

---

## Skills

| Skill | What it covers | Ships in |
|---|---|---|
| `antislop` | The core filter: rules, purpose test, Delivery Gate. Load always. | v2.1.0 |
| `antislop-master` | The P0–P6 master taxonomy: ~180 indicators across color, type, layout, components, copy, motion, UX states, authenticity, code, and platform. The canonical audit source. | v2.1.0 |
| `antislop-ui` | UI / visual: layout, color, components, decoration, motion, structure | v2.1.0 |
| `antislop-layout` | Layout & composition: hero, sections, symmetry, grids, spacing rhythm | v2.1.0 |
| `antislop-copywriting` | Copy & text: headlines, CTAs, tone, fake stats, anti-AI-writing patterns, markdown hygiene | v2.1.0 |
| `antislop-human` | Human: contrast (with the checker), keyboard, focus, states | v2.1.0 |
| `antislop-layoutmobile` | Mobile layout: responsive breakpoints, grids, overflow, tap targets, navigation | v2.1.0 |
| `antislop-mobile` | Mobile & native: reflow, no overflow, 44px targets, Flutter/native intent | v2.1.0 |
| `antislop-dashboard` | Dashboard / data: metric cards, charts, tables, complete states | v2.1.0 |
| `antislop-forms` | Forms & states: validation, empty/loading/error/offline, keyboard-reachable | v2.1.0 |
| `antislop-motion` | Motion: a UX reason, one focal animation, easing, reduced-motion | v2.1.0 |
| `antislop-nav` | Navigation & chrome: real IA, no dead links, honest footer | v2.1.0 |
| `antislop-authenticity` | Authenticity: no fake metrics, testimonials, logos, or claims | v2.1.0 |
| `antislop-designsystem` | Design-system consistency: real tokens, spacing scale, theme parity | v2.1.0 |
| `antislop-imagery` | Imagery & decoration: illustrations, backgrounds, icons, media tied to product | v2.1.0 |
| `antislop-code` | Code comments: remove generic AI-slop comments, keep the valuable ones, never touch the code | v2.1.0 |
| `slop` | One-shot loader that pulls in the whole anti-ai-slop family at once | v2.1.0 |

Pick what matches the work: the master for a broad audit, UI work → `antislop-ui`, layout → `antislop-layout`, copy → `antislop-copywriting`, people → `antislop-human`, mobile layout → `antislop-layoutmobile`, native/mobile → `antislop-mobile`, dashboards → `antislop-dashboard`, forms/states → `antislop-forms`, motion → `antislop-motion`, nav → `antislop-nav`, claims/evidence → `antislop-authenticity`, design systems → `antislop-designsystem`, visuals → `antislop-imagery`, code comments → `antislop-code`, more than one → install several, or none (the core alone is a complete filter).

---

## Usage modes

antislop is used one of two ways, chosen at the start of a session:

- **DURING** guides the work while it is built, ending with the Delivery Gate. Use it when building new UI.
- **AFTER** audits finished work: a numbered findings list, you approve which to fix, then a follow-up report. Use it to clean up existing output.

The core skill always asks: *"When does antislop apply: during the work, or after it is done?"* Answer before anything proceeds.

---

## Examples

**Build a new landing page (DURING):** load `antislop` + `antislop-ui` + `antislop-copywriting`. It applies the rules as you build and finishes with the Delivery Gate report.

**Audit an existing dashboard (AFTER):** load `antislop` + `antislop-ui` + `antislop-human`. It returns a numbered findings list; you approve which to fix, then it re-reports.

**Write a blog post (copy only):** load `antislop` + `antislop-copywriting`.

**Refactor comments in a repo (code only):** load `antislop` + `antislop-code`.

---

## FAQ

**Is antislop a style guide?** No — a filter. It does not prescribe colors, fonts, or layouts. It rejects technique without purpose and requires liveliness; direction is yours (your `DESIGN.md`).

**Which agents does it work with?** All of them, but the install paths differ:
- The picker and the skills directory support Claude Code, Codex, Antigravity, OpenCode, Cursor, Gemini CLI, and Hermes (Hermes installs globally only). These are the recommended paths.
- The plugins are per-agent doors: the Claude Code marketplace plugin and the Antigravity plugin, both installed from this repo.
- The single file (`antislop.md`) works with any agent that reads plain Markdown, including a plain chat window.

**What is a "skill"?** A folder that goes deeper into one concern (UI, copywriting, accessibility, and so on), holding a `SKILL.md` with its rules. It references the core rules by number and never duplicates them, so adding a skill does not change the core.

**What are DURING and AFTER?** The two usage modes: DURING applies the rules while building, AFTER audits finished work. You pick one at the start of a session.

---

## Contributing

Found a new AI slop pattern, a rule that missed something, or a bug in the installer? Open an issue. PRs are welcome for new AI slop patterns, clarifications, or checklist items out of sync with their rule.

## License

MIT — see [LICENSE](LICENSE).
