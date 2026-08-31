# anti-ai-slop

**License:** MIT | **Version:** v1.0.0

[![skills.sh](https://img.shields.io/badge/skills.sh-anti--slop-6366f1?style=flat-square&logo=github)](https://skills.sh)

> Anti Slop: Rules for AI Coding Agents. It stops them from generating generic "AI slop" UI and copy, without letting the result turn sterile. It is a filter, not a style guide: no prescribed colors, fonts, or layouts. It is not only for building pages: it also writes and audits copy, so AI text stops reading like AI. And it never beautifies on its own; DESIGN.md (yours) is where beauty and direction come from.

New here? [Start with the guide](#guide). It explains what antislop is and how to install it, from zero.

---

## Table of Contents

- [Guide](#guide)
  - [What It Does](#what-it-does)
  - [What It Is Not](#what-it-is-not)
  - [The 38 Rules](#the-38-rules)
  - [The Liveliness Toolkit](#the-liveliness-toolkit)
  - [Delivery Gate](#delivery-gate)
- [Install](#install)
  - [Path 1: The Picker (Recommended)](#path-1-the-picker-recommended)
  - [Path 2: The Skills Directory](#path-2-the-skills-directory)
  - [Path 3: The Plugin (Claude Code)](#path-3-the-plugin-claude-code)
  - [Path 4: The Plugin (Antigravity)](#path-4-the-plugin-antigravity)
  - [Manual Install](#manual-install-single-file-no-packaging)
  - [Which Agents Are Supported?](#which-agents-are-supported)
  - [OS Compatibility](#os-compatibility)
- [Skills](#skills)
- [Usage Modes](#usage-modes)
  - [Mode 1: During the Work](#mode-1-during-the-work)
  - [Mode 2: After the Work (Audit)](#mode-2-after-the-work-audit)
- [Examples](#examples)
  - [Before antislop](#before-antislop)
  - [After antislop](#after-antislop)
- [Roadmap](#roadmap)
- [FAQ](#faq)
- [Contributing](#contributing)
- [License](#license)

---

## Guide

### What It Does

- **38 mandatory rules** (R-01 to R-38) in three tiers: Hard Gate (absolute), Purpose-Gate (technique allowed, reason required), Quality Locks (consistency).
- A **Liveliness Toolkit** with three dials (ENERGY / RHYTHM / MOTION) and a Design Read, so the result is alive and specific, not just "clean".
- A **Delivery Gate**: a mandatory PASS/FAIL report in four blocks, run before anything ships.
- **Additive skills**, one per concern, so an agent only loads what a task needs.

The core prevents slop but cannot invent direction. DESIGN.md (yours) supplies it; a sterile result means the direction was missing, not that the filter failed (R-37).

### What It Is Not

- **Not a style guide.** It does not prescribe colors, fonts, layouts, or "house styles."
- **Not a ban list.** It does not ban gradients, glassmorphism, badges, or card grids. Those are tools. What it rejects is **technique without purpose**.
- **Not a design system.** You still need your own `DESIGN.md` with brand identity, palette, typography, and mood.
- **Not a beauty filter.** It removes slop but cannot add energy. Liveliness must be added deliberately (see [The Liveliness Toolkit](#the-liveliness-toolkit)).

### The 38 Rules

All rules are grouped into three tiers. **Hard Gate** rules are absolute. **Purpose-Gate** rules allow the technique but require a written reason. **Quality Locks** are consistency requirements.

#### Group 1: Hard Gate

These rules protect honesty, function, and accessibility. Breaking any of them is a FAIL regardless of purpose.

| Rule | Concern | Summary |
|------|---------|---------|
| R-02 | Copywriting | No em dash (`—`). Use comma, period, colon, or parentheses. |
| R-03 | Mobile | Mobile layout must be perfect. No overflow, no clipping, no broken navbar. |
| R-17 | Data | No numbers without a real source. Empty is better than deceptive. |
| R-18 | Testimonials | No AI avatars, random names, or fictional reviews. |
| R-23 | Assets | Before creating assets without instructions, ask or use a clear placeholder. |
| R-24 | Navigation | No links to sections that do not exist. |
| R-25 | Contrast | All text meets WCAG AA (4.5:1 normal, 3:1 large). |
| R-26 | Interactivity | Every button and link has real behavior, or it is removed. |
| R-27 | UI States | Every data view has empty, loading, and error states. |
| R-28 | FAQ | No generic template questions. Every question must be product-specific. |
| R-32 | Keyboard | All interactive elements reachable by keyboard. Visible focus indicators. |
| R-33 | Patching | No external scripts rewriting source/CSS. Build features in source. |
| R-34 | Themes | If you ship a toggle, both modes must fully work. |
| R-35 | Verify | Run the app before declaring done. Check console, themes, breakpoints. |
| R-36 | Claims | No fabricated security, compliance, or performance claims. |
| R-37 | Direction | Load style direction before building. Label drafts without direction. |
| R-38 | Content | Real content or honest placeholder. No fabricated realistic content. |

#### Group 2: Purpose-Gate

Each technique is allowed. It FAILS only when it appears as a default without a stated purpose.

| Rule | Concern | Summary |
|------|---------|---------|
| R-01 | Color | No default blue-purple gradients. Allowed with written brand purpose. |
| R-04 | Icons | No generic sparkle/star/magic icons. Allowed with relevance written down. |
| R-06 | Typography | No monospace-for-aesthetic. Choose typeface for brand character. |
| R-07 | Background | No grid/blueprint/dot patterns. Allowed with identity purpose. |
| R-08 | Arrows | No arrows on every button. Allowed with proportional, written purpose. |
| R-09 | Badges | No "AI Powered" pills. Allowed only when functionally needed. |
| R-10 | Glassmorphism | Max 1-2 elements with blur. Forbidden on navbar+card+modal+sidebar. |
| R-12 | Shadow | Use as elevation marker, not default for every component. |
| R-13 | Glow | Max 1-2 elements. Forbidden on cards+buttons+badges+icons+background. |
| R-14 | Feature Cards | No identical cards. Variation reflecting content hierarchy. |
| R-19 | Animations | Motion must have clear UX purpose. Match the declared MOTION dial. |
| R-22 | Illustrations | No generic Undraw/Storyset. Must connect to the product. |

#### Group 3: Quality Locks

Consistency requirements.

| Rule | Concern | Summary |
|------|---------|---------|
| R-05 | Layout | No AI template layouts. Build around actual content needs. |
| R-11 | Border Radius | No universal pill shapes. Radius is a hierarchy tool. |
| R-15 | CTAs | No "Get Started" / "Learn More" / "Try Now". Be specific to the action. |
| R-16 | Buzzwords | No "AI Powered" / "Revolutionary" / "Seamless". Use specific language. |
| R-20 | Visual Identity | Design must have its own identity. Swap the logo and it should look different. |
| R-21 | Dark Mode | Choose theme from brand identity, not "dark looks tech". |
| R-29 | Palette | Max 2-3 core colors + 1 accent. |
| R-30 | No Cloning | Do not mimic Linear/Vercel/Stripe/Notion unless asked. |
| R-31 | Write Reasons | Every major decision gets a one-line reason. The keystone rule. |

### The Liveliness Toolkit

A filter can remove slop, but it cannot add energy. Liveliness must be **added** deliberately.

#### Three Dials

Every design must set three dials:

| Dial | 1 (Calm) | 2 (Balanced) | 3 (Bold) |
|------|----------|--------------|----------|
| **ENERGY** | Linear, GOV.UK | Stripe, Vercel | Awwwards, agency portfolio |
| **RHYTHM** | Uniform grid, predictable | Consistent with a few breaks | Asymmetric, mixed compositions |
| **MOTION** | Hover states only | Scroll-reveal, transitions | Parallax, pin, choreography |

**Example sets:**
- Designer portfolio: ENERGY 3, RHYTHM 3, MOTION 2
- Public service site: ENERGY 1, RHYTHM 1, MOTION 1
- SaaS landing for developers: ENERGY 1, RHYTHM 2, MOTION 1

#### Design Read

Before generating, declare one line:

> Reading this as: `<page kind>` for `<audience>`, in a `<visual language>` style, dial `<ENERGY/RHYTHM/MOTION>`.

Example: *"Reading this as: B2B SaaS landing for technical buyers, with a Linear-style minimalist language, dial ENERGY 1 / RHYTHM 2 / MOTION 1."*

### Delivery Gate

Run this gate BEFORE delivering. If any item is FAIL, fix it first, then re-run.

#### Block 1: Hard Gate

All answers must be **no**:

- [ ] Em dash in text? (R-02)
- [ ] Mobile overflow or broken layout? (R-03)
- [ ] Statistics without a source? (R-17)
- [ ] Fictional testimonials? (R-18)
- [ ] Assets created without confirmation? (R-23)
- [ ] Dead navigation links? (R-24)
- [ ] Text below WCAG AA contrast? (R-25)
- [ ] Buttons that do nothing? (R-26)
- [ ] Missing empty/loading/error states? (R-27)
- [ ] Generic FAQ? (R-28)
- [ ] Not keyboard navigable? (R-32)
- [ ] Features added via patching scripts? (R-33)
- [ ] Broken theme mode? (R-34)
- [ ] App not run before delivery? (R-35)
- [ ] Fabricated claims? (R-36)
- [ ] Built without direction, not labeled draft? (R-37)
- [ ] Fabricated realistic content? (R-38)

#### Block 2: Purpose-Gate

All answers must be **no**:

- [ ] Default gradients with no brand purpose? (R-01)
- [ ] Generic icons with no relevance? (R-04)
- [ ] Monospace-for-aesthetic typography? (R-06)
- [ ] Grid/blueprint backgrounds without identity purpose? (R-07)
- [ ] Decorative arrows on buttons? (R-08)
- [ ] Capsule badges without function? (R-09)
- [ ] Glassmorphism on 3+ elements? (R-10)
- [ ] Shadows on every component? (R-12)
- [ ] Glow on everything? (R-13)
- [ ] Identical feature cards? (R-14)
- [ ] Template animations with no UX purpose? (R-19)
- [ ] Generic illustrations? (R-22)

#### Block 3: Liveliness

All answers must be **yes**:

- [ ] Dials set and explicit?
- [ ] Output consistent with claimed dials?
- [ ] At least one clear focal point per screen?
- [ ] Whitespace structural, not leftover?
- [ ] One deliberate accent (not zero, not everywhere)?
- [ ] Identity motif present?
- [ ] Design Read declared?

#### Block 4: Craftsmanship

All answers must be **no**:

- [ ] Any decision justified only by "AI default"? (C-1)
- [ ] Non-functional interactive elements? (C-2)
- [ ] Sections that only fill a template? (C-3)
- [ ] UI broken in any state/theme/breakpoint? (C-4)
- [ ] Fabricated testimonials/claims? (C-5)
- [ ] AI template layout? (R-05)
- [ ] Universal pill shapes? (R-11)
- [ ] Generic CTAs? (R-15)
- [ ] AI buzzwords? (R-16)
- [ ] Generic visual identity? (R-20)
- [ ] Forced dark mode without reason? (R-21)
- [ ] Palette exceeds 2-3 core + 1 accent? (R-29)
- [ ] Clone of another product? (R-30)
- [ ] Unexplainable major decisions? (R-31)

---

## Install

antislop is a set of standard agent skills (one folder per skill, SKILL.md) you can install as a package. The core is always loaded; the skills load only for the task at hand. Pick one of these paths.

### Path 1: The Picker (Recommended)

One command, then choose. It shows the antislop banner, lists the skills with the core locked on, asks where (project or global) and which agents (Claude Code, Antigravity, Codex, OpenCode, Cursor, Gemini CLI, Hermes), then installs the folders and writes the pointer that loads antislop every session. The skills directory (path 2) does not write that pointer, so this is the one to use:

```bash
npx antislop-ai
```

### Path 2: The Skills Directory

antislop is listed on [skills.sh](https://skills.sh), the open directory for agent skills:

```bash
npx skills add muris11/anti-ai-slop
```

Add `--all` for every skill, `-g` for a global install, or `--skill <name>` for a single one. Run `--list` first to see what is available.

> **Note:** `npx skills add` copies the skill folders but does not write the agent entry pointer that loads antislop every session; skills.sh does not write them, so that gap is theirs, not antislop's. That is why the picker (path 1) is the recommended way to install. If you already used path 2, run `npx antislop-ai`, choose the same skills and agent, and pick **Keep what is there** when it finds the existing folders; that writes the pointer.

skills.sh reads the skill folders straight from this repository, so the listing appears as soon as the repo is live; there is no separate setup step.

### Path 3: The Plugin (Claude Code)

Add the marketplace once, then install the plugin:

```bash
/plugin marketplace add https://github.com/muris11/anti-ai-slop
/plugin install antislop@anti-ai-slop
```

### Path 4: The Plugin (Antigravity)

The same repo is a full Antigravity plugin: a root `plugin.json`, the six skills registered as Antigravity skills, and a `rules/antislop.md` pointer that loads antislop into every session. Install it with the Antigravity CLI:

```bash
agy plugin install https://github.com/muris11/anti-ai-slop
```

### Manual Install (Single File, No Packaging)

The core `antislop.md` alone remains a complete filter you can paste into any chat window. Download it and tell your agent to read it; the First-Run wizard inside it installs skills the manual way:

```bash
# macOS / Linux
curl -o antislop.md https://raw.githubusercontent.com/muris11/anti-ai-slop/main/antislop.md

# Windows (PowerShell)
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/muris11/anti-ai-slop/main/antislop.md" -OutFile "antislop.md"
```

### Which Agents Are Supported?

Every skill is a folder of the open Agent Skills standard (`<name>/SKILL.md`), so it drops into any agent that reads the standard:

| Agent | Skill Folder | Picker | Plugin |
|-------|-------------|--------|--------|
| Claude Code | `.claude/skills/` | Yes | Yes (marketplace) |
| Antigravity | `.agents/skills/` | Yes | Yes (`agy plugin`) |
| Codex | `.codex/skills/` | Yes | No |
| OpenCode | `.opencode/skills/` | Yes | No |
| Cursor | `.cursor/skills/` | Yes | No |
| Gemini CLI | `.gemini/skills/` | Yes | No |
| Hermes | `~/.hermes/skills/` | Yes (global only) | No |

The picker (path 1) asks which of these agents you use and installs into them, creating the skill folder if it does not exist yet; the skills directory (path 2) handles the same agents and more. The plugins are per-agent doors: path 3 is the Claude Code marketplace plugin, path 4 the Antigravity plugin.

### OS Compatibility

antislop works on **Windows**, **macOS**, and **Linux**. All installation paths are cross-platform:

| Method | Windows | macOS | Linux |
|--------|---------|-------|-------|
| Picker (`npx antislop-ai`) | Yes | Yes | Yes |
| Skills dir (`npx skills add`) | Yes | Yes | Yes |
| Plugin (Claude Code) | Yes | Yes | Yes |
| Plugin (Antigravity) | Yes | Yes | Yes |
| Manual (`curl` / `Invoke-WebRequest`) | Yes | Yes | Yes |

**Requirements:** Node.js 18+ (for `npx`), Git. The contrast-check script requires Python 3.8+ (optional, for `antislop-human`).

---

## Skills

| Skill | What It Covers | Ships In |
|-------|---------------|----------|
| **antislop** | The core filter: rules, tiers, Delivery Gate, liveliness | v1.0.0 |
| **antislop-ui** | UI / visual: layout, color, components, decoration, motion, structure | v1.0.0 |
| **antislop-copywriting** | Copy & text: headlines, CTAs, tone, fake stats, anti-AI-writing patterns, markdown hygiene | v1.0.0 |
| **antislop-human** | Human: contrast (with the checker), keyboard, focus, states | v1.0.0 |
| **antislop-layoutmobile** | Mobile layout: responsive breakpoints, grids, overflow, tap targets, navigation | v1.0.0 |
| **antislop-code** | Code comments: remove generic AI-slop comments, keep the valuable ones, never touch the code | v1.0.0 |
| **slop** | One-shot loader that pulls in the whole antislop family (core + all skills) at once | v1.0.0 |

Pick what matches the work:
- **UI work** -> `antislop-ui`
- **Copy work** -> `antislop-copywriting`
- **People/accessibility work** -> `antislop-human`
- **Mobile layout work** -> `antislop-layoutmobile`
- **Code comments work** -> `antislop-code`
- **More than one** -> install several
- **None** -> the core alone is a complete filter

### Skill Details

#### antislop (Core)

The foundation. Always loaded. Contains:
- All 38 rules (R-01 to R-38) in three tiers
- The Liveliness Toolkit (three dials + Design Read)
- The Delivery Gate (four-block PASS/FAIL checklist)
- First-Run Install Wizard

#### antislop-ui

Cleans AI-generated UI. Covers:
- Color/gradient defaults (R-01): blue-purple gradients, harsh gradients, purple-and-black, neon, pastel, radial orbs
- Glassmorphism (R-10): blur on navbar+card+modal+sidebar
- Border radius (R-11): universal pill shapes
- Shadows (R-12): default elevation on everything
- Glow (R-13): neon glow on everything
- Background grids (R-07): dot grids, blueprint patterns
- Dark mode (R-21): forced dark without reason
- Palette (R-29): exceeding 2-3 core + 1 accent
- Icons (R-04): Lucide-style generic icons
- Typography (R-06): monospace-for-aesthetic, Geist Mono and friends
- Badges (R-09): capsule badges, colored left stripes
- Animations (R-19): template motion with no UX purpose
- Layout (R-05): bento grids, AI template layouts, fake terminal windows, demos without a product
- Dashboard patterns, charts, tables, motion

#### antislop-copywriting

Cleans AI-generated prose. Covers:
- Empty AI vocabulary: unlock, elevate, empower, delve, harness, seamlessly
- Em dashes (R-02)
- Significance inflation
- Empty claims
- Weasel attributions ("many say", "experts agree")
- Chatbot closers
- Fake-candid openers
- Rule-of-three overuse
- Fabricated specifics
- Generic CTAs (R-15)
- AI buzzwords (R-16)
- Preserves: specific details, mixed feelings, dated references, sentence variety, genuine asides

#### antislop-human

Ensures accessibility. Covers:
- WCAG AA contrast: 4.5:1 normal text, 3:1 large text, 3:1 non-text
- Keyboard navigation (R-32): all interactive elements reachable
- Focus indicators: visible on every interactive element
- UI states (R-27): empty, loading, error states for every data view
- Zoom compatibility
- Mobile keyboard handling
- Provides: `contrast-check.py` script, formula, reference table

#### antislop-layoutmobile

Ensures mobile responsiveness. Covers:
- Layout reflows into a distinct mobile state
- Sizes use mobile scale
- Grids collapse and stack
- No horizontal overflow (R-03)
- Tap targets 44x44px
- Hover interactions have tap equivalents
- Navigation reflows
- Fixed bars respect content

#### antislop-code

Cleans AI-generated code comments. Covers:
- Removes: decorative separators (`// =====`), restating-the-obvious comments, workflow narration (`// Step 1:`), empty labels (`// Main logic`), vague TODOs, signature echo, decorative emoji, end markers
- Preserves: business logic, architectural decisions, security considerations, performance trade-offs, edge cases, API contracts, workarounds
- Never touches the code itself

---

## Usage Modes

antislop is used one of two ways, chosen at the start of a session:

### Mode 1: During the Work

**Best for:** new projects, building from scratch, adding features.

The agent follows all rules while generating. Every visual decision gets a purpose test. Every design gets a liveliness check. The session ends with a Delivery Gate report.

**How it works:**
1. Agent asks: "When do you want to use antislop?" You answer: "During."
2. Agent loads the core + relevant skills.
3. Agent builds, applying rules in real-time.
4. Agent runs Delivery Gate before declaring done.
5. Agent reports PASS/FAIL. If FAIL, agent fixes and re-runs.

### Mode 2: After the Work (Audit)

**Best for:** reviewing existing code, pre-launch checks, finding problems.

The agent produces a numbered findings list in `anti-slop/audit-001-YYYY-MM-DD.md` (numbers keep rising). Each finding cites the violated rule (R-XX) and a one-line reason.

- **HIGH priority**: Hard Gate violations (honesty, function, accessibility)
- **MEDIUM priority**: Purpose-Gate violations (technique without purpose)
- **LOW priority**: Quality Lock violations (consistency)

The agent does not modify anything until you approve specific numbers. Numbers not mentioned are not touched. After approval, the agent fixes the items and writes a follow-up report.

**How it works:**
1. Agent asks: "When do you want to use antislop?" You answer: "After."
2. Agent loads the core + relevant skills.
3. Agent audits the existing work.
4. Agent produces a numbered findings list with priorities.
5. You approve specific numbers to fix.
6. Agent fixes approved items and writes a follow-up report.

---

## Examples

### Before antislop

```html
<section class="bg-gradient-to-br from-blue-600 via-purple-500 to-pink-500">
  <div class="flex flex-col items-center text-center">
    <span class="inline-flex items-center px-3 py-1 text-xs font-semibold rounded-full bg-white/20 text-white">
      <Sparkles class="w-3 h-3 mr-1" /> AI Powered
    </span>
    <h1 class="text-4xl md:text-6xl font-bold text-white mt-4">
      Unlock the Power of Seamless Collaboration
    </h1>
    <p class="text-white/80 mt-4 max-w-xl">
      Empower your team to elevate their journey to the next level.
    </p>
    <button class="mt-6 px-6 py-3 rounded-full bg-white text-purple-600 font-semibold">
      Get Started <ArrowRight class="w-4 h-4 ml-1" />
    </button>
  </div>
</section>
```

**Problems:**
- Blue-purple gradient (R-01) - default without brand purpose
- "AI Powered" badge (R-09) - capsule without function
- Sparkle icon (R-04) - generic, no relevance
- "Unlock the Power" (R-16) - AI buzzword
- "Seamless Collaboration" (R-16) - empty claim
- "Get Started" (R-15) - generic CTA
- Arrow decoration (R-08) - decorative, no purpose
- Pill button (R-11) - universal pill shape
- No purpose written for any element (R-31)

### After antislop

```html
<section style="background-color: #0f172a; padding: 80px 24px;">
  <div style="max-width: 640px; margin: 0 auto;">
    <h1 style="color: #f8fafc; font-size: 36px; line-height: 1.2;">
      Your team shares files. This tool keeps them from getting lost.
    </h1>
    <p style="color: #94a3b8; margin-top: 16px; font-size: 18px;">
      Every file lives in one place. Search works. Nothing falls through the cracks.
    </p>
    <a href="#signup" style="display: inline-block; margin-top: 24px; padding: 12px 24px; background-color: #22c55e; color: #ffffff; font-weight: 600; text-decoration: none;">
      Create your free workspace
    </a>
  </div>
</section>
```

**Improvements:**
- Specific product copy, no buzzwords
- No gradient (R-01) - background is purposeful
- No badge (R-09) - removed
- No icon (R-04) - removed
- CTA specific to the action (R-15) - "Create your free workspace"
- Rectangular button (R-11) - design system, not pill
- Purpose for every element (R-31) - each serves a function

---

## Roadmap

| Version | Changes |
|---------|---------|
| v1.0.0 | Initial public release. Ships the core filter (R-01 → R-38), the Liveliness Toolkit, and the Delivery Gate, plus six additive skills (UI, copywriting, human, layout-mobile, code, and the `slop` loader). Ships packaging for all install paths: the npm picker, the skills directory, the Claude Code marketplace plugin, the Antigravity plugin, and the single-file manual path. |

See [ROADMAP.md](ROADMAP.md) for the full tracker, including the cross-agent plugin plan.

---

## FAQ

### Is antislop a style guide?

No, a filter. It does not prescribe colors, fonts, or layouts. It rejects technique without purpose and requires liveliness; direction is yours.

### Which agents does it work with?

All of them, but the install paths differ:

- **The picker and the skills directory** support Claude Code, Codex, Antigravity, OpenCode, Cursor, Gemini CLI, and Hermes (the picker detects each agent's skill folder; Hermes installs globally only). These are the recommended paths.
- **The plugins** are per-agent doors: the Claude Code marketplace plugin (path 3) and the Antigravity plugin (path 4), both installed from the same repo.
- **The single file** (`antislop.md`) works with any agent that reads plain Markdown, including a plain chat window.

The packaged skills use the open Agent Skills standard (folder per skill), so they drop into any tool that reads the standard.

### What is a "skill"?

A folder that goes deeper into one concern (UI, copywriting, accessibility, and so on), holding a `SKILL.md` with its rules. It references the core rules by number and never duplicates them, so adding a skill does not change the core.

### What are DURING and AFTER?

The two usage modes: DURING applies the rules while building, AFTER audits finished work. You pick one at the start of a session.

### Do I need DESIGN.md?

Yes. antislop is a filter, not a direction provider. Without `DESIGN.md`, the filter can remove slop but the result may be sterile. `DESIGN.md` supplies brand identity, palette, typography, and mood. A sterile result means the direction was missing, not that the filter failed (R-37).

### What if I only use the core, without any skills?

The core alone is a complete filter. It has all 38 rules, the Liveliness Toolkit, and the Delivery Gate. The skills go deeper into specific concerns but are not required.

### Can I install only one skill?

Yes. Use `npx skills add muris11/anti-ai-slop --skill antislop-ui` to install a single skill. The core is always included.

### Does it work with non-UI projects?

Yes. The `antislop-code` skill cleans code comments. The `antislop-copywriting` skill cleans prose. The core rules apply to any AI-generated content, not just UI.

---

## Contributing

Found a new AI slop pattern, a rule that missed something, or a bug in the installer? Open an issue. PRs are welcome for:

- New AI slop patterns
- Clarifications
- Checklist items out of sync with their rule

Before submitting:

1. Read the core rules
2. Run the Delivery Gate on your changes
3. Write a one-line reason for every rule you add or modify (R-31)

---

## License

MIT. Do whatever you want with it.

---

---

# Versi Bahasa Indonesia

> Aturan Anti Slop untuk AI Coding Agent. Menghentikan AI menghasilkan UI dan teks yang generik dan "slop", tanpa membuat hasilnya jadi kaku. Ini adalah filter, bukan style guide: tidak ada warna, font, atau layout yang ditentukan. Tidak hanya untuk membangun halaman: juga menulis dan mengaudit teks, sehingga teks AI tidak terbaca seperti AI. Dan tidak pernah mempercantik sendiri; DESIGN.md (milikmu) adalah sumber keindahan dan arah.

Baru di sini? [Mulai dari panduan](#panduan). Penjelasan lengkap tentang apa itu antislop dan cara menginstalnya dari nol.

---

## Daftar Isi

- [Panduan](#panduan)
  - [Apa yang Dilakukan](#apa-yang-dilakukan)
  - [Bukan Apa](#bukan-apa)
  - [38 Aturan](#38-aturan)
  - [Toolkit Kehidupan](#toolkit-kehidupan)
  - [Delivery Gate](#delivery-gate-1)
- [Instalasi](#instalasi)
  - [Jalur 1: Picker (Disarankan)](#jalur-1-picker-disarankan)
  - [Jalur 2: Skills Directory](#jalur-2-skills-directory)
  - [Jalur 3: Plugin (Claude Code)](#jalur-3-plugin-claude-code)
  - [Jalur 4: Plugin (Antigravity)](#jalur-4-plugin-antigravity)
  - [Instalasi Manual](#instalasi-manual-single-file-tanpa-packaging)
  - [Agent yang Didukung](#agent-yang-didukung)
  - [Kompatibilitas OS](#kompatibilitas-os)
- [Skills](#skills-1)
- [Mode Penggunaan](#mode-penggunaan)
  - [Mode 1: Selama Pekerjaan](#mode-1-selama-pekerjaan)
  - [Mode 2: Setelah Pekerjaan (Audit)](#mode-2-setelah-pekerjaan-audit)
- [Contoh](#contoh)
  - [Sebelum antislop](#sebelum-antislop)
  - [Sesudah antislop](#sesudah-antislop)
- [Roadmap](#roadmap-1)
- [FAQ](#faq-1)
- [Kontribusi](#kontribusi)
- [Lisensi](#lisensi)

---

## Panduan

### Apa yang Dilakukan

- **38 aturan wajib** (R-01 sampai R-38) dalam tiga tier: Hard Gate (absolut), Purpose-Gate (teknik diizinkan, alasan wajib), Quality Locks (konsistensi).
- **Toolkit Kehidupan** dengan tiga dial (ENERGY / RHYTHM / MOTION) dan Design Read, sehingga hasilnya hidup dan spesifik, bukan sekadar "bersih".
- **Delivery Gate**: laporan PASS/FAIL wajib dalam empat blok, dijalankan sebelum sesuatu dirilis.
- **Skill tambahan**, satu per concern, sehingga agent hanya memuat yang dibutuhkan oleh tugas.

Core mencegah slop tapi tidak bisa menciptakan arah. DESIGN.md (milikmu) menyediakannya; hasil yang kaku berarti arahnya tidak ada, bukan filternya gagal (R-37).

### Bukan Apa

- **Bukan style guide.** Tidak menentukan warna, font, layout, atau "gaya rumah".
- **Bukan daftar larangan.** Tidak melarang gradient, glassmorphism, badge, atau card grid. Itu adalah alat. Yang ditolak adalah **teknik tanpa tujuan**.
- **Bukan design system.** Kamu masih butuh `DESIGN.md` sendiri dengan identitas brand, palet, tipografi, dan mood.
- **Bukan filter kecantikan.** Menghapus slop tapi tidak bisa menambah energi. Kehidupan harus ditambahkan secara sadar (lihat [Toolkit Kehidupan](#toolkit-kehidupan)).

### 38 Aturan

Semua aturan dikelompokkan dalam tiga tier. Aturan **Hard Gate** bersifat absolut. **Purpose-Gate** mengizinkan teknik tapi membutuhkan alasan tertulis. **Quality Locks** adalah persyaratan konsistensi.

#### Grup 1: Hard Gate

Aturan ini melindungi kejujuran, fungsi, dan aksesibilitas. Melanggar salah satunya = FAIL terlepas dari tujuan.

| Aturan | Concern | Ringkasan |
|--------|---------|-----------|
| R-02 | Copywriting | Tidak pakai em dash (`—`). Gunakan koma, titik, titik dua, atau kurung. |
| R-03 | Mobile | Layout mobile harus sempurna. Tidak ada overflow, clipping, atau navbar rusak. |
| R-17 | Data | Tidak ada angka tanpa sumber nyata. Kosong lebih baik dari menipu. |
| R-18 | Testimonial | Tidak ada avatar AI, nama acak, atau review fiksi. |
| R-23 | Aset | Sebelum membuat aset tanpa instruksi, tanya atau gunakan placeholder jelas. |
| R-24 | Navigasi | Tidak ada link ke section yang tidak ada. |
| R-25 | Kontras | Semua teks memenuhi WCAG AA (4.5:1 normal, 3:1 besar). |
| R-26 | Interaktivitas | Setiap tombol dan link punya perilaku nyata, atau dihapus. |
| R-27 | State UI | Setiap tampilan data punya state kosong, loading, dan error. |
| R-28 | FAQ | Tidak ada pertanyaan template generik. Setiap pertanyaan harus spesifik produk. |
| R-32 | Keyboard | Semua elemen interaktif bisa diakses keyboard. Indikator fokus terlihat. |
| R-33 | Patching | Tidak ada script eksternal yang menimpa source/CSS. Bangun fitur di source. |
| R-34 | Tema | Kalau ada toggle, kedua mode harus berfungsi penuh. |
| R-35 | Verifikasi | Jalankan aplikasi sebelum deklarasi selesai. Cek console, tema, breakpoint. |
| R-36 | Klaim | Tidak ada klaim keamanan, compliance, atau performa yang dibuat-buat. |
| R-37 | Arah | Muat arah style sebelum membangun. Label draft tanpa arah. |
| R-38 | Konten | Konten nyata atau placeholder jujur. Tidak ada konten realistis yang dibuat-buat. |

#### Grup 2: Purpose-Gate

Setiap teknik diizinkan. GAGAL hanya kalau muncul sebagai default tanpa tujuan tertulis.

| Aturan | Concern | Ringkasan |
|--------|---------|-----------|
| R-01 | Warna | Tidak ada gradient biru-ungu default. Diizinkan dengan tujuan brand tertulis. |
| R-04 | Ikon | Tidak ada ikon sparkle/star/magic generik. Diizinkan dengan relevansi tertulis. |
| R-06 | Tipografi | Tidak ada monospace-untuk-estetika. Pilih typeface untuk karakter brand. |
| R-07 | Background | Tidak ada pola grid/blueprint/dot. Diizinkan dengan tujuan identitas. |
| R-08 | Panah | Tidak ada panah di setiap tombol. Diizinkan dengan tujuan proporsional tertulis. |
| R-09 | Badge | Tidak ada pill "AI Powered". Diizinkan hanya kalau dibutuhkan secara fungsional. |
| R-10 | Glassmorphism | Maks 1-2 elemen dengan blur. Dilarang di navbar+card+modal+sidebar. |
| R-12 | Bayangan | Gunakan sebagai penanda elevasi, bukan default untuk semua komponen. |
| R-13 | Glow | Maks 1-2 elemen. Dilarang di cards+buttons+badges+icons+background. |
| R-14 | Feature Cards | Tidak ada card identik. Variasi mencerminkan hierarki konten. |
| R-19 | Animasi | Motion harus punya tujuan UX jelas. Sesuaikan dengan dial MOTION yang dideklarasikan. |
| R-22 | Ilustrasi | Tidak ada Undraw/Storyset generik. Harus terhubung ke produk. |

#### Grup 3: Quality Locks

Persyaratan konsistensi.

| Aturan | Concern | Ringkasan |
|--------|---------|-----------|
| R-05 | Layout | Tidak ada layout template AI. Bangun sesuai kebutuhan konten aktual. |
| R-11 | Border Radius | Tidak ada bentuk pill universal. Radius adalah alat hierarki. |
| R-15 | CTA | Tidak ada "Get Started" / "Learn More" / "Try Now". Spesifik sesuai aksi. |
| R-16 | Buzzwords | Tidak ada "AI Powered" / "Revolutionary" / "Seamless". Gunakan bahasa spesifik. |
| R-20 | Identitas Visual | Desain harus punya identitas sendiri. Tukar logo dan seharusnya terlihat beda. |
| R-21 | Dark Mode | Pilih tema dari identitas brand, bukan "dark keliatan tech". |
| R-29 | Palet | Maks 2-3 warna inti + 1 aksen. |
| R-30 | Tidak cloning | Jangan tiru Linear/Vercel/Stripe/Notion kecuali diminta. |
| R-31 | Tulis Alasan | Setiap keputusan besar dapat satu baris alasan. Aturan batu kunci. |

### Toolkit Kehidupan

Filter bisa menghapus slop, tapi tidak bisa menambah energi. Kehidupan harus **ditambahkan** secara sadar.

#### Tiga Dial

Setiap desain harus menetapkan tiga dial:

| Dial | 1 (Tenang) | 2 (Seimbang) | 3 (Bold) |
|------|-----------|-------------|----------|
| **ENERGY** | Linear, GOV.UK | Stripe, Vercel | Awwwards, portofolio agency |
| **RHYTHM** | Grid seragam, prediktabel | Konsisten dengan beberapa jeda | Asimetris, komposisi campuran |
| **MOTION** | State hover saja | Scroll-reveal, transisi | Parallax, pin, koreografi |

**Contoh set:**
- Portofolio desainer: ENERGY 3, RHYTHM 3, MOTION 2
- Situs layanan publik: ENERGY 1, RHYTHM 1, MOTION 1
- Landing SaaS untuk developer: ENERGY 1, RHYTHM 2, MOTION 1

#### Design Read

Sebelum generate, deklarasikan satu baris:

> Reading this as: `<jenis halaman>` untuk `<audiens>`, dalam gaya `<visual language>`, dial `<ENERGY/RHYTHM/MOTION>`.

Contoh: *"Reading this as: B2B SaaS landing untuk pembeli teknis, dengan gaya minimalis Linear-style, dial ENERGY 1 / RHYTHM 2 / MOTION 1."*

### Delivery Gate

Jalankan gate INI SEBELUM mengirim. Kalau ada item FAIL, perbaiki dulu, lalu jalankan ulang.

#### Blok 1: Hard Gate

Semua jawaban harus **tidak**:

- [ ] Ada em dash di teks? (R-02)
- [ ] Overflow mobile atau layout rusak? (R-03)
- [ ] Statistik tanpa sumber? (R-17)
- [ ] Testimonial fiksi? (R-18)
- [ ] Aset dibuat tanpa konfirmasi? (R-23)
- [ ] Link navigasi mati? (R-24)
- [ ] Teks di bawah kontras WCAG AA? (R-25)
- [ ] Tombol yang tidak berfungsi? (R-26)
- [ ] State kosong/loading/error tidak ada? (R-27)
- [ ] FAQ generik? (R-28)
- [ ] Tidak bisa navigasi keyboard? (R-32)
- [ ] Fitur ditambahkan via patching script? (R-33)
- [ ] Mode tema rusak? (R-34)
- [ ] Aplikasi tidak dijalankan sebelum pengiriman? (R-35)
- [ ] Klaim dibuat-buat? (R-36)
- [ ] Dibangun tanpa arah, tidak dilabeli draft? (R-37)
- [ ] Konten realistis dibuat-buat? (R-38)

#### Blok 2: Purpose-Gate

Semua jawaban harus **tidak**:

- [ ] Gradient default tanpa tujuan brand? (R-01)
- [ ] Ikon generik tanpa relevansi? (R-04)
- [ ] Tipografi monospace-untuk-estetika? (R-06)
- [ ] Background grid/blueprint tanpa tujuan identitas? (R-07)
- [ ] Panah dekoratif di tombol? (R-08)
- [ ] Badge kapsul tanpa fungsi? (R-09)
- [ ] Glassmorphism di 3+ elemen? (R-10)
- [ ] Bayangan di semua komponen? (R-12)
- [ ] Glow di mana-mana? (R-13)
- [ ] Feature card identik? (R-14)
- [ ] Animasi template tanpa tujuan UX? (R-19)
- [ ] Ilustrasi generik? (R-22)

#### Blok 3: Kehidupan

Semua jawaban harus **ya**:

- [ ] Dial ditetapkan dan eksplisit?
- [ ] Output konsisten dengan dial yang diklaim?
- [ ] Setidaknya satu titik fokus jelas per layar?
- [ ] Whitespace struktural, bukan sisa?
- [ ] Satu aksen yang disengaja (bukan nol, bukan di mana-mana)?
- [ ] Motif identitas ada?
- [ ] Design Read dideklarasikan?

#### Blok 4: Craftsmanship

Semua jawaban harus **tidak**:

- [ ] Ada keputusan yang alasan hanya "AI default"? (C-1)
- [ ] Elemen interaktif tidak berfungsi? (C-2)
- [ ] Section yang hanya mengisi template? (C-3)
- [ ] UI rusak di state/theme/breakpoint tertentu? (C-4)
- [ ] Testimonial/klaim dibuat-buat? (C-5)
- [ ] Layout template AI? (R-05)
- [ ] Bentuk pill universal? (R-11)
- [ ] CTA generik? (R-15)
- [ ] Buzzword AI? (R-16)
- [ ] Identitas visual generik? (R-20)
- [ ] Dark mode dipaksakan tanpa alasan? (R-21)
- [ ] Palet melebihi 2-3 inti + 1 aksen? (R-29)
- [ ] Clone produk lain? (R-30)
- [ ] Keputusan besar tidak bisa dijelaskan? (R-31)

---

## Instalasi

antislop adalah kumpulan skill agent standar (satu folder per skill, SKILL.md) yang bisa diinstal sebagai paket. Core selalu dimuat; skill hanya dimuat untuk tugas yang sedang dikerjakan. Pilih salah satu jalur ini.

### Jalur 1: Picker (Disarankan)

Satu perintah, lalu pilih. Menampilkan banner antislop, mencantumkan skill dengan core yang dikunci, bertanya di mana (project atau global) dan agent mana (Claude Code, Antigravity, Codex, OpenCode, Cursor, Gemini CLI, Hermes), lalu menginstal folder dan menulis pointer yang memuat antislop setiap sesi. Skills directory (jalur 2) tidak menulis pointer itu, jadi ini yang harus digunakan:

```bash
npx antislop-ai
```

### Jalur 2: Skills Directory

antislop terdaftar di [skills.sh](https://skills.sh), direktori terbuka untuk skill agent:

```bash
npx skills add muris11/anti-ai-slop
```

Tambahkan `--all` untuk semua skill, `-g` untuk instalasi global, atau `--skill <nama>` untuk satu skill. Jalankan `--list` dulu untuk melihat yang tersedia.

> **Catatan:** `npx skills add` menyalin folder skill tapi tidak menulis pointer entry agent yang memuat antislop setiap sesi; skills.sh tidak menulisnya, jadi gap itu milik mereka, bukan antislop. Itulah sebabnya picker (jalur 1) adalah cara instalasi yang disarankan. Kalau sudah pakai jalur 2, jalankan `npx antislop-ai`, pilih skill dan agent yang sama, dan pilih **Keep what is there** saat folder yang sudah ada ditemukan; itu menulis pointer.

skills.sh membaca folder skill langsung dari repository ini, jadi daftar muncul begitu repo live; tidak ada langkah setup terpisah.

### Jalur 3: Plugin (Claude Code)

Tambahkan marketplace sekali, lalu instal plugin:

```bash
/plugin marketplace add https://github.com/muris11/anti-ai-slop
/plugin install antislop@anti-ai-slop
```

### Jalur 4: Plugin (Antigravity)

Repo yang sama adalah plugin Antigravity lengkap: `plugin.json` root, enam skill terdaftar sebagai skill Antigravity, dan pointer `rules/antislop.md` yang memuat antislop ke setiap sesi. Instal dengan CLI Antigravity:

```bash
agy plugin install https://github.com/muris11/anti-ai-slop
```

### Instalasi Manual (Single File, Tanpa Packaging)

Core `antislop.md` saja sudah merupakan filter lengkap yang bisa kamu paste ke chat window mana pun. Unduh dan suruh agent membacanya; wizard First-Run di dalamnya menginstal skill secara manual:

```bash
# macOS / Linux
curl -o antislop.md https://raw.githubusercontent.com/muris11/anti-ai-slop/main/antislop.md

# Windows (PowerShell)
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/muris11/anti-ai-slop/main/antislop.md" -OutFile "antislop.md"
```

### Agent yang Didukung

Setiap skill adalah folder standar Agent Skills (`<nama>/SKILL.md`), jadi masuk ke agent mana pun yang membaca standar:

| Agent | Skill Folder | Picker | Plugin |
|-------|-------------|--------|--------|
| Claude Code | `.claude/skills/` | Ya | Ya (marketplace) |
| Antigravity | `.agents/skills/` | Ya | Ya (`agy plugin`) |
| Codex | `.codex/skills/` | Ya | Tidak |
| OpenCode | `.opencode/skills/` | Ya | Tidak |
| Cursor | `.cursor/skills/` | Ya | Tidak |
| Gemini CLI | `.gemini/skills/` | Ya | Tidak |
| Hermes | `~/.hermes/skills/` | Ya (global only) | Tidak |

Picker (jalur 1) menanyakan agent mana yang kamu gunakan dan menginstal ke dalamnya, membuat folder skill jika belum ada; skills directory (jalur 2) menangani agent yang sama dan lebih banyak lagi. Plugin adalah pintu per-agent: jalur 3 adalah plugin marketplace Claude Code, jalur 4 adalah plugin Antigravity.

### Kompatibilitas OS

antislop bekerja di **Windows**, **macOS**, dan **Linux**. Semua jalur instalasi cross-platform:

| Metode | Windows | macOS | Linux |
|--------|---------|-------|-------|
| Picker (`npx antislop-ai`) | Ya | Ya | Ya |
| Skills dir (`npx skills add`) | Ya | Ya | Ya |
| Plugin (Claude Code) | Ya | Ya | Ya |
| Plugin (Antigravity) | Ya | Ya | Ya |
| Manual (`curl` / `Invoke-WebRequest`) | Ya | Ya | Ya |

**Persyaratan:** Node.js 18+ (untuk `npx`), Git. Script contrast-check membutuhkan Python 3.8+ (opsional, untuk `antislop-human`).

---

## Skills

| Skill | Apa yang Dicakup | Ships In |
|-------|-----------------|----------|
| **antislop** | Filter core: aturan, tier, Delivery Gate, kehidupan | v1.0.0 |
| **antislop-ui** | UI / visual: layout, warna, komponen, dekorasi, motion, struktur | v1.0.0 |
| **antislop-copywriting** | Teks & copy: headline, CTA, tone, stats palsu, pola anti-AI-writing, kebersihan markdown | v1.0.0 |
| **antislop-human** | Aksesibilitas: kontras (dengan checker), keyboard, fokus, state | v1.0.0 |
| **antislop-layoutmobile** | Layout mobile: breakpoint responsif, grid, overflow, tap target, navigasi | v1.0.0 |
| **antislop-code** | Komentar kode: hapus komentar AI-slop generik, pertahankan yang berharga, jangan sentuh kodenya | v1.0.0 |
| **slop** | Loader sekali-jalan yang memuat seluruh keluarga antislop (core + semua skill) sekaligus | v1.0.0 |

Pilih yang sesuai dengan pekerjaan:
- **Pekerjaan UI** -> `antislop-ui`
- **Pekerjaan copy** -> `antislop-copywriting`
- **Pekerjaan aksesibilitas** -> `antislop-human`
- **Pekerjaan layout mobile** -> `antislop-layoutmobile`
- **Pekerjaan komentar kode** -> `antislop-code`
- **Lebih dari satu** -> instal beberapa
- **Tidak ada** -> core saja sudah filter lengkap

### Detail Skill

#### antislop (Core)

Fondasi. Selalu dimuat. Berisi:
- Semua 38 aturan (R-01 sampai R-38) dalam tiga tier
- Toolkit Kehidupan (tiga dial + Design Read)
- Delivery Gate (ceklist PASS/FAIL empat blok)
- First-Run Install Wizard

#### antislop-ui

Membersihkan UI yang dihasilkan AI. Mencakup:
- Default warna/gradient (R-01): gradient biru-ungu, gradient keras, ungu-hitam, neon, pastel, radial orbs
- Glassmorphism (R-10): blur di navbar+card+modal+sidebar
- Border radius (R-11): bentuk pill universal
- Bayangan (R-12): elevasi default di semua komponen
- Glow (R-13): neon glow di mana-mana
- Background grid (R-07): dot grid, pola blueprint
- Dark mode (R-21): dark dipaksakan tanpa alasan
- Palet (R-29): melebihi 2-3 inti + 1 aksen
- Ikon (R-04): Lucide-style ikon generik
- Tipografi (R-06): monospace-untuk-estetika, Geist Mono dan kawan-kawan
- Badge (R-09): kapsul badge, stripe kiri berwarna
- Animasi (R-19): motion template tanpa tujuan UX
- Layout (R-05): bento grid, layout template AI, fake terminal window, demo tanpa produk
- Pola dashboard, chart, tabel, motion

#### antislop-copywriting

Membersihkan teks yang dihasilkan AI. Mencakup:
- Kosakata AI kosong: unlock, elevate, empower, delve, harness, seamlessly
- Em dash (R-02)
- Inflasi signifikansi
- Klaim kosong
- Atribusi weasel ("banyak yang bilang", "para ahli setuju")
- Penutup chatbot
- Pembuka fake-candid
- Penyalahgunaan rule-of-three
- Spesifikasi dibuat-buat
- CTA generik (R-15)
- Buzzword AI (R-16)
- Mempertahankan: detail spesifik, perasaan campuran, referensi berdated, variasi kalimat, aside asli

#### antislop-human

Memastikan aksesibilitas. Mencakup:
- Kontras WCAG AA: 4.5:1 teks normal, 3:1 teks besar, 3:1 non-teks
- Navigasi keyboard (R-32): semua elemen interaktif bisa diakses
- Indikator fokus: terlihat di setiap elemen interaktif
- State UI (R-27): kosong, loading, error untuk setiap tampilan data
- Kompatibilitas zoom
- Penanganan keyboard mobile
- Menyediakan: script `contrast-check.py`, formula, tabel referensi

#### antislop-layoutmobile

Memastikan responsivitas mobile. Mencakup:
- Layout berubah ke state mobile yang berbeda
- Ukuran menggunakan skala mobile
- Grid runtuh dan menumpuk
- Tidak ada overflow horizontal (R-03)
- Tap target 44x44px
- Interaksi hover punya padanan tap
- Navigasi berubah
- Bar tetap menghormati konten

#### antislop-code

Membersihkan komentar kode yang dihasilkan AI. Mencakup:
- Menghapus: separator dekoratif (`// =====`), komentar yang hanya menyatakan yang jelas, narasi workflow (`// Step 1:`), label kosong (`// Main logic`), TODO samar, echo tanda tangan, emoji dekoratif, penanda akhir
- Mempertahankan: logika bisnis, keputusan arsitektural, pertimbangan keamanan, trade-off performa, edge case, kontrak API, workaround
- Tidak pernah menyentuh kode itu sendiri

---

## Mode Penggunaan

antislop digunakan dengan salah satu dari dua cara, dipilih di awal sesi:

### Mode 1: Selama Pekerjaan

**Cocok untuk:** project baru, membangun dari nol, menambahkan fitur.

Agent mengikuti semua aturan saat generate. Setiap keputusan visual mendapat uji tujuan. Setiap desain mendapat pengecekan kehidupan. Sesi diakhiri dengan laporan Delivery Gate.

**Cara kerja:**
1. Agent bertanya: "Kapan kamu mau pakai antislop?" Kamu jawab: "Selama."
2. Agent memuat core + skill yang relevan.
3. Agent membangun, menerapkan aturan secara real-time.
4. Agent menjalankan Delivery Gate sebelum deklarasi selesai.
5. Agent melaporkan PASS/FAIL. Kalau FAIL, agent memperbaiki dan menjalankan ulang.

### Mode 2: Setelah Pekerjaan (Audit)

**Cocok untuk:** meng-review kode yang ada, pengecekan pra-rilis, menemukan masalah.

Agent menghasilkan daftar temuan bernomor di `anti-slop/audit-001-YYYY-MM-DD.md` (nomor terus naik). Setiap temuan mencantumkan aturan yang dilanggar (R-XX) dan alasan satu baris.

- **Prioritas HIGH**: Pelanggaran Hard Gate (kejujuran, fungsi, aksesibilitas)
- **Prioritas MEDIUM**: Pelanggaran Purpose-Gate (teknik tanpa tujuan)
- **Prioritas LOW**: Pelanggaran Quality Lock (konsistensi)

Agent tidak memodifikasi apa pun sampai kamu menyetujui nomor tertentu. Nomor yang tidak disebut tidak disentuh. Setelah persetujuan, agent memperbaiki item dan menulis laporan tindak lanjut.

**Cara kerja:**
1. Agent bertanya: "Kapan kamu mau pakai antislop?" Kamu jawab: "Setelah."
2. Agent memuat core + skill yang relevan.
3. Agent mengaudit pekerjaan yang ada.
4. Agent menghasilkan daftar temuan bernomor dengan prioritas.
5. Kamu menyetujui nomor tertentu untuk diperbaiki.
6. Agent memperbaiki item yang disetujui dan menulis laporan tindak lanjut.

---

## Contoh

### Sebelum antislop

```html
<section class="bg-gradient-to-br from-blue-600 via-purple-500 to-pink-500">
  <div class="flex flex-col items-center text-center">
    <span class="inline-flex items-center px-3 py-1 text-xs font-semibold rounded-full bg-white/20 text-white">
      <Sparkles class="w-3 h-3 mr-1" /> AI Powered
    </span>
    <h1 class="text-4xl md:text-6xl font-bold text-white mt-4">
      Unlock the Power of Seamless Collaboration
    </h1>
    <p class="text-white/80 mt-4 max-w-xl">
      Empower your team to elevate their journey to the next level.
    </p>
    <button class="mt-6 px-6 py-3 rounded-full bg-white text-purple-600 font-semibold">
      Get Started <ArrowRight class="w-4 h-4 ml-1" />
    </button>
  </div>
</section>
```

**Masalah:**
- Gradient biru-ungu (R-01) - default tanpa tujuan brand
- Badge "AI Powered" (R-09) - kapsul tanpa fungsi
- Ikon sparkle (R-04) - generik, tanpa relevansi
- "Unlock the Power" (R-16) - buzzword AI
- "Seamless Collaboration" (R-16) - klaim kosong
- "Get Started" (R-15) - CTA generik
- Dekorasi panah (R-08) - dekoratif, tanpa tujuan
- Tombol pill (R-11) - bentuk pill universal
- Tidak ada alasan untuk elemen apapun (R-31)

### Sesudah antislop

```html
<section style="background-color: #0f172a; padding: 80px 24px;">
  <div style="max-width: 640px; margin: 0 auto;">
    <h1 style="color: #f8fafc; font-size: 36px; line-height: 1.2;">
      Your team shares files. This tool keeps them from getting lost.
    </h1>
    <p style="color: #94a3b8; margin-top: 16px; font-size: 18px;">
      Every file lives in one place. Search works. Nothing falls through the cracks.
    </p>
    <a href="#signup" style="display: inline-block; margin-top: 24px; padding: 12px 24px; background-color: #22c55e; color: #ffffff; font-weight: 600; text-decoration: none;">
      Create your free workspace
    </a>
  </div>
</section>
```

**Perbaikan:**
- Copy produk spesifik, tanpa buzzwords
- Tidak ada gradient (R-01) - background punya tujuan
- Tidak ada badge (R-09) - dihapus
- Tidak ada ikon (R-04) - dihapus
- CTA spesifik sesuai aksi (R-15) - "Create your free workspace"
- Tombol persegi panjang (R-11) - design system, bukan pill
- Tujuan untuk setiap elemen (R-31) - setiap elemen berfungsi

---

## Roadmap

| Versi | Perubahan |
|-------|-----------|
| v1.0.0 | Rilis perdana. Mengirim filter core (R-01 → R-38), Toolkit Kehidupan, dan Delivery Gate, plus enam skill tambahan (UI, copywriting, human, layout-mobile, code, dan loader `slop`). Mengirim packaging untuk semua jalur instalasi: picker npm, skills directory, plugin marketplace Claude Code, plugin Antigravity, dan jalur manual single-file. |

Lihat [ROADMAP.md](ROADMAP.md) untuk tracker lengkap, termasuk rencana plugin cross-agent.

---

## FAQ

### Apakah antislop adalah style guide?

Bukan, filter. Tidak menentukan warna, font, atau layout. Menolak teknik tanpa tujuan dan menuntut kehidupan; arah adalah milikmu.

### Agent mana yang didukung?

Semua, tapi jalur instalasinya berbeda:

- **Picker dan skills directory** mendukung Claude Code, Codex, Antigravity, OpenCode, Cursor, Gemini CLI, dan Hermes (picker mendeteksi folder skill masing-masing agent; Hermes hanya instal global). Ini jalur yang disarankan.
- **Plugin** adalah pintu per-agent: plugin marketplace Claude Code (jalur 3) dan plugin Antigravity (jalur 4), keduanya diinstal dari repo yang sama.
- **Single file** (`antislop.md`) bekerja dengan agent mana pun yang membaca Markdown biasa, termasuk chat window biasa.

Skill yang dipaketkan menggunakan standar Agent Skills terbuka (folder per skill), jadi masuk ke tool mana pun yang membaca standar.

### Apa itu "skill"?

Folder yang masuk lebih dalam ke satu concern (UI, copywriting, aksesibilitas, dll), berisi `SKILL.md` dengan aturannya. Merujuk aturan core berdasarkan nomor dan tidak pernah menduplikasi, jadi menambahkan skill tidak mengubah core.

### Apa itu DURING dan AFTER?

Dua mode penggunaan: DURING menerapkan aturan saat membangun, AFTER mengaudit pekerjaan yang sudah selesai. Kamu pilih salah satu di awal sesi.

### Apakah saya butuh DESIGN.md?

Ya. antislop adalah filter, bukan penyedia arah. Tanpa `DESIGN.md`, filter bisa menghapus slop tapi hasilnya bisa kaku. `DESIGN.md` menyediakan identitas brand, palet, tipografi, dan mood. Hasil yang kaku berarti arahnya tidak ada, bukan filternya gagal (R-37).

### Bagaimana kalau saya hanya pakai core, tanpa skill?

Core saja sudah filter lengkap. Punya semua 38 aturan, Toolkit Kehidupan, dan Delivery Gate. Skill masuk lebih dalam ke concern spesifik tapi tidak wajib.

### Bisakah saya instal hanya satu skill?

Ya. Gunakan `npx skills add muris11/anti-ai-slop --skill antislop-ui` untuk menginstal satu skill. Core selalu disertakan.

### Apakah ini bekerja dengan project non-UI?

Ya. Skill `antislop-code` membersihkan komentar kode. Skill `antislop-copywriting` membersihkan teks. Aturan core berlaku untuk konten AI yang dihasilkan, bukan hanya UI.

---

## Kontribusi

Menemukan pola AI slop baru, aturan yang melewatkan sesuatu, atau bug di installer? Buka issue. PR diterima untuk:

- Pola AI slop baru
- Klarifikasi
- Item checklist yang tidak sinkron dengan aturannya

Sebelum submit:

1. Baca aturan core
2. Jalankan Delivery Gate pada perubahanmu
3. Tulis alasan satu baris untuk setiap aturan yang kamu tambah atau ubah (R-31)

---

## Lisensi

MIT. Lakukan apa pun yang kamu mau.
