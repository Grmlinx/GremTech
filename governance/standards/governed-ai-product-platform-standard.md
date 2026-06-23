# Alfred-Class Standard

## Purpose

Define the minimum architecture and control expectations for an
`Alfred-class` repo.

This is the deepest and heaviest governed product archetype in the current
portfolio.

## Naming Rule

`Alfred-class` is the named baseline because `alfred` is the first repo in this
portfolio built at that scale.

Use `Alfred-class` to mean:

- the starting baseline for future serious governed self-evolving repos
- the minimum bar, not the final aspiration

Future repos should aim to exceed this baseline where justified.

## Scope

Use this standard for repos that need all of the following:

- a strong AI startup contract
- explicit operator surfaces
- approval-bearing execution boundaries
- durable runtime-control state
- deterministic workers or background handlers
- read-only or bounded review surfaces
- machine-readable policy and assurance layers
- explicit compatibility retirement and deprecation discipline
- explicit release posture and self-audit discipline

## Alfred Boundary

This standard generalizes what is reusable from Alfred.

It does not mean:

- Alfred itself should be stripped back from outside its own management lane
- every Alfred-specific domain layer becomes mandatory for every future repo

If Alfred is ever simplified or reorganized, that should be handled inside
Alfred's own management and release discipline.

## Core Rule

A governed AI product platform is not just:

- a prompt pack
- a CLI
- a dashboard
- a memory model

It is a coordinated product with explicit boundaries between:

- chat or operator reasoning
- approval-bearing execution
- deterministic background work
- derived review surfaces
- durable policy and audit state

## Required Layers

### 1. Startup And Surface Contract

The repo must define:

- a strong `start.ai`
- explicit operator-surface roles
- clear statements about what each surface can and cannot do

### 2. Runtime Configuration And Root Discipline

The repo must define:

- how runtime roots are configured
- which roots are authoritative
- which roots are local overrides only
- what must fail closed when authority context is missing

### 3. Work-Unit Record Model

The repo must define a durable record model for the unit of work.

Depending on domain, that might be:

- case-local records
- project-local records
- task-local records
- engagement-local records

The important rule is that live work does not depend on chat memory alone.

### 4. Control Plane State

The repo must expose durable state for:

- work units
- jobs
- workers
- locks
- tasks
- diagnostics
- approvals when applicable

### 5. Workflow And Capability Resolution

The repo must make routing explicit through:

- workflow profiles
- skill or capability catalogs
- tool or adapter selection policy
- repo-owned evaluation surfaces where repeated review or build work justifies
  them

The platform should also distinguish:

- deterministic flows for governed execution
- autonomous teams for bounded exploratory or synthesis-heavy work
- explicit handoffs when responsibility changes

### 6. Deterministic Worker Lane

If background or delegated execution exists, it must be:

- bounded
- deterministic where possible
- recorded
- reviewable
- policy-constrained

### 7. Approval-Bearing Execution Lane

Authority-bearing work must flow through:

- typed action requests
- explicit approval records
- fixed allowlisted actions
- visible execution

Do not blur this into arbitrary shell access.

### 8. Validation And Readiness Layer

The repo must have:

- structural validation
- readiness or doctor checks
- operator-path smoke
- gate status
- documentation-sync enforcement on critical paths

### 9. Review API And Review UI

If browser or API surfaces exist, they should normally be:

- derived-record review surfaces
- read-only by default
- explicit about what they do not control

Where multiple surfaces exist, they should sit above a shared governed runtime
core rather than each surface reimplementing the workflow model.

### 10. Machine-Readable Assurance And Policy Surfaces

The repo should expose structured control files for the policy that validators
or runtime code depend on, such as:

- workflow catalogs
- tool catalogs
- support-state inventories
- adapter registries
- assurance inventories
- documentation-sync contracts
- repo-surface manifests
- compatibility or deprecation ledgers when legacy or fallback lanes exist

### 11. Release Posture

The repo must state:

- what is supported
- what is unsupported
- what is approval-required
- what is maintainer-required
- what is blocked

### 12. Repo Audit And Continual Improvement

The repo must support:

- governed self-audit
- explicit product plus governance top-band review
- durable audit-run state
- promotion of proven lessons into standards, templates, docs, or memory

## Upstream Pattern Rule

Alfred-class systems should be willing to learn from strong outside projects,
but only through selective assimilation:

- absorb the trait
- reject the baggage
- assess source lifecycle and support posture before adopting foundational
  patterns

## Tiering Rule

The platform core should stay generic.

Domain-heavy packs such as DFIR, M365, vulnerability management, or other
specialized workflows should be optional or separately governed layers unless
the product is intentionally domain-specific.

## Non-Goals

Do not require every repo in the portfolio to adopt this shape.

This standard is for the heaviest archetype only.

## Related Navigation

- [Repo archetypes](repo-archetypes.md)
- [Validation and readiness standard](validation-and-readiness-standard.md)
- [Documentation sync standard](documentation-sync-standard.md)
- [Release posture standard](release-posture-standard.md)
- [Machine-readable control surface standard](machine-readable-control-surface-standard.md)
- [Repo audit control standard](repo-audit-control-standard.md)
- [Skill pack standard](skill-pack-standard.md)
- [Compatibility retirement standard](compatibility-retirement-standard.md)
