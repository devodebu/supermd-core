# Prompt: Code Review

Audit the indicated code against the `AGENTS.md` and `STACK.md` checklist:

1.  **Architecture:** Does it respect the layer separation/folder structure defined in `STACK.md`? Is business logic free of UI-framework dependencies where it should be?
2.  **Data integrity (section 8 of `AGENTS.md`):** Is there any place where a missing value gets filled in with a made-up value instead of reflecting the real state?
3.  **Security (section 9 of `AGENTS.md` + section 9 of `STACK.md`):** Any hardcoded secrets? Are listeners/subscriptions/timers cleaned up correctly? Any sensitive data outside the secure storage mechanism defined in `STACK.md`?
4.  **State management:** Does it follow the loading/error/empty/data pattern defined in `STACK.md` for async operations? Is state properly scoped, without being recreated unnecessarily?
5.  **Conventions (section 6 of `AGENTS.md` + `STACK.md`):** naming, file structure, consistency with `docs/design.md`.
6.  **Tests:** Is there reasonable coverage for the business logic touched?

Deliver the result as a list of prioritized findings (critical / important / minor), not as an automatic patch — the user decides what to fix and when.
