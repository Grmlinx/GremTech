---
name: governed-runtime-core-builder
description: Design and implement the core runtime surfaces for Alfred-class systems, including work-unit records, control-plane state, deterministic workers, action-request and approval lanes, and review boundaries. Use when turning runtime governance standards into actual repo scaffolds or evaluating runtime architecture decisions.
---

# Governed Runtime Core Builder

## Purpose

Build or review the minimal governed runtime core before domain-specific packs,
workers, or product surfaces expand around it.

## Workflow

1. Start with the canonical runtime standards and the Alfred-class blueprint.
2. Identify the smallest real runtime slice that proves the architecture.
3. Map work-unit records, control-plane state, deterministic workers, approval
   records, and review surfaces together.
4. Define the implementation order and the proof needed at each stage.
5. Record non-goals so runtime ambition does not outrun governance clarity.

## Use This Skill For

- implementing governed runtime scaffolds from `GremTech` standards
- reviewing whether a proposed runtime split preserves authority boundaries
- planning milestone order for state, queueing, workers, approvals, and review
  surfaces

## Do Not Use It For

- adding domain-specific automation before the runtime core exists
- treating orchestration ambition as permission to weaken approval or review
  boundaries

## References

- [../../../governance/standards/work-unit-record-standard.md](../../../governance/standards/work-unit-record-standard.md)
- [../../../governance/standards/control-plane-state-standard.md](../../../governance/standards/control-plane-state-standard.md)
- [../../../governance/standards/action-request-and-approval-standard.md](../../../governance/standards/action-request-and-approval-standard.md)
- [../../../governance/standards/deterministic-worker-standard.md](../../../governance/standards/deterministic-worker-standard.md)
- [../../../governance/standards/review-platform-standard.md](../../../governance/standards/review-platform-standard.md)
- [../../../docs/alfred-class-platform-blueprint.md](../../../docs/alfred-class-platform-blueprint.md)
- [../../../docs/alfred-class-runtime-gap-analysis.md](../../../docs/alfred-class-runtime-gap-analysis.md)
- [../../../delivery/work-packages/alfred-class-platform-blueprint/core-milestone-plan.md](../../../delivery/work-packages/alfred-class-platform-blueprint/core-milestone-plan.md)

## Validation

- verify the runtime slice is core-first rather than domain-pack-first
- verify authority, approval, and review boundaries are explicit
- verify the implementation plan points at real proof surfaces, not prose only
