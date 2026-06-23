# Project Inspiration Scan

## Target

- target repo: `Doofus`
- initiative: `doofus-governed-baseline`
- repo archetype: `operator-tool-product`

## Problem To Solve

Add the minimum governed baseline to `Doofus` without destroying its practical
operator-tool character.

## Local Analogues

- source:
  - `Doofus` current repo surface
  - what was useful:
    - practical README
    - workflow docs
    - build, install, smoke-test, and release surfaces already exist
  - what should not be copied:
    - missing governance and startup surfaces
- source:
  - `gremlin-git`
  - what was useful:
    - evidence of repeated operator-tool workflows
    - practical file and folder processing patterns
  - what should not be copied:
    - script-garden sprawl
    - mixed support boundaries
- source:
  - `alfred`
  - what was useful:
    - strong startup-contract rigor
    - strong memory discipline
    - layered validation and smoke-gate discipline
    - documentation-sync enforcement for critical entrypoints
  - what should not be copied:
    - heavier governed-runtime and memory structure than `Doofus` needs

## External References

- source:
  - CLI best-practice guidance
  - why relevant:
    - `Doofus` is a multi-command operator tool
  - what was useful:
    - human-first but scriptable CLI behavior
    - clear help and examples
  - what should not be copied:
    - one-size-fits-all command philosophy that ignores this portfolio's
      Windows-first operational reality

## Patterns To Borrow

- pattern:
  - explicit `start.ai`
- pattern:
  - light governance and release-decision surfaces
- pattern:
  - explicit gate checklist and smoke-proof expectations for maintainer paths
- pattern:
  - keep user docs separate from maintainer and control docs
- pattern:
  - preserve single-file, folder-per-file, and folder-combined workflow modes

## Patterns To Reject

- pattern:
  - full operational memory model
  - why reject:
    - too heavy for a lightweight operator tool
- pattern:
  - support every harness by default
  - why reject:
    - no current evidence `Doofus` needs that complexity

## Absorption Plan

- what will be promoted into this project:
  - `start.ai`
  - light governance lane
  - explicit QA and release surfaces
- what will be remembered for later:
  - operator-tool CLI patterns
  - promotion path from `gremlin-git` style scripts into curated tool products

## Follow-Up Memory Targets

- `memory/References/`
- `memory/long-term/`
- standard or template updates:
  - `governance/standards/cli-tool-standard.md`
