# Release Posture Standard

## Purpose

Define how a governed repo states what is actually ready, what remains bounded,
and what still requires human approval or maintainer control.

## Core Rule

Do not describe a repo or feature as simply "ready" or "not ready" when the
real answer is more nuanced.

Use an explicit release posture that separates:

- what is supported
- what is unsupported
- what is approval-required
- what is maintainer-required
- what is blocked

## Why

This avoids the most common governance failure in growing repos:
capability is implied by existence instead of being stated by policy and proof.

## Required Sections

A substantive release or adoption decision should include:

- decision type
- decision status
- supported
- unsupported
- approval-required
- maintainer-required
- blocked
- evidence
- risk acceptance
- required before wider rollout

Not every repo needs every section in the same depth.
Every serious rollout needs the categories.

## Category Meaning

- `supported`
  - the repo can do this within the stated boundaries and proof basis
- `unsupported`
  - the repo must not present this as a supported capability
- `approval-required`
  - the capability may exist but cannot be used without explicit human
    authority
- `maintainer-required`
  - the capability may exist but changes or operation require maintainer-level
    control
- `blocked`
  - the repo must refuse or clearly prevent this path until conditions change

## Evidence Rule

Every non-trivial posture claim should point to evidence such as:

- gate checklists
- QA records
- smoke proof
- validation output
- audit runs
- governance decisions

## Risk Rule

Risk acceptance must be written explicitly.

Do not blur accepted limitations together with supported capability.

## Rollout Rule

If a repo is accepted only for a bounded rollout, say so plainly.

Do not let "internal", "pilot", "alpha", "beta", or "experimental" stand in
for real boundary language.

## Related Navigation

- [Validation and readiness standard](validation-and-readiness-standard.md)
- [Repo audit control standard](repo-audit-control-standard.md)
- [Work package standard](work-package-standard.md)
