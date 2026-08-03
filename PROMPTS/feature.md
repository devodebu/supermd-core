# Prompt: New Feature

Follow the full PRAR cycle defined in `AGENTS.md`:

1.  Read `docs/SESSION.md`, `docs/PRD.md`, `docs/design.md`, and `STACK.md` to understand the context, requirements, and technical conventions for this feature.
2.  If the feature involves data from an external source (backend/API/DB), verify the existing data model — don't assume fields you haven't confirmed exist.
3.  Present a plan: files to create/modify, state pieces needed, and test strategy. Wait for approval before implementing.
4.  Implement following the conventions in `STACK.md` and section 6 of `AGENTS.md`.
5.  Cover the 4 mandatory UI states (`docs/design.md` section 5): loading, empty, error, with data.
6.  If you made a relevant technical decision, log it in `docs/DECISIONS.md`.
7.  Run the test and lint commands defined in `STACK.md`.
8.  Run the functional verification from section 11 of `AGENTS.md` and log the evidence — don't consider the feature done just because it compiled and tests passed.
9.  Update `docs/TASKS.md`, `docs/LEARNINGS.md`, and `docs/SESSION.md`.
