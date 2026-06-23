# Alfred-Class Platform Blueprint

## Purpose

Define what it would take for `GremTech` to recreate something like `alfred`
without touching `alfred` itself.

This is a reconstruction blueprint, not a copy plan.

## Naming And Position

`Alfred-class` is the right term for this baseline.

Reason:

- `alfred` is the first repo in this portfolio built at that scale
- it should be treated as the starting baseline for future serious governed
  self-evolving repos
- future projects should aim to build beyond it, not below it

That does not make Alfred the direct implementation host for the next-stage
generic platform core.

## Feasibility Verdict

Yes, `GremTech` can recreate an Alfred-class platform.

It cannot do that today by turning on one missing feature.

What exists now is the contract and governance layer.
What is still missing is the runtime and product layer.

## What Alfred Actually Is

At a systems level, `alfred` is a governed AI product platform with these
coordinated layers:

1. strong startup contract
2. explicit operator-surface model
3. authoritative runtime-root and control-root discipline
4. durable work-unit records outside chat memory
5. local control-plane state for cases, jobs, workers, tasks, and diagnostics
6. workflow, tool, adapter, and skill resolution
7. deterministic workers
8. typed approval-bearing action requests and visible execution
9. read-only platform API
10. read-only review UI
11. layered validation and smoke proof
12. machine-readable policy and assurance surfaces
13. explicit release posture
14. governed repo-audit and continual-improvement loop

## Current GremTech Position

### Already Exists In GremTech

- startup-contract standardization
- role activation and CTO Desk routing
- work-package and audit artifact standards
- learning and memory standards
- validation, documentation-sync, release-posture, and audit-control standards
- machine-readable routing and portfolio-registry surfaces
- cross-harness and runtime-governance rules

### Missing From GremTech

- a root CLI or orchestrator product surface
- authoritative runtime-root selection logic
- a durable control-plane state store
- a work-unit record scaffold
- deterministic workers
- typed action-request and approval runner lane
- a platform API
- a review UI
- a repo validator that enforces semantic invariants
- optional domain packs that prove real workflows end to end

The current gap is now spelled out in
`docs/alfred-class-runtime-gap-analysis.md`.

## Recreate The Class, Not The Exact Product

The right target is:

- recreate the class of system Alfred represents

Not:

- clone Alfred's exact DFIR, M365, or case-specific internals

That means the reusable core should be generic:

- governed work-unit lifecycle
- bounded operator surfaces
- visible approval lane
- deterministic worker lane
- durable review API/UI
- machine-readable control surfaces
- layered validation and release posture

Specialized domains should sit on top as optional packs.

## Minimal Reproducible Slice

If `GremTech` wanted to prove it can build an Alfred-class platform, the
smallest credible slice would be:

1. root CLI for governed work-unit setup and status
2. machine-local config and authoritative runtime-root selection
3. durable work-unit scaffold with status, notes, exports, and action-request
   folders
4. local state store for work units, jobs, workers, locks, and diagnostics
5. one deterministic worker lane
6. typed action requests plus one visible approval-bearing runner lane
7. validator plus smoke proof
8. read-only API over derived records and control-plane state
9. small read-only UI
10. explicit release decision and support-state record

That would be enough to prove the architecture class without rebuilding all of
Alfred's domain depth.

## Recommended Build Sequence

### Phase 1: Generic Control Plane

Build:

- runtime-root discipline
- config model
- repo-surface manifest
- work-unit scaffold
- local state store
- root CLI
- durable work-unit record scaffold

### Phase 2: Deterministic Workflow Core

Build:

- workflow profile resolver
- support-state inventory
- one deterministic worker class
- readiness and validation harness

### Phase 3: Approval And Execution

Build:

- action-request schema
- approval record shape
- allowlisted action execution lane
- visible runner or equivalent operator approval surface

### Phase 4: Review Platform

Build:

- read-only API
- read-only review UI
- derived-record review contracts

### Phase 5: Domain Packs

Add optional packs such as:

- DFIR
- M365
- infra operations
- other governed specialist domains

Only after the generic platform core is stable.

## Non-Negotiables

- do not touch `alfred`
- do not start stripping Alfred from outside its own management lane
- do not force Alfred's domain-specific shape into every repo
- do not treat prose-only governance as sufficient runtime control
- do not build hidden execution power before the approval model exists
- do not call a repo Alfred-class until the runtime and proof layers exist

## Best Next Move

The best next move inside `GremTech` is not to start cloning Alfred file by
file.

It is to build the generic Alfred-class core blueprint first, then choose a
pilot implementation repo or create a new dedicated platform repo for that
purpose.

The first concrete contract set for that work now lives in:

- `governance/standards/work-unit-record-standard.md`
- `governance/standards/control-plane-state-standard.md`
- `governance/standards/action-request-and-approval-standard.md`
- `governance/standards/deterministic-worker-standard.md`
- `governance/standards/review-platform-standard.md`
