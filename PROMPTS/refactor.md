# Prompt: Refactor

1.  Read `docs/SESSION.md` and `docs/DECISIONS.md` — confirm this refactor doesn't contradict a decision already made (if it does, propose a new ADR instead of ignoring the previous one).
2.  Confirm test coverage exists for the code being refactored. If it doesn't, propose adding it first.
3.  Observable behavior must NOT change — this prompt is only for improving structure, readability, or performance.
4.  Present the refactor plan (what's being moved, what's being extracted) before executing, if it touches more than one file.
5.  Implement in small increments, running tests after each step.
6.  Run the test and lint commands defined in `STACK.md` when finished.
7.  The "internal change with no observable behavior" exception from section 11 of `AGENTS.md` **does not apply here** unless the refactor is trivial (renaming a local variable, for example): a real refactor touches observable behavior by definition even though it shouldn't change it, so run functional verification to confirm the result is identical to before the refactor.
8.  Update `docs/LEARNINGS.md` if the refactor revealed something relevant, and `docs/SESSION.md`.
