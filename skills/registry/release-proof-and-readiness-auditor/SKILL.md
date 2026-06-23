---
name: release-proof-and-readiness-auditor
description: Evaluate whether a repo's claimed release or readiness state is supported by executable proof, documentation-sync, supported-path classification, fallback and compatibility state, and QA evidence. Use when assessing rollout decisions, production posture, support claims, or readiness gates for governed tools and Alfred-class systems.
---

# Release Proof And Readiness Auditor

## Purpose

Audit the truth of a release claim.

## Workflow

1. Read the claimed release posture first.
   Find the current support-state, readiness, or production-promotion summary.
2. Identify the required proof paths.
   Look for validators, smoke checks, route checks, build steps, readiness
   profiles, CI jobs, and documented support boundaries.
3. Separate supported proof from incidental proof.
   Distinguish supported operator or maintainer paths from local convenience
   paths, mock paths, and compatibility-only paths.
4. Check documentation-sync on critical entrypoints.
   If startup, approval, review, or operator surfaces changed, confirm the
   docs and sync contracts match the implementation.
5. Classify the verdict using real support language.
   Prefer supported, approval-required, maintainer-required, blocked, or
   degraded over vague maturity labels.

## Focus Areas

- executable proof versus prose-only confidence
- supported proof path versus unsupported local path
- CI proof versus operator-path proof
- proof-path register presence versus ad hoc proof vocabulary
- validation coverage over startup, approval, and review surfaces
- compatibility and fallback lanes that still affect release truth

## Output

Produce:

- current claimed state
- proof surfaces reviewed
- proof gaps or contradictions
- support-state recommendation
- post-release hardening items where needed

## Boundaries

Do not:

- treat unexecuted inventory as proof
- confuse a passing fallback path with a supported release path
- flatten maintainer-only or transition-only paths into normal support
- recommend release confidence without checking the canonical readiness record

## References

Read these when working in `GremTech`:

- [../../../governance/standards/validation-and-readiness-standard.md](../../../governance/standards/validation-and-readiness-standard.md)
- [../../../governance/standards/documentation-sync-standard.md](../../../governance/standards/documentation-sync-standard.md)
- [../../../governance/standards/release-posture-standard.md](../../../governance/standards/release-posture-standard.md)
- [../../../governance/standards/proof-path-classification-standard.md](../../../governance/standards/proof-path-classification-standard.md)
- [../../../governance/standards/compatibility-retirement-standard.md](../../../governance/standards/compatibility-retirement-standard.md)
- [../../../docs/alfred-read-only-recommendations-pass-02.md](../../../docs/alfred-read-only-recommendations-pass-02.md)
- [../../../docs/alfred-read-only-recommendations-pass-03.md](../../../docs/alfred-read-only-recommendations-pass-03.md)

## Validation

- verify that every verdict cites an actual proof surface
- verify that CI proof is not silently treated as supported-proof coverage when
  the repo says otherwise
- verify that supported-path claims distinguish normal from compatibility-only
  execution
- verify that missing proof is recorded as a gap, not implied away
