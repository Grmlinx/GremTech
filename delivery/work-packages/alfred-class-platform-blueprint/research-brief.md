# Research Brief

## Objective

Determine the minimum generic architecture required to recreate an Alfred-class
platform from `GremTech`.

## Current Truth

- `GremTech` already has a strong contract layer
- `GremTech` does not yet have a runtime or product layer
- `alfred` demonstrates the target architecture class most clearly in the
  portfolio
- `alfred` must remain untouched and reference-only in this effort

## Desired Future State

`GremTech` should be able to:

- describe an Alfred-class platform precisely
- distinguish core platform layers from optional domain packs
- create a future implementation repo or pilot from a governed blueprint

## Similar Projects And References

- local benchmark:
  - `alfred`
    - useful: operator surfaces, control-plane state, worker model, proof gates,
      release posture, and repo-audit loop
    - do not copy: Alfred-specific forensic workflow depth as mandatory core
- portfolio governance analogue:
  - `GremTech`
    - useful: standards, templates, work packages, role activation, and
      learning loop
    - do not copy: standards-only maturity as a substitute for runtime maturity

## Patterns To Borrow Or Reject

- borrow:
  - generic governed runtime core
  - typed approval-bearing execution
  - machine-readable policy where validators or runtime rely on it
  - read-only review surfaces for browser/API layers
- reject:
  - file-by-file imitation
  - universalizing one domain pack as the only product shape

## Evidence

- read-only benchmark pass over Alfred startup, operator-surface, validator,
  smoke, release, audit, platform API, WebUI, workflow profile, tool catalog,
  and adapter registry surfaces
- current `GremTech` standards, templates, work-package model, and capability
  model

## Constraints

- no writes to `alfred`
- keep the future core generic
- do not assume the first Alfred-class recreation must be DFIR-specific

## Risks

- underestimating the runtime gap between contracts and product
- overfitting the future platform to Alfred's current repo history
- creating machine-readable surfaces that no validator or runtime uses

## Recommended Direction

1. define the Alfred-class platform as a reusable archetype standard
2. capture the reconstruction blueprint in `GremTech`
3. keep domain-heavy packs optional
4. choose a future pilot repo only after the generic core is stable on paper
