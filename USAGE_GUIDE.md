# Usage Guide — SuperMD Core

This guide explains how to use this template set in any software project, regardless of stack. Everything here is stack-agnostic by design — `AGENTS.md` never hardcodes a language or framework, all of that lives in the one `STACK.md` you fill in per project.

> Looking for ready-made stack presets, bug-audit/feature-discovery workflows, or a bilingual version? Those are in [SuperMD Pro](https://gumroad.com/) — this guide only covers what's included in Core.

## 1. Installing in a new project

1.  Copy everything in this repo to your project's root (next to `package.json`/`pubspec.yaml`/equivalent). `CLAUDE.md` and `GEMINI.md` are symlinks pointing to `AGENTS.md` — if your filesystem or zip tool doesn't preserve symlinks on copy, recreate them:
    ```bash
    ln -s AGENTS.md CLAUDE.md
    ln -s AGENTS.md GEMINI.md
    ```
2.  Fill in `STACK.md` with your actual language, framework, testing setup, and commands (see section 8 of `STACK.md` for the command list your agent will run).
3.  Fill in the placeholders before you start coding for real:
    - `README.md` and `docs/PRD.md` — project name, scope, MVP features
    - `AGENTS.md` section 3 — project description and target platforms
    - `docs/design.md` — color palette, typography, tokens

No need to touch `docs/SESSION.md`, `docs/DECISIONS.md`, `docs/TASKS.md`, or `docs/LEARNINGS.md` at the start — they start empty and fill in on their own as you use them.

## 2. The reading order you ask your AI agent to follow

At the start of any work session, ask your agent (Claude Code, Gemini CLI, Codex) to follow this order — or just trust that `AGENTS.md` already tells it to in PRAR Phase 1:

1. `docs/SESSION.md` → where the last task left off
2. `AGENTS.md` → rules, conventions, workflow cycle
3. `STACK.md` → what language/framework/backend this project is built with
4. `docs/PRD.md` + `docs/design.md` → what's being built and how it should look
5. `docs/TASKS.md` → what's next

## 3. How to request a task

Instead of writing a long prompt every time, use the `PROMPTS/` templates as a starting point and add the specific detail of your task:

```
Follow PROMPTS/feature.md.
Task: add a user profile screen with name and photo editing.
```

```
Follow PROMPTS/bugfix.md.
Task: the like counter doesn't update in real time on the post list.
```

Core ships four templates: `feature.md`, `bugfix.md`, `refactor.md`, `review.md` — covering the most common task types. This saves you from re-explaining the whole process (plan → approval → tests → functional verification → docs) every time.

## 4. The PRAR workflow in practice

Every task, regardless of size, follows 4 phases (defined in `AGENTS.md` section 2):

| Phase | What the agent does | What you do |
|---|---|---|
| **Perceive** | Reads `docs/SESSION.md` and `STACK.md`, understands the request, reviews existing code | Clarify anything it asks about |
| **Reason** | Proposes a plan: which files it'll touch, what tests it'll write | **You approve or adjust the plan before it codes anything** |
| **Act** | Implements in small steps, runs the tests and lint from `STACK.md`, and runs functional verification (section 11 of `AGENTS.md`) when done | Review the code as it progresses |
| **Refine** | Runs the full suite, logs functional verification evidence in `docs/LEARNINGS.md`, updates docs, `docs/TASKS.md`, and `docs/SESSION.md` | Make the commit, or ask it to |

The "Reason" phase is the most important one for you: that's where you stop an approach you're not happy with **before** a single line of code gets written.

> **Functional verification (`AGENTS.md` section 11):** no task moves to "Done" in `docs/TASKS.md` just because it compiled or the tests passed — real-use evidence is required (a real call for endpoints, a screenshot/recording for UI, a reproduced case for bugfixes). If something fails 3 times in a row on the same approach, the agent must dump the state into `docs/LEARNINGS.md`/`docs/SESSION.md` and stop instead of blindly iterating — don't let it try a fourth time the same way.

## 5. Maintaining each file — who updates it and when

| File | Updated by | Frequency |
|---|---|---|
| `docs/SESSION.md` | The agent, when closing each task | Every session |
| `docs/TASKS.md` | The agent (when planning and completing) | Every task |
| `docs/LEARNINGS.md` | The agent, after each full PRAR cycle | Every task |
| `docs/DECISIONS.md` | The agent, when it makes a relevant technical decision | Occasional (only important decisions) |
| `docs/PRD.md` | You, when product scope changes | When you decide to add/remove features |
| `docs/design.md` | You (or the agent, if you provide new mockups) | When visual design changes |
| `README.md` | You, occasionally | When project setup changes |
| `STACK.md` | You, if the technical stack changes | Rarely — only if you migrate framework/backend |
| `AGENTS.md` | You, if the protocol rules change | Very rarely — it's the stack-agnostic base, it shouldn't change often |

## 6. Things you need to watch (the agent won't self-correct these)

- **`AGENTS.md` section 8 (Data Integrity):** if you ever see the agent "fill in" a missing value instead of showing an empty or error state, that's a direct violation of this rule — fix it immediately, don't let it slide even once.
- **Outdated `docs/DECISIONS.md`:** if you notice the agent reopening an already-settled debate (e.g., proposing another state library that was already ruled out), point it to the corresponding entry.
- **`docs/SESSION.md` not updated:** if the agent doesn't seem to know where you left off at the start of a new session, check whether it actually wrote there at the end of the previous one.
- **`STACK.md` out of sync with the real code:** if you migrate library or backend mid-project, update `STACK.md` at the same time — otherwise the agent will keep assuming the old stack.

## 7. Using it in an existing project (not from scratch)

If you're adding this set to a project that already has code:

1. Ask the agent to first fill in `STACK.md` describing the actual stack already in use (not a blank guess), and to fill `AGENTS.md` section 3 and `docs/TASKS.md` with an inventory of the current state (what exists, what's missing) before touching anything.
2. Don't retroactively force `docs/design.md` if the project already has a different design system — document the existing one instead of imposing the generic template.
3. Log a first entry in `docs/DECISIONS.md` for "why this file set was adopted" — it's a useful anchor if you later wonder why certain changes were made.

## 8. Reusing the set in a new project

The whole set (`AGENTS.md` + symlinks + `PROMPTS/` + `docs/` templates) is 100% reusable as-is between projects, regardless of stack. Only `STACK.md` needs to be filled in again from scratch for each new project — Core doesn't ship pre-filled presets (that's in Pro). Only `README.md`, `docs/PRD.md`, `docs/design.md`, `docs/TASKS.md`, `docs/SESSION.md`, `docs/LEARNINGS.md`, and `docs/DECISIONS.md` need to be reset (left blank) for each new project.
