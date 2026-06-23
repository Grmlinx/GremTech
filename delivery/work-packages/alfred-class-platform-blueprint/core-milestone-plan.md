# Core Milestone Plan

## Purpose

Turn the Alfred-class platform blueprint into a concrete implementation path for
the generic governed runtime core.

## Milestone 0: Contract Complete

Status:
- mostly complete in `GremTech`

Goal:
- finish the contract layer before runtime implementation starts

Must exist:
- startup-contract rules
- operator-surface rules
- work-unit record rules
- control-plane state rules
- action-request and approval rules
- worker rules
- review-platform rules
- release-posture rules
- validation and documentation-sync rules

Acceptance:
- standards and templates exist
- blueprint and gap analysis exist
- active work package exists

## Milestone 1: Generic Control Plane

Goal:
- create the first real runtime core without any domain-heavy packs

Build:
- machine-local config model
- authoritative runtime-root selection
- work-unit scaffold
- local state store for work units, jobs, workers, locks, tasks, diagnostics
- root CLI for create, status, list, and diagnostics

Acceptance:
- a fresh runtime can create a new work unit
- status survives restart
- mutating commands fail closed without explicit authority context
- runtime state is inspectable through the root CLI

## Milestone 2: Deterministic Worker Core

Goal:
- add bounded background execution without hidden authority

Build:
- worker catalog
- one deterministic worker class
- queue or job-claim path
- worker logs and failure records
- locks for scarce or conflicting resources

Acceptance:
- one deterministic background job can be queued and executed
- worker output is durable and reviewable
- stale job or lock state is visible

## Milestone 3: Approval-Bearing Action Lane

Goal:
- separate ordinary deterministic work from authority-bearing action

Build:
- typed action-request schema
- approval-record schema
- exact request binding
- one visible approval-bearing execution lane
- one allowlisted action implementation

Acceptance:
- a request can be drafted, approved, and executed visibly
- arbitrary command payloads are refused
- approval is tied to the exact request

## Milestone 4: Proof And Review Surfaces

Goal:
- make the runtime inspectable and provable

Build:
- repo validator with semantic invariant checks
- smoke proof for the operator path
- documentation-sync validation
- gate checklist and release decision flow
- read-only API over work-unit and control-plane state
- small read-only review UI

Acceptance:
- validator catches semantic drift, not just syntax errors
- smoke passes through the real runtime entrypoint
- API and UI remain read-only by default

## Milestone 5: Optional Domain Packs

Goal:
- add specialist packs only after the generic governed runtime core is stable

Possible packs:
- DFIR
- M365
- infrastructure operations
- other governed specialist domains

Acceptance:
- the pack declares its support boundaries
- the pack proves one real workflow end to end
- the pack does not weaken the generic core boundaries

## Current Recommendation

Do not start with Milestone 5.

The next real implementation decision should be whether to build Milestone 1 in:

- a new dedicated repo
- `GremTech`
- another future platform repo

`Doofus` is not the right home for this core.
