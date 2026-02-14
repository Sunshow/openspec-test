# Spec: Project Baseline — openspec-test

## Module: OpenSpec Infrastructure

### SPEC-001: OpenSpec Directory Structure

> Given the project repository is initialized
> When a developer checks the openspec/ directory
> Then the following structure exists:
>   - openspec/config.yaml
>   - openspec/specs/ (Source of Truth)
>   - openspec/changes/ (active changes)
>   - openspec/changes/archive/ (archived changes)

### SPEC-002: Config File

> Given the openspec/config.yaml file exists
> When a developer reads the config
> Then it contains:
>   - schema: spec-driven
>   - context section describing the project
>   - rules section with per-artifact conventions

### SPEC-003: Spec Format Convention

> Given a spec file exists in openspec/specs/
> When a developer reads the spec
> Then each behavior is described in Given/When/Then format
> And each delta spec is tagged ADDED, MODIFIED, or REMOVED

### SPEC-004: Change Workflow

> Given a developer wants to propose a change
> When they create a new change directory under openspec/changes/<change-name>/
> Then it contains:
>   - proposal.md (motivation, scope, non-goals)
>   - specs/ directory with delta spec files
>   - design.md (technical approach, file changes)
>   - tasks.md (implementation checklist)

### SPEC-005: Archive Workflow

> Given a change has been fully implemented
> When the change is archived
> Then delta specs are merged into openspec/specs/ (Source of Truth)
> And the change directory is moved to openspec/changes/archive/
