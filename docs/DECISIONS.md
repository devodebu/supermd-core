# DECISIONS.md — Technical Decisions Log (ADR)

> Every non-trivial technical decision is logged here before implementing it.
> Past decisions are never edited or deleted — if a decision gets reversed, a new ADR is added that replaces it and references the old one.

---

## Format

```
## ADR-00X: <title>
- Date:
- Status: Proposed / Accepted / Superseded by ADR-00Y
- Context: why this needed to be decided
- Decision: what was chosen
- Alternatives considered: what was discarded and why
- Consequences: what this decision implies going forward
```

---

## Example (illustrative — adapt the content to your `STACK.md`'s actual decisions)

## ADR-001: Project state management

- Date: 2026-07-25
- Status: Accepted
- Context: The project needs a consistent state-management solution across the app, with good support for async operations against the backend defined in `STACK.md`.
- Decision: (the chosen library/pattern — see `STACK.md`)
- Alternatives considered: (what was evaluated and why it was discarded)
- Consequences: All async data consumption must consistently follow the chosen pattern across the app.

---

<!-- New ADRs are added below this line -->
