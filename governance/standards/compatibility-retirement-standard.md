# Compatibility Retirement Standard

## Purpose

Define how compatibility paths, fallback lanes, redirects, and migration shims
should be governed.

## Core Rule

Compatibility is allowed.
Permanent ambiguity is not.

If a repo keeps a compatibility or fallback surface, that surface should be:

- explicit
- justified
- owned
- removable

## Applies To

Use this standard for:

- legacy CLI flags or parameters
- fallback config resolution paths
- route redirects kept for migration
- mock or fixture modes retained after real backends exist
- older review or report inference paths kept for historical support
- compatibility wrappers around canonical workflow surfaces

## Required Ledger Fields

Each substantive compatibility surface should have a durable record with:

- surface name
- type
- canonical replacement
- why it still exists
- current support value
- known risk if removed too early
- owner
- validation or proof dependency
- exit criteria
- intended review cadence

This may live in a deprecation ledger, release record, repo surface manifest,
or equivalent governed control file.

## Product Rule

Compatibility paths should not silently become the normal path.

Operators and maintainers should be able to tell:

- what is current
- what is compatibility-only
- what is transition-only
- what is planned for retirement

## Retirement Rule

Remove a compatibility surface when:

- the supported callers have migrated
- the remaining support value is weak
- the replacement path is proven
- rollback or recovery remains possible without the old surface

Do not remove a compatibility surface only because it looks untidy.
Do not keep it forever because no one wrote the exit rule down.

## Anti-Patterns

Do not:

- hide compatibility paths inside normal product language
- keep fallbacks with no named owner
- let validation prove both the old and new path forever without deciding
  which one is canonical
- leave migration shims out of release posture and support-state review

## Review Rule

Compatibility surfaces should be reviewed during:

- release posture review
- readiness audits
- major route or startup contract changes
- post-release hardening or simplification work

## Related Navigation

- [Capability tiering standard](capability-tiering-standard.md)
- [Workflow surface policy](workflow-surface-policy.md)
- [Release posture standard](release-posture-standard.md)
- [Repo audit control standard](repo-audit-control-standard.md)
