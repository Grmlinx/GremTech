# Work Package Standard

## Purpose

Define how a substantive `CTO Desk` request becomes a durable execution packet.

## Core Rule

If work is important enough to cross multiple phases, roles, or gates, it
should have a work package.

A work package is the durable folder that binds together:
- the request
- the active team
- the current phase
- the governing artifacts
- the current delivery decision

## Required Shape

Each work package should contain:
- `work-package.md`
  - the front door summary
- `executive-intake-brief.md`
- `role-activation-record.md`
- `project-inspiration-scan.md` when the work benefits from local or external comparison
- `research-brief.md` when discovery is required
- `implementation-plan.md` when change is being designed
- `governance-decision.md` when scope or policy needs explicit approval

Add when the work reaches them:
- `qa-gate.md`
- `gate-checklist.md`
- `release-decision.md`
- `documentation-sync-contract.json` when the work changes critical startup or
  operator entrypoints
- `learning-promotion-note.md` when the project teaches something worth future reuse

## Front Door Fields

`work-package.md` should state:
- work-package id
- status
- target repo
- repo archetype
- repo change posture
- current phase
- objective
- owners
- required gates
- artifact links

## Status Rule

Allowed work-package states:
- proposed
- active
- blocked
- complete
- deferred

The status should reflect delivery reality, not optimism.

## Ownership Rule

Every active work package should name:
- the executive surface
- the sequencing owner
- the architecture owner
- the governance owner when applicable
- the current phase owner

## Routing Rule

Work packages should live under:
- `delivery/work-packages/`

They are delivery records, not general docs and not memory summaries.

## Reuse Rule

If a package produces reusable policy, promote that policy into:
- `governance/standards/`
- `templates/`
- `portfolio/`
- `docs/`

Do not hide durable portfolio decisions only inside one work package.
