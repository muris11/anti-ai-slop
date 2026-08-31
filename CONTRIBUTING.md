# Contributing to anti-ai-slop

Thanks for helping make this better. This guide explains how to contribute a new AI-slop pattern, a rule clarification, a fix, or an improvement to the installer.

---

## Ways to contribute

- **Report a new AI slop pattern** — something you keep seeing that isn't covered yet.
- **Clarify a rule** — a rule that's ambiguous or a checklist item out of sync with its rule.
- **Fix the installer** — a bug in the `cli/` picker, the plugins, or the sync script.
- **Improve docs** — README, guide, or the skill files.

---

## Before you start

1. Read the core rules (`skills/antislop/SKILL.md`).
2. Read the master catalog (`skills/antislop-master/SKILL.md`) so a new indicator fits the existing P0–P6 tiers and code scheme.
3. Run the Delivery Gate on your own change (see the core skill).

---

## How to add a new indicator

Every indicator lives in `skills/antislop-master/SKILL.md` under a section and gets a code (e.g. `C-13`). A good indicator states:

- **What it is** — the concrete pattern.
- **The tier** — P0–P6, matching how strong the signal is.
- **The test** — how to tell a real choice from a default (purpose / convergence).

Then, if it's area-specific, mirror it in the matching domain skill (`-ui`, `-layout`, `-forms`, etc.) with a pointer back to the master code.

---

## Checklist

- [ ] One idea per change; keep PRs focused.
- [ ] Indicator carries a tier and a code.
- [ ] No `raw.githubusercontent.com` runtime download URLs in any `SKILL.md` (the sync guard blocks these).
- [ ] `npm run test` (smoke test) passes.
- [ ] JSON files are valid (`package.json`, `cli/package.json`, plugin manifests).
- [ ] Write a one-line reason for the change (R-31 philosophy).

---

## Submitting

- Open a PR against `main`.
- Explain what and why in the description.
- Reference any related issue.
- Follow the existing code style (no comments unless they add meaning).

## License

By contributing, you agree that your contributions are licensed under the [MIT License](LICENSE).
