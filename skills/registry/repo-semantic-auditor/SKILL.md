---
name: repo-semantic-auditor
description: Audit governed repositories for semantic drift across startup contracts, documentation, machine-readable catalogs, validators, operator surfaces, release posture, and review contracts. Use when evaluating Alfred-class repos, preparing governance or adoption recommendations, or checking whether prose, control files, and runtime behavior still align.
---

# Repo Semantic Auditor

## Purpose

Audit a repo for cross-surface truth drift, not just syntax or test failures.

## Workflow

1. Start with the repo's claimed truth.
   Read the startup contract, top-level README, current-state or posture notes,
   and any surface manifest or system overview first.
2. Locate the canonical machine-readable control files.
   Prefer catalogs, manifests, policy JSON, route maps, release records, and
   documentation-sync contracts over scattered prose.
3. Compare those claims against the real implementation surfaces.
   Inspect validators, root CLI or runtime entrypoints, API/UI boundaries,
   worker or job surfaces, and approval-bearing execution paths.
4. Classify the gaps precisely.
   Use categories such as semantic drift, support-state confusion,
   compatibility residue, missing proof, boundary ambiguity, or maintainability
   pressure.
5. Recommend durable promotion targets.
   Prefer standards, templates, docs, skill packs, or machine-readable control
   files over chat-only conclusions.

## Focus Areas

- startup and operator-surface contracts
- docs versus runtime behavior
- validator coverage versus claimed guarantees
- release posture and support-state language
- machine-readable control surfaces versus prose
- proof-path and route-contract surfaces versus scattered claims
- compatibility paths and fallback lanes
- derived-review boundaries versus source-data boundaries

## Output

Produce:

- an executive verdict
- prioritized findings with evidence
- specific recommendation targets inside the repo
- a note on what appears load-bearing and should not be stripped casually

## Boundaries

Do not:

- treat every compatibility surface as a defect
- assume a green test suite proves support posture
- recommend subtractive cleanup without checking what proof or support surface
  still depends on it
- blur source-data handling, review surfaces, and authority-bearing execution

## References

Read these when working in `GremTech`:

- [../../../docs/alfred-read-only-assessment.md](../../../docs/alfred-read-only-assessment.md)
- [../../../docs/alfred-read-only-recommendations-pass-02.md](../../../docs/alfred-read-only-recommendations-pass-02.md)
- [../../../docs/alfred-read-only-recommendations-pass-03.md](../../../docs/alfred-read-only-recommendations-pass-03.md)
- [../../../governance/standards/machine-readable-control-surface-standard.md](../../../governance/standards/machine-readable-control-surface-standard.md)
- [../../../governance/standards/proof-path-classification-standard.md](../../../governance/standards/proof-path-classification-standard.md)
- [../../../governance/standards/operator-route-contract-standard.md](../../../governance/standards/operator-route-contract-standard.md)
- [../../../governance/standards/release-posture-standard.md](../../../governance/standards/release-posture-standard.md)
- [../../../governance/standards/compatibility-retirement-standard.md](../../../governance/standards/compatibility-retirement-standard.md)

## Validation

- verify that the claimed canonical surfaces were actually read
- verify that findings compare at least two different repo surfaces
- verify that recommendations identify a durable repo-owned target
