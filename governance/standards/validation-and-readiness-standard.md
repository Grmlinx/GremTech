# Validation And Readiness Standard

## Purpose

Define how `GremTech`-managed repos prove that a change is ready through
executable evidence instead of prose alone.

## Core Rule

If a change affects runtime behavior, operator paths, automation, CI, release
behavior, startup contracts, or trust boundaries, it must produce layered proof
before it is treated as durable repo truth.

Documentation is necessary.
Documentation is not proof.

## Required Proof Layers

1. structural validation
   - lint, typecheck, schema validation, catalog validation, or build checks
   - fail on malformed machine-readable surfaces before deeper testing starts
2. readiness or doctor checks
   - verify required files, expected repo surfaces, and declared prerequisites
   - report blocked or partial states explicitly instead of implying readiness
3. operator-path smoke
   - exercise the primary user-facing path in a non-destructive or synthetic way
   - prefer going through the real CLI, UI, or repo entrypoint rather than a
     private helper
4. gate status
   - expose blockers, unchecked gate items, risk acceptances, and known limits
   - do not collapse unresolved readiness gaps into a green status
5. release or adoption decision
   - state whether the change is accepted, deferred, blocked, or accepted with
     conditions
   - record evidence references and follow-up obligations

## Proof Design Requirements

- keep smoke execution non-destructive by default
- use isolated scratch or synthetic roots for temporary smoke data
- bound smoke steps with timeouts where hangs are plausible
- fail closed when required inputs, policies, or catalogs are missing
- surface partial or not-ready states honestly
- keep the validation path visible to maintainers and reviewers
- prefer machine-readable output for gates and status where practical

## Validator Expectations

Strong validators should check more than syntax.

Where relevant, also validate:

- critical required files or surfaces exist
- trust-boundary assumptions still hold
- startup or workflow docs still match the real entrypoint
- prohibited patterns are absent from protected surfaces
- support-state, catalog, or contract files reference real paths

The goal is to catch drift in behavior, not just malformed JSON.

## Status Surface Rule

Readiness or gate status should expose:

- overall `ok` or equivalent state
- blockers
- warnings or hardening items
- unchecked gate items
- evidence references
- explicit scope of what the status does and does not mean

Do not compress all of that into a single green/red result.

## Evidence Expectations

Use the smallest evidence set that still proves the claim:

- CLI and operator tools
  - command help, static validation, build or package validation where
    relevant, and smoke coverage of the main task path
- UI and full-stack repos
  - lint, typecheck, build, integration smoke, and accessibility or UX checks
    when the change is user-facing
- infrastructure repos
  - syntax validation, dry runs, plan output, post-change verification steps,
    and recovery-aware runbook checks
- governed AI or runtime-control repos
  - startup-contract validation, catalog validation, approval-boundary checks,
    and smoke proof that sensitive paths stay gated

## Artifact Rule

Substantive work should emit or update:

- `qa-gate.md`
- `gate-checklist.md`
- `release-decision.md`
- repo-local validation scripts or CI workflow definitions when they exist
- machine-readable status or contract surfaces when the repo depends on them

When critical entrypoints changed, also run the documentation-sync check
defined in `documentation-sync-standard.md`.

## CI Rule

If a repo has CI, structural validation should run on pull requests and primary
delivery branches.

Operator-path smoke should run in CI when it is deterministic, safe, and does
not require privileged or external state.

Heavier environment, platform, tenant, or infrastructure checks may stay as
explicit pre-release or pre-deployment gates, but they still need a durable
record.

## Promotion Rule

Do not promote a pattern into a shared standard, template, or startup contract
because it was described well.

Promote it because it was proven, reviewed, and remained understandable after
proof.

## Related Navigation

- [Development lifecycle](development-lifecycle.md)
- [Documentation sync standard](documentation-sync-standard.md)
- [External framework alignment](external-framework-alignment.md)
- [Work package standard](work-package-standard.md)
