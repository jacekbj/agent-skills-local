# Agent Skills

A collection of agent skills that extend capabilities across planning, development, and tooling. All outputs are stored as local Markdown files in `./docs/` subdirectories — no external services required.

## Planning & Design

These skills help you think through problems before writing code.

- **write-a-prd** — Create a PRD through an interactive interview, codebase exploration, and module design. Saved to `./docs/prds/`.

- **prd-to-plan** — Turn a PRD into a multi-phase implementation plan using tracer-bullet vertical slices. Saved to `./plans/`.

- **prd-to-tasks** — Break a PRD into independently-grabbable task files using vertical slices. Saved to `./docs/tasks/`.

- **grill-me** — Get relentlessly interviewed about a plan or design until every branch of the decision tree is resolved.

- **design-an-interface** — Generate multiple radically different interface designs for a module using parallel sub-agents.

- **request-refactor-plan** — Create a detailed refactor plan with tiny commits via user interview. Saved to `./docs/refactors/`.

## Development

These skills help you write, refactor, and fix code.

- **tdd** — Test-driven development with a red-green-refactor loop. Builds features or fixes bugs one vertical slice at a time.

- **triage-issue** — Investigate a bug by exploring the codebase, identify the root cause, and save a report with a TDD-based fix plan. Saved to `./docs/issues/`.

- **improve-codebase-architecture** — Explore a codebase for architectural improvement opportunities, focusing on deepening shallow modules and improving testability. Saved to `./docs/rfcs/`.

- **migrate-to-shoehorn** — Migrate test files from `as` type assertions to @total-typescript/shoehorn.

- **scaffold-exercises** — Create exercise directory structures with sections, problems, solutions, and explainers.

## Tooling & Setup

- **setup-pre-commit** — Set up Husky pre-commit hooks with lint-staged, Prettier, type checking, and tests.

- **git-guardrails-claude-code** — Set up Claude Code hooks to block dangerous git commands (push, reset --hard, clean, etc.) before they execute.

## Writing & Knowledge

- **write-a-skill** — Create new skills with proper structure, progressive disclosure, and bundled resources.

- **edit-article** — Edit and improve articles by restructuring sections, improving clarity, and tightening prose.

- **ubiquitous-language** — Extract a DDD-style ubiquitous language glossary from the current conversation.

- **obsidian-vault** — Search, create, and manage notes in an Obsidian vault with wikilinks and index notes.
