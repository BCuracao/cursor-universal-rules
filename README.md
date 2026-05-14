# cursor-universal-rules

Plug-and-play baseline rules for **agentic coding** with Cursor. These files encode how we want the AI to write, test, commit, and communicate so behavior stays consistent across repositories.

## How to use this repo

1. Copy the contents of `.cursor/rules/` from this repository into **your new project’s** `.cursor/rules/` directory (create `.cursor/rules/` if it does not exist).
2. Copy `PROJECT_JOURNAL.md` into the project root if we want the same milestone tracking template.
3. Commit those files in the consuming project so the whole team shares the same agent defaults.

We treat `.cursor/rules/*.mdc` as **project law** for the agent: short, high-signal instructions that apply globally unless we scope them with globs.

## What’s inside

| Path | Purpose |
|------|---------|
| `.cursor/rules/code-quality.mdc` | DRY, SOLID, early exits, ~20-line function guidance |
| `.cursor/rules/communication-style.mdc` | Concise “we” voice; **Why** before large changes |
| `.cursor/rules/git-workflow.mdc` | Atomic commits + Conventional Commits |
| `.cursor/rules/efficiency-and-safety.mdc` | Secrets, performance, imports |
| `.cursor/rules/testing-first.mdc` | TDD bias; confirm where tests live first |
| `.cursor/rules/project-journal.mdc` | Offer to append `PROJECT_JOURNAL.md` after milestones |
| `PROJECT_JOURNAL.md` | Dated log template for tasks, state, debt, and next steps |

## Philosophy

These rules align with a **high signal-to-noise** mindset: think before coding, prefer the smallest correct change, define verifiable success, and avoid speculative abstractions—in the spirit of practical guidelines for LLM-assisted development (e.g. [Karpathy-style coding discipline](https://github.com/forrestchang/andrej-karpathy-skills)).

## License

Add a license in the consuming project as needed. This template repository ships without an implicit license until we add one.
