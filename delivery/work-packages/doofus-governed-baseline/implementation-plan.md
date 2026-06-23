# Implementation Plan

## Objective

Introduce the minimum `GremTech` baseline to `Doofus` without disturbing its
existing operator-tool strengths.

## Scope

- add a repo-level AI startup contract
- add a light governance surface
- add a maintainer-facing docs front door
- define explicit QA and release decision checkpoints
- define a light documentation-sync contract for critical maintainer entrypoints
- define an explicit release posture for supported, approval-required, and
  non-goal capability

## Out Of Scope

- large product refactors
- background runtime expansion
- multi-harness support by default
- heavy memory-model expansion
- changes to packaging behavior that are not justified by the baseline rollout

## Proposed Changes

- add `start.ai`
- add a small `governance/` surface for:
  - repo operating rules
  - release or QA decision policy
  - change and exception boundaries
- add a maintainer docs front door that complements `documentation/`
- align build, install, smoke-test, and release docs to the new governed flow
  without changing the existing user-facing command model
- add a lightweight gate-checklist path so smoke proof and release conditions
  are explicit
- add a small machine-readable repo-surface manifest only if it materially
  improves validation or maintainability

## Required Roles

- `project-manager`
- `product-architect`
- `governance-officer`
- `code-reviewer`
- `qa-release-engineering-reviewer`
- `devops-engineer`

Add only if later justified:
- `prompt-engineer`
- `security-engineer`

## Required Gates

- structural change gate
- AI contract gate
- runtime or automation gate

## Dependencies

- write access to the `Doofus` repo for implementation
- confirmation of which maintainer docs surface should sit alongside
  `documentation/`
- smoke-test execution after changes

## Validation Plan

- verify the new startup and governance surfaces are readable and coherent
- verify existing install and build commands still match documentation
- run the existing smoke-test lane after implementation
- verify the new documentation-sync surface covers the critical maintainer
  entrypoints without turning into blanket doc ceremony
- verify the release posture is honest about supported scope and non-goals
- confirm no unnecessary runtime or harness surface was introduced
