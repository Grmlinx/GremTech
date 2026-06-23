# Workflow Surface Policy

## Purpose

Define where canonical workflow behavior should live.

This standard is inspired by skills-first systems such as
`everything-claude-code`, but it is adapted to the broader portfolio model used
here.

## Canonical First

New workflow contributions should land in the most durable canonical surface
first.

For `GremTech`, that usually means:

- `governance/standards/`
- `docs/`
- `skills/`
- `portfolio/`
- `templates/`

For target repos, that may mean:

- `skills/`
- `runbooks/`
- `governance/`
- `docs/`
- `templates/`

## Compatibility Surfaces

Compatibility surfaces are allowed, but they are secondary.

Examples:
- slash commands
- harness-local command files
- plugin wrappers
- legacy shims
- thin launchers

These should point to canonical behavior, not compete with it.

## Promotion Rule

When a new workflow is proposed:

1. define the durable behavior once
2. place it in the canonical source surface
3. add adapter or shim entrypoints only where needed
4. document any harness-specific limitations explicitly

## Anti-Patterns

- command-first sprawl with no canonical source
- duplicate workflow definitions across harness folders
- burying durable process rules in transient command wrappers
- adding a second competing orchestration surface instead of strengthening the existing one

## Review Rule

Any new compatibility surface should answer:

- what canonical source does this wrap
- why is a shim needed
- what would break if the shim disappeared

If those answers are weak, do not add the shim.
