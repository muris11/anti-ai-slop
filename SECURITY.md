# Security

**anti-ai-slop** is a set of agent skills — Markdown rule files plus two local Python helper scripts. It is a **filter** that tells an agent how to write UI, copy, and code. It does not fetch, execute, or transmit anything on its own beyond what the agent already does.

This document explains what is in the box, the trust boundaries, and how to report a concern.

---

## What's in the box

- `skills/*/SKILL.md` — plain Markdown rule files (17 skills). These are instructions an agent reads; they contain no executable code.
- `antislop.md` — the standalone core rules, usable as a single file without packaging.
- `skills/antislop-human/contrast-check.py` — a small local Python script that checks color contrast (run locally, no network, no dependencies beyond Python 3.8+).
- `skills/antislop-human/contrast-mcp.py` — an optional MCP server that wraps the same contrast check. Loaded **only** if you enable the `antislop-contrast` MCP server in the Claude Code plugin (`.claude-plugin/plugin.json`).
- `cli/` — the `anti-ai-slop` npm picker that copies skill folders into the agent folders you choose and writes a session pointer.

## What it does not do

- It does **not** download, fetch, or install anything at runtime.
- It does **not** phone home or transmit telemetry of its own.
- It does **not** execute remote code. The only executable content is the two optional, local-only Python helpers, and only the MCP server runs when you explicitly enable it.
- The session pointer it writes is plain Markdown inside an agent's entry file — never a hook, never a script.

## Trust boundaries

- **Direction is yours.** `DESIGN.md` is the source of direction; anti-ai-slop never supplies aesthetics. This boundary is stated in the core rules.
- **No runtime self-install.** The core skill must not instruct the agent to download further instruction files at runtime. The `cli/scripts/sync-skills.mjs` guard enforces this and refuses to build if a runtime `raw.githubusercontent.com` URL is present.
- **Scoped writes only.** The installer (`cli/`) copies files into only the folders you select and for only the agents you select. When it writes a session pointer, it does so strictly between `<!-- antislop:start -->` and `<!-- antislop:end -->` and never overwrites content outside that block.
- **Audit the source.** Skills are code-adjacent policy applied by an agent. Only install from a source you trust. Review the `SKILL.md` files and the two Python scripts before enabling the MCP server.

## Supported-agent storage

The installer targets these folders (never touching files elsewhere):

| Agent | Target |
|---|---|
| Claude Code | `.claude/skills` |
| Antigravity | `.agents/skills` |
| Codex | `.codex/skills` |
| OpenCode | `.opencode/skills` |
| Cursor | `.cursor/skills` |
| Gemini CLI | `.gemini/skills` |
| Hermes | `~/.hermes/skills` (global only) |

## Reporting a vulnerability

If you find a security issue, a rule that causes harm, or a supply-chain concern:

- Open a GitHub issue at <https://github.com/muris11/anti-ai-slop/issues> with the details.
- Do **not** embed secrets, credentials, or live malicious links directly in an issue.
- For anything time-sensitive, describe the affected file and the behavior rather than pasting raw payloads.

## Supported versions

Security updates apply to the current `main` branch. We do not backport fixes to older tags.

---

## License

MIT — see [LICENSE](LICENSE).
