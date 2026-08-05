# STACK.md — Project Technical Stack

> This file holds everything specific to this project's language/framework/backend. `AGENTS.md` references it but never hardcodes it — that way the rest of the set (`AGENTS.md`, `PROMPTS/`, `docs/TASKS.md`, etc.) is reusable across projects with different stacks.
>
> To create a new preset (e.g. SvelteKit, Astro, Next.js, a Node/Python backend...): copy this file, fill in each section, and save it as `stacks-en/<preset-name>/STACK.md` along with its lint config file if applicable.

## 1. Language and Framework

- Language:
- Main framework:
- Minimum version:

## 2. Project type and target platforms

- (mobile app / web app / static site / backend / library)
- Platforms: (iOS / Android / Web / Desktop — specify)

## 3. State Management

- (chosen library/pattern and why)

## 4. Backend / Data

- (own API / BaaS / no backend / etc.)
- Main data source:

## 5. Testing

- Unit:
- Integration/E2E:
- Mocks:
- Functional verification (evidence when closing a task — see `AGENTS.md` section 11):

## 6. Folder structure

```
(project's folder tree)
```

## 7. Naming conventions

- Files:
- Components/Modules/Classes:
- Variables/functions:

## 8. Commands

```bash
# install dependencies

# start dev environment

# run tests

# lint / static analysis

# production build

# functional verification (manual smoke test or script — see AGENTS.md section 11)
```

### Failure extraction

> How to reduce a failed run to its actionable core for this project's tooling.
> Used by any role that has to act on a failure — see `AGENTS.md`, Phase 3.

| Purpose | Command |
|---|---|
| Extract failing cases from test output | |
| Extract errors from lint output | |

### Review thresholds

- Maximum change size reviewable in one pass: (e.g. 400 changed lines)
- Paths excluded from review: (generated files, lock files, vendored code)

## 9. Stack-specific security

- Where environment variables / secrets live:
- Secure storage mechanism for sensitive client data:
- What's public vs. private in this stack (e.g. in web apps, anything that reaches the client bundle is public):

## 10. CI/CD and Deploy

- CI:
- Deploy:
