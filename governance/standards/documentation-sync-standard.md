# Documentation Sync Standard

## Purpose

Define how `GremTech`-managed repos keep critical operator and maintainer docs
aligned with real behavior.

## Core Rule

When a change affects a critical entrypoint, update both:

- the implementation or runtime surface
- the documentation sync contract and protected docs for that surface

Critical behavior must not rely on chat memory, team habit, or a reviewer
remembering to update the right file later.

## Protected Surface Types

Treat these as documentation-sync candidates:

- `start.ai` or equivalent startup contracts
- primary `README.md` getting-started or operating instructions
- maintainer docs that define the first-run or release path
- operator-facing CLI examples and workflow docs
- repo structure notes when layout affects repeatability
- approval, escalation, or trust-boundary instructions
- recovery, rollback, or deployment entrypoints

Not every note needs sync enforcement.
High-friction or high-consequence surfaces do.

## Default Contract Pattern

The preferred repo-local contract path is:

- `governance/documentation-sync-contract.json`

Each protected entry should define:

- a stable surface id
- a description
- one or more checks
- the implementation surface or source of truth
- the docs that must stay aligned
- the validator command or check path
- any repo-archetype-specific notes

Use `templates/documentation-sync-contract.json` as the seed shape.

Each check may define:

- `path`
- `required_snippets`
- `forbidden_snippets`

Use required snippets to assert critical behavior is still described.
Use forbidden snippets to catch retired or disallowed instructions lingering in
protected docs.

## Validation Rule

If a repo defines a documentation sync contract, the validator for that repo
should check it during normal validation or readiness review.

The check may be simple at first.
It still needs to be durable, explicit, and runnable.

## Expansion Rule

Add a surface to the contract when:

- new users or maintainers repeatedly trip over drift there
- the surface is part of startup, release, or operator control
- the repo archetype depends on it for safe repeatability

Do not turn the contract into a blanket index of every markdown file.

## Promotion Rule

If a repo repeatedly changes behavior without updating critical docs, treat that
as a governance and QA problem, not as a writing problem.

## Related Navigation

- [Repo startup contract](repo-startup-contract.md)
- [Validation and readiness standard](validation-and-readiness-standard.md)
- [Workflow surface policy](workflow-surface-policy.md)
