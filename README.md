# general-agent-rules

Gold-standard Cursor agent rules for high-performance, efficient, and safe agentic coding. Copy into any project to align the agent on architecture, discovery, testing, and communication.

## How to use

Copy the `.cursor/rules/` folder and the `.cursorrules` file into your project root. If the project already has `.cursor/`, merge `rules/` without dropping existing rules.

In short:

1. Copy `.cursor/rules/` → `<your-project>/.cursor/rules/` (merge if needed).
2. Copy `.cursorrules` → `<your-project>/.cursorrules`.

Optional: read `PROJECT_JOURNAL.md` for a lightweight change log template you can adopt in this repo or downstream projects.

## Contents

| Path | Purpose |
|------|---------|
| `.cursorrules` | Global persona: senior architect, concise, local-first |
| `.cursor/rules/*.mdc` | Scoped rules: standards, discovery, architecture, debug, git, testing, docs |

## Conventions

Rules use [Conventional Commits](https://www.conventionalcommits.org/) for agent-assisted commits and favor evidence-based debugging over guessing.
