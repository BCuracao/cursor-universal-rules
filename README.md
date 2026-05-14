# The universal baseline for high-performance agentic coding

**Drop-in Cursor rules and persona defaults** so every repository gets the same senior-level discipline: read the tree first, change the smallest correct surface, prove fixes with evidence, and ship with tests and safe commits.

**Live repo:** [github.com/BCuracao/cursor-universal-rules](https://github.com/BCuracao/cursor-universal-rules)

---

## Why this exists

### The problem: context drift

Agents inherit **whatever happens to be in the chat window**. Without durable project law, behavior drifts: wrong dependency versions, mystery refactors, vague commits, skipped tests, and “helpful” essays instead of diffs. That is **context drift**—the model optimizes for plausibility, not for *your* stack, *your* patterns, or *your* risk profile.

### The fix: a senior-architect guardrail

This repo encodes **non-negotiables in repo-local files** (`.cursorrules` + `.cursor/rules/*.mdc`). Together they act like a staff engineer sitting on every session: **local-first**, **evidence-based debugging**, **manifest-grounded imports**, **bounded file and function size**, and **Conventional Commits**—so LLM output stays aligned with how we actually build software.

---

## Features

| Rule file | What it enforces |
|-----------|-------------------|
| `code-standards.mdc` | DRY, SOLID, early exits; ~20-line function ceiling; modularize instead of sprawl |
| `tech-discovery.mdc` | Read `package.json`, `pom.xml`, `go.mod`, etc. **before** adding imports or APIs |
| `modular-architecture.mdc` | ~250-line file target; decomposition plan before growing files further |
| `debug-protocol.mdc` | **Hypothesis → evidence → fix**; no blind guessing or drive-by refactors while debugging |
| `git-and-commits.mdc` | [Conventional Commits](https://www.conventionalcommits.org/); offer a copy-paste commit after coherent work |
| `testing-and-safety.mdc` | TDD bias; **no hardcoded secrets**; basic unit coverage for new logic; performance/import hygiene |
| `communication-and-docs.mdc` | “We” voice; JSDoc/docstrings on new functions; brief technical explanations |
| `project-journal.mdc` | After milestones, **offer** to append `PROJECT_JOURNAL.md` (running narrative of shipped work and risk) |

Plus **`PROJECT_JOURNAL.md`**: a lightweight template for dated action, debt, and next steps.

---

## Before vs. after

| Without these rules | With these rules |
|--------------------|------------------|
| Guesses library versions and import paths from training data | Opens **`package.json` / lockfile / build manifest** and matches what the repo actually uses |
| “Try restarting the server” loops | States a **hypothesis**, cites **stack trace / test / log line**, then applies a **minimal fix** |
| 400-line “god files” and 80-line functions | **Splits** work when files or functions exceed agreed ceilings |
| `git commit -m "updates"` | **`feat:` / `fix:` / `chore:`** messages and atomic intent |
| Keys pasted into source for a quick test | **Refuses** hardcoded secrets; uses env / existing secret patterns |

---

## Quick install

**Copy rules (and optional persona file) into the current project** with a one-liner:

```bash
git clone --depth 1 https://github.com/BCuracao/cursor-universal-rules.git /tmp/cursor-universal-rules && mkdir -p .cursor && cp -R /tmp/cursor-universal-rules/.cursor/rules .cursor/ && cp -f /tmp/cursor-universal-rules/.cursorrules . && rm -rf /tmp/cursor-universal-rules
```

- **Rules only** (if you already have `.cursorrules`):  
  `git clone --depth 1 https://github.com/BCuracao/cursor-universal-rules.git /tmp/cursor-universal-rules && mkdir -p .cursor && cp -R /tmp/cursor-universal-rules/.cursor/rules .cursor/ && rm -rf /tmp/cursor-universal-rules`

Then **commit** `.cursor/rules/`, `.cursorrules`, and optionally `PROJECT_JOURNAL.md` in the consuming repo so the whole team shares the same defaults.

---

## Usage

- **`.cursorrules` (repo root)** — **Persona and global operating mode**: senior architect, concise, local-first, no apology loops, read context before inventing files.
- **`.cursor/rules/*.mdc`** — **Specific logic**: coding standards, discovery, architecture limits, debug protocol, git, testing, communication, journal discipline. Each file uses YAML frontmatter (`name`, `description`, `globs: "*"`) so Cursor can load them consistently.

Optional: copy **`PROJECT_JOURNAL.md`** to the consumer project root if we want the same milestone log template.

---

## Philosophy

High signal-to-noise: smallest correct change, verifiable success, no speculative abstractions—in the spirit of practical LLM-assisted discipline (e.g. [Karpathy-style coding discipline](https://github.com/forrestchang/andrej-karpathy-skills)).

---

## License

Add a license in the consuming project as needed. This template repository ships without an implicit license until we add one here.
