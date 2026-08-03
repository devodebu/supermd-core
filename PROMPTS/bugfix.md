# Prompt: Bugfix

1.  Read `docs/SESSION.md` and `docs/LEARNINGS.md` — check whether this error was already reported or fixed before (avoid known regressions).
2.  Reproduce the error before touching any code. If you can't reproduce it, say so explicitly instead of assuming the cause.
3.  Find the root cause — don't apply a superficial patch that hides the symptom.
4.  If the error involves missing or inconsistent data from an external source (backend/API/DB), review section 8 of `AGENTS.md` (Data Integrity) before deciding how to handle it.
5.  Present the diagnosis and the proposed fix before implementing, if the change is significant.
6.  Implement the fix and add a test that covers the case (regression test).
7.  Run the test and lint commands defined in `STACK.md`.
8.  Run the functional verification from section 11 of `AGENTS.md`: reproduce the case that was failing (before → fails, after → passes) and log the evidence.
9.  Document the bug, the root cause, and the fix in `docs/LEARNINGS.md`. Update `docs/SESSION.md`.
