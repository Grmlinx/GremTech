# Proof Path Classification Standard

## Purpose

Define how `GremTech`-managed repos classify multiple proof surfaces so a green
status does not imply more than it actually proves.

## Core Rule

If a repo has more than one validation, smoke, build, or readiness path, each
path must be classified explicitly.

Do not collapse:

- structural validation
- synthetic operator smoke
- supported operator proof
- environment-bound proof
- compatibility-only proof
- historical proof

into one vague "validated" state.

## Required Classes

Use these proof classes unless a repo has a stronger justified vocabulary:

- `structural-validation`
  - lint, typecheck, schema validation, build validation, catalog validation
- `synthetic-operator-smoke`
  - non-destructive proof through the real entrypoint with synthetic or bounded
    state
- `supported-operator-proof`
  - the normal supported maintainer or operator proof lane for a feature or
    surface
- `environment-bound-proof`
  - proof that depends on Docker, a tenant, a host profile, a lab, or another
    environment outside normal fast CI
- `compatibility-proof`
  - proof for a transition-only, legacy, fallback, or migration surface
- `historical-proof`
  - retained record of a past proof milestone that is no longer a live support
    requirement

## Required Fields

Repos with multiple meaningful proof paths should maintain a machine-readable
proof-path register.

Each entry should usually state:

- stable id
- human summary
- proof class
- support state
- entrypoint or command
- execution venue such as `ci`, `local`, `container`, `tenant`, or `lab`
- prerequisite versions or dependencies when material
- surfaces or claims validated
- whether the path is required for release or only for hardening
- durable evidence record path when the proof is not always automated

## Support-State Rule

Every proof path should also carry an explicit support state such as:

- `supported`
- `maintainer-required`
- `transition-only`
- `blocked`
- `historical`

That prevents a successful fallback or convenience path from being mistaken for
the supported truth.

## CI Rule

CI should run every proof path that is:

- deterministic
- safe
- available in the CI venue

When the supported proof lane cannot run in CI, the repo must:

- say so explicitly
- record where that proof does run
- treat it as a separate required gate when it remains release-relevant

Do not let CI green status silently stand in for stronger supported proof that
never ran.

## Documentation Sync Rule

Startup guides, release notes, onboarding docs, and readiness summaries should
point to the same proof-path vocabulary.

If one surface says a proof lane is supported and another surface treats it as
optional, the repo has proof-path drift.

## Promotion Rule

Promote a proof path into a shared portfolio standard only when:

- it has been executed successfully
- its prerequisites are understandable
- its support-state language is stable
- it improves truth clarity for future repos

## Related Navigation

- [Validation and readiness standard](validation-and-readiness-standard.md)
- [Release posture standard](release-posture-standard.md)
- [Documentation sync standard](documentation-sync-standard.md)
- [Machine-readable control surface standard](machine-readable-control-surface-standard.md)
