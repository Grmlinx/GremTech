# Harness Portability Standard

## Purpose

Define how portfolio workflows should travel across AI harnesses without
forking the operating model for every tool.

This standard is inspired by cross-harness systems such as
`everything-claude-code`, but adapted for `GremTech`'s governance-first model.

## Core Rule

Put durable behavior in shared repo-owned source surfaces.
Adapt loading, packaging, and event shape only at the harness edge.

## Shared Source Surfaces

Use shared source surfaces for durable behavior such as:

- governance rules and standards
- startup contracts
- templates
- runbooks
- skills or equivalent reusable workflow definitions
- machine-readable target registries

## Edge Adapter Surfaces

Harness-specific files should be thin adapters only.

Examples:
- `AGENTS.md`
- `.codex/`
- `.claude/`
- `.cursor/`
- `.opencode/`
- plugin manifests
- harness-local hook config

These should define:
- how the shared asset is loaded
- how events are mapped
- how approvals or sandbox settings are expressed

They should not become the only place a workflow is defined.

## Recommended Context Surfaces

For repos that need cross-harness support, prefer this stack:

- `README.md`
  - human front door
- `start.ai`
  - canonical repo AI startup contract
- `AGENTS.md`
  - cross-harness universal instruction bridge when useful
- harness-local config
  - adapter-only behavior

## Memory And Hook Rule

When adding session persistence, hooks, or continuity aids:

- keep persistence local by default
- keep context bounded
- allow opt-out or disablement
- avoid secret-bearing or privacy-unsafe persistence
- document the lifecycle contract clearly

Do not make hosted transcript capture or opaque background persistence the
default.

## Duplication Test

If a workflow change requires editing multiple harness copies of the same
behavior, the durable source is in the wrong place.

Move the durable logic back into:
- shared docs
- a shared skill
- a shared template
- a shared standards file

Then keep only the harness adapter thin.
