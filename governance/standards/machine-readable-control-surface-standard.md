# Machine-Readable Control Surface Standard

## Purpose

Define when `GremTech` should express governance and runtime-critical behavior
in machine-readable form instead of prose only.

## Core Rule

If a surface is meant to be:

- validated repeatedly
- consumed by tooling
- routed by runtime logic
- compared across repos
- treated as a durable source of truth

then prose alone is not enough.

Add a machine-readable companion surface.

## Good Candidates

Use machine-readable control surfaces for:

- workflow routing maps
- role activation matrices
- repo registries and repo profiles
- tool catalogs and support-state inventories
- documentation-sync contracts
- startup or entrypoint manifests
- risk, assurance, or provider inventories
- release posture summaries when runtime or dashboards need them

## Pairing Rule

The preferred pattern is:

- markdown explains meaning, boundaries, and human intent
- JSON or another structured format carries stable fields for validators,
  automation, or future runtime code

Neither replaces the other.

## Minimum Expectations

A machine-readable control surface should usually include:

- schema or contract version
- stable ids
- explicit status values
- owner or governing role
- relevant source paths or surface bindings
- validation or review notes when they matter

## Validation Rule

Machine-readable control surfaces should be:

- syntactically valid
- semantically constrained where practical
- checked during repo validation or readiness review

Do not add a JSON artifact that no one validates and no process actually uses.

## Scope Discipline

Do not build catalogs because catalogs feel sophisticated.

Use them when they reduce ambiguity, support validation, or let future runtime
code stay aligned with policy.

## Repo Archetype Rule

Different repo types need different levels of structure:

- lightweight CLI tools may need only a small support-state inventory and doc
  sync contract
- infrastructure repos may need environment or service inventories and change
  posture records
- governed AI or orchestration repos may justify richer routing, assurance, and
  policy registries

## Related Navigation

- [Validation and readiness standard](validation-and-readiness-standard.md)
- [Documentation sync standard](documentation-sync-standard.md)
- [Release posture standard](release-posture-standard.md)
- [Harness portability standard](harness-portability-standard.md)
