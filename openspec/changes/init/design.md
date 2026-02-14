# Design: OpenSpec SDD Initialization

## Overview

This change establishes the OpenSpec Spec-Driven Development infrastructure for the `openspec-test` project. Since there is no existing application code, the focus is on setting up the SDD workflow itself.

## Technical Approach

### 1. Configuration

Update `openspec/config.yaml` to include:
- Project context (name, description, status, conventions)
- Per-artifact rules for proposal, specs, design, and tasks

### 2. Baseline Specs

Create `openspec/specs/project-baseline.spec.md` containing five foundational specs (SPEC-001 through SPEC-005) that define the expected behavior of the OpenSpec infrastructure:
- Directory structure
- Config file format
- Spec format conventions (Given/When/Then)
- Change workflow
- Archive workflow

### 3. Change Artifacts

Create the `init` change under `openspec/changes/init/` with:
- `proposal.md` — motivation and scope
- `specs/delta-project-baseline.spec.md` — all five specs tagged as ADDED
- `design.md` — this file
- `tasks.md` — implementation checklist

## Data Flow

```
Developer → creates change → openspec/changes/<name>/
  ├── proposal.md      (why & what)
  ├── specs/*.spec.md  (delta specs: ADDED/MODIFIED/REMOVED)
  ├── design.md        (how)
  └── tasks.md         (execution plan)

After implementation → archive:
  delta specs → merged into openspec/specs/ (Source of Truth)
  change dir  → moved to openspec/changes/archive/
```

## File Changes

| Action   | File                                                  |
|----------|-------------------------------------------------------|
| Modified | `openspec/config.yaml`                                |
| Created  | `openspec/specs/project-baseline.spec.md`             |
| Created  | `openspec/changes/init/proposal.md`                   |
| Created  | `openspec/changes/init/specs/delta-project-baseline.spec.md` |
| Created  | `openspec/changes/init/design.md`                     |
| Created  | `openspec/changes/init/tasks.md`                      |
