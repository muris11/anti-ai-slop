# Security

antislop is a set of agent skills — Markdown rule files plus two local Python helper scripts. It is a **filter** that tells an agent how to write UI, copy, and code. It does not fetch, execute, or transmit anything on its own beyond what the agent already does.

## What's in the box

- `skills/*/SKILL.md` — plain Markdown rule files.
- `antislop.md` — the standalone core rules.
- `skills/antislop-human/contrast-check.py` — a small local Python script that checks color contrast (run locally, no network).
- `skills/antislop-human/contrast-mcp.py` — an optional MCP server that wraps the same contrast check. Loaded only if you enable the `antislop-contrast` MCP server in the Claude Code plugin.

## Boundaries

- The `DESIGN.md` file is explicitly the source of direction. antislop never supplies aesthetics; that boundary is stated in the core rules.
- The core skill (`SKILL.md`) must not instruct the agent to download further instruction files at runtime. The sync script enforces this and refuses to build if a runtime download URL is present.
- The installer (`cli/`) copies files only into the folders you choose, for the agents you select. It writes a pointer block between `<!-- antislop:start -->` and `<!-- antislop:end -->` in the agent's entry file, and never overwrites content outside that block.

## Reporting

If you find a vulnerability, a rule that causes harm, or a supply-chain concern, open a GitHub issue with the details rather than embedding secrets or links in an issue.

## What to do before installing

Skills are code-adjacent policy applied by an agent. Only install from a source you trust. Review the `SKILL.md` files and the two Python scripts before enabling the MCP server.
