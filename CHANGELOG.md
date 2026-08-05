# Changelog — SuperMD Core

## v1.1.0

### Added

- **`PROMPTS/plan.md`** (new): planning-only prompt — produces a plan and stops, filling the gap between whole-task protocols (`feature.md`, `bugfix.md`, `refactor.md`) and the read-only `review.md`.
- **`STACK.md`**: new "Failure extraction" and "Review thresholds" subsections under Commands.
- **`docs/TASKS.md`**: new "Backlog" section for incidental bugs found out of scope while working on another task.

### Changed

- `AGENTS.md` (and its `CLAUDE.md`/`GEMINI.md` copies):
  - Phase 1 (Perceive and Understand): new point — ask whether to split a request containing several independent units of work into separate tasks, or log them in the Backlog, instead of merging them into one.
  - Phase 3 (Act and Implement): new point — work from extracted failure summaries, not raw verification output; new point — log incidental bugs to the Backlog instead of fixing them on the spot, unless they block the current task.
  - `PROMPTS/` list now includes `plan.md`.
  - Minor clarification: `docs/LEARNINGS.md` lives in the project root.
- `README.md`: prompt list updated to include `plan.md`.

## v1.0.0

- First public release.
- `AGENTS.md` with the PRAR protocol (Perceive, Reason, Act, Refine) and mandatory functional verification at task close.
- `PROMPTS/feature.md`, `bugfix.md`, `refactor.md`, `review.md`.
- `docs/` templates: `PRD.md`, `design.md`, `TASKS.md`, `SESSION.md`, `LEARNINGS.md`, `DECISIONS.md`.
- `STACK.md` blank template, stack-agnostic by design.
