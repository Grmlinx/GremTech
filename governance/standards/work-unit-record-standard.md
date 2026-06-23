# Work Unit Record Standard

## Purpose

Define the durable record model for governed repos whose live work must not
depend on chat continuity alone.

`Work unit` is the generic term here.

Examples:

- case
- task
- investigation
- engagement
- project run

## Core Rule

If a repo coordinates meaningful multi-step work, it should preserve a durable
record set for each work unit.

The record set should be sufficient for a fresh human or AI session to
understand:

- what the unit is
- what happened
- what remains
- what was decided
- what outputs exist
- what limitations still apply

## Required Record Categories

Every governed work-unit model should define durable places for:

- intake or request framing
- action log
- decision log
- errors and recoveries
- invariant or quality checks
- derived outputs or exports
- current status
- run-end or closeout state

Add domain-specific records when needed, such as:

- custody or transfer logs
- evidence manifests
- findings trace
- approval records
- workflow status

## Placement Rule

The work-unit record set should live with the work unit, not in chat history.

Repo-global governance, standards, and templates remain in the repo.
Live unit records stay in the unit-local surface.

## Boundary Rule

The durable record set should prefer:

- derived records
- structured status
- decision rationale
- safe operational metadata

It should not casually absorb:

- secrets
- tokens
- arbitrary chat transcripts as system of record
- raw source material when the repo's boundary forbids it

## Fresh-Session Rule

A fresh session should be able to resume responsibly from the durable record
set without hidden dependence on prior conversation state.

## Machine-Readable Rule

When validators or review tools depend on the record model, define a
machine-readable catalog of the required record set.

Use `templates/work-unit-record-set.json` as the seed shape.

## Related Navigation

- [Governed AI product platform standard](governed-ai-product-platform-standard.md)
- [Machine-readable control surface standard](machine-readable-control-surface-standard.md)
- [Validation and readiness standard](validation-and-readiness-standard.md)
