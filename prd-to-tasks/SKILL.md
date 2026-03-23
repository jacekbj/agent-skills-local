---
name: prd-to-tasks
description: Break a PRD into independently-grabbable task files using tracer-bullet vertical slices. Use when user wants to convert a PRD to tasks, create implementation tickets, or break down a PRD into work items.
---

# PRD to Tasks

Break a PRD into independently-grabbable task files using vertical slices (tracer bullets).

## Process

### 1. Locate the PRD

Ask the user for the PRD file path. PRDs are typically stored in `./docs/prds/`.

If the PRD is not already in your context window, read it with the Read tool.

### 2. Explore the codebase (optional)

If you have not already explored the codebase, do so to understand the current state of the code.

### 3. Draft vertical slices

Break the PRD into **tracer bullet** tasks. Each task is a thin vertical slice that cuts through ALL integration layers end-to-end, NOT a horizontal slice of one layer.

Slices may be 'HITL' or 'AFK'. HITL slices require human interaction, such as an architectural decision or a design review. AFK slices can be implemented and merged without human interaction. Prefer AFK over HITL where possible.

<vertical-slice-rules>
- Each slice delivers a narrow but COMPLETE path through every layer (schema, API, UI, tests)
- A completed slice is demoable or verifiable on its own
- Prefer many thin slices over few thick ones
</vertical-slice-rules>

### 4. Quiz the user

Present the proposed breakdown as a numbered list. For each slice, show:

- **Title**: short descriptive name
- **Type**: HITL / AFK
- **Blocked by**: which other slices (if any) must complete first
- **User stories covered**: which user stories from the PRD this addresses

Ask the user:

- Does the granularity feel right? (too coarse / too fine)
- Are the dependency relationships correct?
- Should any slices be merged or split further?
- Are the correct slices marked as HITL and AFK?

Iterate until the user approves the breakdown.

### 5. Create the task files

Create the `./docs/tasks/` directory if it doesn't exist. For each approved slice, create a Markdown file using a numbered slug (e.g. `./docs/tasks/01-setup-auth-schema.md`, `./docs/tasks/02-login-endpoint.md`). Use the template below.

Create files in dependency order (blockers first) so you can reference real file names in the "Blocked by" field.

<task-template>
## Parent PRD

[<prd-filename>](../prds/<prd-filename>)

## What to build

A concise description of this vertical slice. Describe the end-to-end behavior, not layer-by-layer implementation. Reference specific sections of the parent PRD rather than duplicating content.

## Acceptance criteria

- [ ] Criterion 1
- [ ] Criterion 2
- [ ] Criterion 3

## Blocked by

- Blocked by [<task-filename>](./<task-filename>) (if any)

Or "None - can start immediately" if no blockers.

## User stories addressed

Reference by number from the parent PRD:

- User story 3
- User story 7

</task-template>

Do NOT modify the parent PRD file.

After creating all task files, print a summary listing each file and its title.
