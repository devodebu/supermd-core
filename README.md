# SuperMD Core

A stack-agnostic `.md` template set that gives your AI coding agent (Claude Code, Gemini CLI, Codex) a real working protocol: a Perceive→Reason→Act→Refine cycle, mandatory functional verification before anything counts as "done", and session continuity so your agent doesn't lose the thread between conversations.

Works with any language or framework — `AGENTS.md` never hardcodes a stack, everything project-specific lives in one `STACK.md` you fill in once.

## What's in Core

- `AGENTS.md` — the full PRAR protocol: perceive, reason, act, refine, with mandatory functional verification (section 11) and behavioral guardrails (simplicity-first, surgical changes).
- `PROMPTS/feature.md`, `bugfix.md`, `refactor.md`, `review.md` — ready-to-use instruction templates for the 4 most common task types.
- `docs/` — `PRD.md`, `design.md`, `TASKS.md`, `SESSION.md`, `LEARNINGS.md`, `DECISIONS.md` templates to keep your project's context alive across sessions.
- `STACK.md` — blank template, fill it in for any stack.
- Compatible with Claude Code, Gemini CLI, and Codex/GPT (`CLAUDE.md`/`GEMINI.md` symlinks included).

## What's in [SuperMD Pro](https://gumroad.com/) (paid, updates included for life)

- **Bug audit & feature discovery workflows** — `PROMPTS/audit.md` and `PROMPTS/discovery.md`, with an automatic Backlog system in `TASKS.md` so findings never get lost or pasted into the wrong file.
- **Ready-made stack presets** — Flutter, React/Vite, and more added over time. Skip filling `STACK.md` from scratch.
- **Version migration guides** — when the protocol updates, a step-by-step guide walks your existing projects through the upgrade instead of you figuring it out by diffing files.
- Free lifetime updates to all of the above.

## Quick start

1. Copy everything in this repo into your project root.
2. Tell your agent: *"Fill in STACK.md with this project's real stack, and AGENTS.md section 3 with a short project description."*
3. Work normally — ask for features/fixes like you always do. The agent now follows the protocol automatically.

See `USAGE_GUIDE.md` for a full walkthrough (reading order, how to request tasks, who updates each file, and what to watch for).

## License

MIT — use it, fork it, adapt it.
