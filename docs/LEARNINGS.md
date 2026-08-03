# LEARNINGS.md — Learnings Log

> Immutable, timestamped log. Every completed PRAR cycle adds a new entry at the end.
> Past entries are never edited or deleted — only appended to.

---

## Entry format

```
## [YYYY-MM-DD HH:MM] Brief task title

**Context:** What was requested and why.

**Decisions made:** Relevant technical choices (library used, state pattern, data structure, etc. — consistent with `STACK.md`).

**What worked:** What went well and is worth repeating.

**What failed / was discarded:** Approaches that didn't work and why they were abandoned.

**Lesson for the future:** What to apply in similar tasks going forward.
```

---

## Example (illustrative — adapt the technical terms to the project's real `STACK.md`)

## [2026-07-25 10:00] Initial auth setup

**Context:** Login/signup was implemented against the project's backend.

**Decisions made:** Used the async state pattern defined in `STACK.md` to listen for session changes; loading/error handled consistently across the UI.

**What worked:** Separating the data layer (backend calls) from the state layer made testing with mocks easier.

**What failed / was discarded:** A simple synchronous approach to session state was tried first, but it didn't react well to async backend changes — migrated to a reactive pattern (stream/observable, per whatever `STACK.md` defines).

**Lesson for the future:** For any reactive data source (auth, sockets, real-time data), prefer a reactive pattern from the start instead of simple synchronous state.

---

<!-- New entries are added below this line -->
