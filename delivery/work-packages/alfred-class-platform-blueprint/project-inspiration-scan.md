# Project Inspiration Scan

## Target

- target repo: `GremTech`
- initiative: `alfred-class-platform-blueprint`
- repo archetype: `governance-orchestration-layer`

## Problem To Solve

Define how to recreate an Alfred-class governed AI product platform without
touching Alfred or blindly importing its domain-specific shape.

## Local Analogues

- source:
  - `alfred`
  - what was useful:
    - strong startup contract
    - explicit operator surfaces
    - deterministic worker and control-plane model
    - layered proof and release posture
    - machine-readable policy and assurance surfaces
  - what should not be copied:
    - Alfred-specific DFIR, M365, and evidence-management depth as mandatory core
- source:
  - `GremTech`
  - what was useful:
    - cross-repo governance, routing, learning, and standards layer
  - what should not be copied:
    - treating standards-only maturity as if runtime maturity already exists

## External References

- source:
  - `everything-claude-code`
  - why relevant:
    - cross-harness and workflow-source discipline
  - what was useful:
    - thin adapter thinking
  - what should not be copied:
    - command sprawl or oversized harness clutter
- source:
  - `hermes-agent`
  - why relevant:
    - capability packaging and runtime posture design
  - what was useful:
    - capability tiering and config/secrets separation
  - what should not be copied:
    - product assumptions that bypass this portfolio's governance model

## Patterns To Borrow

- generic governed platform core
- optional domain packs on top of that core
- typed approval-bearing execution
- read-only review UI and API
- machine-readable policy only where validators or runtime need it

## Patterns To Reject

- pattern:
  - Alfred file-by-file imitation
  - why reject:
    - recreates accidental repo history instead of the architecture class
- pattern:
  - DFIR-specific assumptions in every future governed platform
  - why reject:
    - would make the core too domain-heavy to reuse

## Absorption Plan

- what will be promoted into this project:
  - Alfred-class platform blueprint
  - governed AI product platform standard
- what will be remembered for later:
  - which Alfred layers are generic core
  - which Alfred layers belong in optional domain packs

## Follow-Up Memory Targets

- `memory/References/`
- `memory/long-term/`
- standard or template updates:
  - `governance/standards/governed-ai-product-platform-standard.md`
