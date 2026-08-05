# Prompt: Plan

This prompt is **planning-only**. It produces a plan and stops. It does not implement anything,
even if the change looks trivial.

1.  Read `docs/SESSION.md`, `docs/TASKS.md`, and `STACK.md`. Check `docs/DECISIONS.md` for any
    ADR that constrains this task.
2.  Restate the request as explicit and implicit requirements, and define a testable version of
    "done".
3.  If the request contains several independent units of work, say so and stop — see Phase 1 of
    `AGENTS.md`. Do not plan them as one task.
4.  Identify: files to read, files to modify, files to create, tests required, risks, and the
    commands that will demonstrate acceptance.
5.  Estimate whether the resulting change fits inside one review pass (`STACK.md`, review
    thresholds). If it does not, split it here — splitting is a planning decision, not a runtime
    one.
6.  Present the plan with the reasoning behind it and **wait for explicit approval**. Do not
    proceed without it.
7.  Once approved, the plan is fixed. If implementation reveals it was wrong, that is a deviation
    to be recorded and raised — not a plan to be quietly rewritten.
