# cursor-universal-rules

Plug-and-play baseline rules for **agentic coding** with Cursor. We encode how the AI writes, tests, commits, and communicates so behavior stays consistent across repositories.

**Repository:** [BCuracao/cursor-universal-rules](https://github.com/BCuracao/cursor-universal-rules)

```bash
git clone https://github.com/BCuracao/cursor-universal-rules.git
```

## How to use

Copy the `.cursor/rules/` folder and the `.cursorrules` file into your project root. If the project already has `.cursor/`, merge `rules/` without dropping existing rules.

1. Copy `.cursor/rules/` → `<your-project>/.cursor/rules/` (merge if needed).
2. Copy `.cursorrules` → `<your-project>/.cursorrules`.
3. Optionally copy `PROJECT_JOURNAL.md` for milestone tracking; commit copied files in the consuming project so the team shares the same agent defaults.

We treat `.cursor/rules/*.mdc` as **project law**: short, high-signal instructions (default `globs: "*"` unless we scope further).

## What’s inside

| Path | Purpose |
|------|---------|
| `.cursorrules` | Global persona: senior architect, concise, local-first |
| `.cursor/rules/code-standards.mdc` | DRY, SOLID, early exits; ~20-line function guidance |
| `.cursor/rules/tech-discovery.mdc` | Read manifests before imports; align to installed versions |
| `.cursor/rules/modular-architecture.mdc` | ~250-line file target; decomposition before sprawl |
| `.cursor/rules/debug-protocol.mdc` | Hypothesis → evidence → fix; no blind guessing |
| `.cursor/rules/git-and-commits.mdc` | Conventional Commits; suggested commit after tasks |
| `.cursor/rules/testing-and-safety.mdc` | TDD bias; no secrets; basic unit coverage for new logic |
| `.cursor/rules/communication-and-docs.mdc` | “We” voice; JSDoc/docstrings on new functions |
| `.cursor/rules/project-journal.mdc` | After milestones, offer to append `PROJECT_JOURNAL.md` |
| `PROJECT_JOURNAL.md` | Dated log template |

## Philosophy

High signal-to-noise: think before coding, smallest correct change, verifiable success, avoid speculative abstractions—aligned with practical LLM-assisted discipline (e.g. [Karpathy-style coding discipline](https://github.com/forrestchang/andrej-karpathy-skills)).

## Conventions

[Conventional Commits](https://www.conventionalcommits.org/) for agent-assisted commits; evidence-based debugging over guessing.

## License

Add a license in the consuming project as needed. This template ships without an implicit license until we add one here.
