# Proposal: Initialize OpenSpec SDD Environment

## Motivation

The project `openspec-test` currently has no structured specification or development workflow. To enable Spec-Driven Development (SDD), we need to establish the OpenSpec infrastructure as the foundation for all future changes.

This initialization ensures that:
- Every feature and change is traceable through specs
- The team has a single Source of Truth for system behavior
- Changes follow a consistent proposal → spec → design → tasks workflow

## What

- Configure `openspec/config.yaml` with project context and artifact rules
- Create baseline specs documenting the OpenSpec infrastructure itself (directory structure, config format, spec conventions, change workflow, archive workflow)
- Establish the `init` change as the first tracked change in the project

## Impact

- **New files**: `openspec/config.yaml` (updated), `openspec/specs/project-baseline.spec.md`, all artifacts under `openspec/changes/init/`
- **Existing code**: No application code is affected — this is purely infrastructure
- **Process**: All future development should follow the OpenSpec SDD workflow

## Non-goals

- This change does not introduce any application code or features
- This change does not define specs for features that don't exist yet
- This change does not enforce CI/CD integration with OpenSpec (that can come later)
