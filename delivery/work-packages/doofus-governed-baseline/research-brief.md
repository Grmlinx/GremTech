# Research Brief

## Objective

Identify the smallest coherent `GremTech` baseline that `Doofus` should adopt
next.

## Current Truth

- `Doofus` already has a strong product-facing `README.md`
- it already exposes user documentation under `documentation/`
- it already has install scripts, build scripts, smoke-test scripts, packaged
  releases, and example workflows
- it does not currently expose `start.ai`
- it does not currently expose an obvious governance surface
- it does not currently expose a durable release-decision or QA-governance lane

## Desired Future State

`Doofus` should keep its practical operator-tool character while gaining:
- an AI startup contract
- a light governance surface
- a maintainer-facing docs front door
- an explicit QA and release decision surface

## Similar Projects And References

- local portfolio analogue:
  - `gremlin-git`
    - useful: evidence of repeated CLI and operator-tool workflows worth curating
    - do not copy: script-garden sprawl and mixed support boundaries
- local portfolio operating analogue:
  - `GremTech`
    - useful: governance, work-package, and routing surfaces
    - do not copy: heavier orchestration surfaces that exceed a lightweight tool repo
- benchmark-only inspiration:
  - `alfred`
    - useful: strong startup-contract discipline
    - useful: explicit proof gates and documentation-sync discipline
    - useful: explicit release posture and machine-readable control surfaces
    - do not copy: heavier memory and governed-runtime model

## Patterns To Borrow Or Reject

- borrow:
  - explicit `start.ai`
  - light governance lane
  - explicit release and QA decision surfaces
- reject:
  - full operational memory model
  - unnecessary multi-harness surfaces
  - runtime-platform expansion

## Evidence

- root files observed:
  - `README.md`
  - `pyproject.toml`
  - `doofus.py`
  - `scripts/build.ps1`
  - `scripts/build.sh`
  - `scripts/test_smoke.ps1`
  - `scripts/test_smoke.sh`
  - `releases/`
  - `documentation/Operations.md`
  - `documentation/Workflows.md`
- missing at repo root:
  - `start.ai`
  - `AGENTS.md`
  - obvious governance or release-policy surface

## Constraints

- keep the repo lightweight
- do not force the Alfred memory model onto it
- avoid unnecessary background-runtime or multi-harness expansion
- avoid disrupting the current install and release docs that already work

## Risks

- adding too many new top-level surfaces too quickly
- creating duplicate docs instead of clarifying the split between user docs and
  maintainer docs
- changing release or build assumptions without explicit QA proof

## Recommended Direction

Adopt the light baseline first:

1. add `start.ai`
2. add a minimal governance lane for decision rights and release expectations
3. add a maintainer docs front door without replacing the existing user docs
4. keep `AGENTS.md` out unless a genuine multi-harness need appears
