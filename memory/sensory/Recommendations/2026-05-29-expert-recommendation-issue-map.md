# Expert Recommendation Issue Map

## Purpose

Starter issue map for GremTech.

Use this file to map overlapping expert findings, preserve conflicts, and avoid
creating duplicate recommendation notes for the same underlying issue.

## Current Issues

### GRM-ALFRED-001

- summary: Alfred-class proof truth is stronger than one generic green status
  and needs explicit classification across CI, synthetic smoke, and supported
  operator proof.
- status: open
- overlap type: additive
- related notes:
  - `docs/alfred-read-only-recommendations-pass-02.md`
  - `docs/alfred-read-only-recommendations-pass-03.md`
- next durable target:
  - `governance/standards/proof-path-classification-standard.md`
  - `templates/proof-path-register.json`

### GRM-ALFRED-002

- summary: Compatibility shims, redirects, and post-release cleanup candidates
  need explicit staged retirement instead of ad hoc subtraction.
- status: open
- overlap type: additive
- related notes:
  - `docs/alfred-read-only-recommendations-pass-02.md`
  - `delivery/work-packages/alfred-class-platform-blueprint/candidate-simplification-zones-2026-06-08.md`
- next durable target:
  - `governance/standards/compatibility-retirement-standard.md`
  - `skills/registry/compatibility-retirement-planner/SKILL.md`

### GRM-ALFRED-003

- summary: Complex operator UI route truth should not stay split across README
  prose, router code, and route-smoke logic.
- status: open
- overlap type: additive
- related notes:
  - `docs/alfred-read-only-recommendations-pass-03.md`
- next durable target:
  - `governance/standards/operator-route-contract-standard.md`
  - `templates/operator-route-contract.json`

### GRM-PLATFORM-001

- summary: GremTech still needs the first generic Alfred-class runtime core and
  its implementation host decision before the class becomes executable rather
  than descriptive.
- status: open
- overlap type: additive
- related notes:
  - `docs/alfred-class-platform-blueprint.md`
  - `docs/alfred-class-runtime-gap-analysis.md`
  - `delivery/work-packages/alfred-class-platform-blueprint/core-milestone-plan.md`
- next durable target:
  - future dedicated Alfred-class implementation repo
  - `skills/registry/governed-runtime-core-builder/SKILL.md`

## Update Rule

When a new recommendation overlaps an existing issue:
- update this file
- link the overlapping note
- record whether the overlap is duplicate, partial, conflicting, or additive
