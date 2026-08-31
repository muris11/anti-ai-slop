# anti-ai-slop

> Stop AI agents from generating generic, recognizable "AI slop" UI, copy, and code comments.

anti-ai-slop is a filter system for AI coding agents (Claude Code, Cursor, Gemini CLI, Copilot, and others). It does not impose an aesthetic. It does not ban techniques. It holds every visual and text decision to a purpose test, and it demands liveliness over sterility.

**The question behind everything:**

> If the logo and product name were swapped out, would this design still feel unique and have its own character?

If the answer is no, the design is too generic. Start over.

---

## Table of Contents

- [What This Is](#what-this-is)
- [What This Is Not](#what-this-is-not)
- [Skills Overview](#skills-overview)
- [Installation](#installation)
  - [Claude Code](#claude-code)
  - [Cursor](#cursor)
  - [Gemini CLI](#gemini-cli)
  - [Other Tools](#other-tools)
- [Usage](#usage)
  - [Mode 1: During the Work](#mode-1-during-the-work)
  - [Mode 2: After the Work (Audit)](#mode-2-after-the-work-audit)
- [The 38 Rules](#the-38-rules)
  - [Group 1: Hard Gate](#group-1-hard-gate)
  - [Group 2: Purpose-Gate](#group-2-purpose-gate)
  - [Group 3: Quality Locks](#group-3-quality-locks)
- [The Liveliness Toolkit](#the-liveliness-toolkit)
  - [Three Dials](#three-dials)
  - [Design Read](#design-read)
- [Delivery Gate](#delivery-gate)
- [Skill Details](#skill-details)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

---

## What This Is

anti-ai-slop is a **filter**, not a style guide. It stops AI coding agents from producing generic, recognizable "AI slop" UI, without falling into the opposite failure: a sterile, lifeless default.

- It does **not** impose an aesthetic: no prescribed colors, fonts, layouts, or "house style".
- It does **not** ban visual techniques (gradients, glassmorphism, badges, card grids). Those are tools. What it rejects is **technique without purpose**.
- It does two things only:
  1. Holds every visual decision to a **purpose test**: what does this technique serve? Write the reason down.
  2. Holds the result to a **liveliness bar**: the output must be alive and specific, not just "clean".

## What This Is Not

- Not a design system. You still need your own `DESIGN.md` with brand identity, palette, typography, and mood.
- Not an aesthetic. There are no "do this" visual rules, only "justify this" tests.
- Not a ban list. Part 1 is a diagnostic scan. Part 2 has the actual rules.

---

## Skills Overview

anti-ai-slop is a system: a core filter plus optional skills, one per concern.

| Skill | Concern | When to Load |
|-------|---------|-------------|
| **antislop** (core) | Purpose test, tiers, delivery gate, liveliness | Always, as the foundation |
| **antislop-ui** | Color, layout, components, decoration, motion | Building or editing UI |
| **antislop-copywriting** | Headlines, CTAs, tone, value propositions | Writing or editing copy |
| **antislop-human** | Contrast, keyboard, focus, accessibility | Any UI work |
| **antislop-layoutmobile** | Breakpoints, grids, overflow, tap targets | Mobile/responsive layouts |
| **antislop-code** | Code comments hygiene | Writing or editing comments |
| **slop** | One-shot loader for all skills | When you want everything at once |

---

## Installation

### Claude Code

**Automatic install (recommended):**

Place the skill files in your project's skills directory, then add a pointer block to your `CLAUDE.md`:

```markdown
<!-- antislop:start -->
## antislop
For UI, copy, people, mobile layout, or code comments work, read `antislop.md` (core) and then the skill for the task:
- UI / visual: `skills/antislop-ui/SKILL.md`
- Copy & text: `skills/antislop-copywriting/SKILL.md`
- People: `skills/antislop-human/SKILL.md`
- Mobile / responsive: `skills/antislop-layoutmobile/SKILL.md`
- Code comments: `skills/antislop-code/SKILL.md`
Before starting, ask the user when antislop applies: during the work, or after it is done.
<!-- antislop:end -->
```

**Manual install:**

1. Copy all skill files into your project:
   ```
   skills/
     antislop/SKILL.md
     antislop-ui/SKILL.md
     antislop-copywriting/SKILL.md
     antislop-human/SKILL.md
     antislop-human/contrast-check.py
     antislop-layoutmobile/SKILL.md
     antislop-code/SKILL.md
     slop/SKILL.md
   ```

2. Add the pointer block above to `CLAUDE.md`.

3. Done. Claude Code will now read antislop rules at the start of each session.

### Cursor

Add the antislop rules to `.cursor/rules/antislop.mdc` or your project's `.cursorrules` file. Copy the content from the skill files. Cursor supports rule files that load automatically when you work on UI tasks.

### Gemini CLI

Add a pointer in your `GEMINI.md`:

```markdown
<!-- antislop:start -->
## antislop
For UI, copy, people, mobile layout, or code comments work, read the antislop skills in `skills/`:
- UI / visual: `skills/antislop-ui/SKILL.md`
- Copy & text: `skills/antislop-copywriting/SKILL.md`
- People: `skills/antislop-human/SKILL.md`
- Mobile / responsive: `skills/antislop-layoutmobile/SKILL.md`
- Code comments: `skills/antislop-code/SKILL.md`
Before starting, ask the user when antislop applies: during the work, or after it is done.
<!-- antislop:end -->
```

### Other Tools

Any tool that reads a project-level instruction file (AGENTS.md, CLAUDE.md, GEMINI.md, etc.) can use antislop. Copy the pointer block into whichever file your tool reads at session start.

---

## Usage

At the start of a session, antislop asks you (or your agent asks you) one question:

> **When do you want to use antislop?**
> 1. **DURING** the project, while working (planning and execution). Rules apply while the agent writes, preventing slop from the start.
> 2. **AFTER** the project is finished. The agent audits what exists: a numbered findings list with priorities, you pick which numbers to fix.

### Mode 1: During the Work

Best for: new projects, building from scratch, adding features.

The agent follows all rules while generating. Every visual decision gets a purpose test. Every design gets a liveliness check. The session ends with a Delivery Gate report.

### Mode 2: After the Work (Audit)

Best for: reviewing existing code, pre-launch checks, finding problems.

The agent produces a numbered findings list in `anti-slop/audit-001-YYYY-MM-DD.md` (numbers keep rising). Each finding cites the violated rule (R-XX) and a one-line reason.

- **HIGH priority**: Hard Gate violations (honesty, function, accessibility)
- **MEDIUM priority**: Purpose-Gate violations (technique without purpose)
- **LOW priority**: Quality Lock violations (consistency)

The agent does not modify anything until you approve specific numbers. Numbers not mentioned are not touched. After approval, the agent fixes the items and writes a follow-up report.

---

## The 38 Rules

All rules are grouped into three tiers. **Hard Gate** rules are absolute. **Purpose-Gate** rules allow the technique but require a written reason. **Quality Locks** are consistency requirements.

### Group 1: Hard Gate

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

### Group 2: Purpose-Gate

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

### Group 3: Quality Locks

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

---

## The Liveliness Toolkit

A filter can remove slop, but it cannot add energy. Liveliness must be **added** deliberately.

### Three Dials

Every design must set three dials:

| Dial | 1 (Calm) | 2 (Balanced) | 3 (Bold) |
|------|----------|--------------|----------|
| **ENERGY** | Linear, GOV.UK | Stripe, Vercel | Awwwards, agency portfolio |
| **RHYTHM** | Uniform grid, predictable | Consistent with a few breaks | Asymmetric, mixed compositions |
| **MOTION** | Hover states only | Scroll-reveal, transitions | Parallax, pin, choreography |

**Example sets:**
- Designer portfolio: ENERGY 3, RHYTHM 3, MOTION 2
- Public service site: ENERGY 1, RHYTHM 1, MOTION 1

### Design Read

Before generating, declare one line:

> Reading this as: `<page kind>` for `<audience>`, in a `<visual language>` style, dial `<ENERGY/RHYTHM/MOTION>`.

Example: *"Reading this as: B2B SaaS landing for technical buyers, with a Linear-style minimalist language, dial ENERGY 1 / RHYTHM 2 / MOTION 1."*

---

## Delivery Gate

Run this gate BEFORE delivering. If any item is FAIL, fix it first, then re-run.

### Block 1: Hard Gate

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

### Block 2: Purpose-Gate

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

### Block 3: Liveliness

All answers must be **yes**:

- [ ] Dials set and explicit?
- [ ] Output consistent with claimed dials?
- [ ] At least one clear focal point per screen?
- [ ] Whitespace structural, not leftover?
- [ ] One deliberate accent (not zero, not everywhere)?
- [ ] Identity motif present?
- [ ] Design Read declared?

### Block 4: Craftsmanship

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

## Skill Details

### antislop-code

Cleans AI-generated code comments:

- **Removes**: decorative separators (`// =====`), restating-the-obvious comments, workflow narration (`// Step 1:`), empty labels (`// Main logic`), vague TODOs, signature echo, decorative emoji, end markers
- **Preserves**: business logic, architectural decisions, security considerations, performance trade-offs, edge cases, API contracts, workarounds

### antislop-copywriting

Cleans AI-generated prose:

- **Removes**: empty AI vocabulary (unlock, elevate, empower, delve), em dashes, significance inflation, empty claims, weasel attributions, chatbot closers, fake-candid openers, rule-of-three overuse, fabricated specifics
- **Preserves**: specific details, mixed feelings, dated references, sentence variety, genuine asides

### antislop-human

Ensures accessibility:

- **Checks**: WCAG AA contrast (4.5:1 normal, 3:1 large), keyboard navigation, focus indicators, non-text contrast (3:1), empty/loading/error states, zoom compatibility, mobile keyboard handling
- **Provides**: contrast-check.py script, formula, reference table

### antislop-layoutmobile

Ensures mobile responsiveness:

- **Checks**: layout reflows into a distinct mobile state, sizes use mobile scale, grids collapse and stack, no horizontal overflow, tap targets 44x44px, hover interactions have tap equivalents, navigation reflows, fixed bars respect content

### antislop-ui

Cleans AI-generated UI:

- **Covers**: color/gradient defaults, glassmorphism, border radius, shadows, glow, background grids, dark mode, palette, icons, typography, badges, animations, layout templates, dashboard patterns, charts, tables, motion

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

**Problems:** blue-purple gradient, em dash potential, "AI Powered" badge, sparkle icon, "Unlock the Power" buzzword, generic CTA, arrow decoration, pill button, no purpose written for any of it.

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

**Improvements:** specific product copy, no gradient, no badge, no icon, CTA specific to the action, rectangular design system button, purpose for every element.

---

## Contributing

Contributions welcome. Before submitting:

1. Read the core `antislop.md` rules
2. Run the Delivery Gate on your changes
3. Write a one-line reason for every rule you add or modify (R-31)

---

## License

MIT. Do whatever you want with it.
