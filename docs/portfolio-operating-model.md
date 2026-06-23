# Portfolio Operating Model

## Purpose

Explain how `GremTech` standardizes development across very different repos
without flattening them into one shape.

## Core Idea

The portfolio is not one product.
It is a governed set of repo types:

- AI platform
- infrastructure platform
- operator tools
- legacy tool estate
- human knowledge vault
- governance/orchestration layer

Standardization happens through:
- shared principles
- explicit team roles
- approved memory patterns
- onboarding standards
- repo change posture
- cross-harness portability rules
- runtime posture rules
- reusable templates
- repo profiles

## Control Stack

1. Repo owner
   - decides priorities and exceptions
2. Governance
   - protects scope, write boundaries, and drift controls
3. Leadership
   - frames work and chooses review depth
4. Risk and assurance
   - blocks unsafe advancement
5. Implementation
   - builds within approved constraints
6. Specialists
   - add domain-specific depth only when justified

## Portfolio Defaults

### Common Requirements

Every governed repo should expose:
- `README.md`
- `start.ai`
- an explicit control surface
- a chosen memory pattern
- a durable documentation front door

If the repo needs multi-harness agent support, it should also expose:
- `AGENTS.md`
- thin harness-local adapter surfaces

### Variable Requirements

These vary by archetype:
- depth of memory model
- whether `runbooks/` are mandatory
- which specialists are required
- how heavy the release gate needs to be
- whether cross-harness adapter surfaces are worth maintaining
- whether the repo should tolerate background runtime surfaces at all

## Runtime Posture

Every repo profile should also state its runtime posture.

Examples:
- explicit governed runtime
- operator-driven automation
- local-tooling first
- consolidation first
- human-first manual

This stops future automation work from assuming every repo wants the same
degree of daemonization, scheduling, delegation, or remote surface growth.

## Change Posture

Every repo profile should also state its current change posture.

Examples:
- observe-only
- active-rollout-target
- defer-active-rollout
- active rollout candidate
- maintain-and-align
- classify-before-expanding
- light-touch only

This stops the `CTO Desk` from choosing the wrong repo as the next execution
target just because it is strategically important.

## Harness Portability

The portable rule is:

1. keep durable workflow logic in shared repo-owned surfaces
2. use `AGENTS.md` only as a universal bridge where it adds value
3. keep harness-specific config and hook files thin
4. avoid duplicating the same workflow across tool-specific folders

## Repo Profiles

The machine-readable source for target-repo classification lives in
[`../portfolio/targets.json`](../portfolio/targets.json).

Human-readable overlays live in:
- `../portfolio/profiles/alfred.md`
- `../portfolio/profiles/home-lab.md`
- `../portfolio/profiles/doofus.md`
- `../portfolio/profiles/gremlin-git.md`
- `../portfolio/profiles/gremoire.md`

## Promotion Rule

When a pattern proves useful in one repo:

1. preserve the repo-specific truth in that repo first
2. generalize only the reusable part
3. express the reusable part in `GremTech`
4. point the other repos at the resulting standard or template

This avoids cargo-cult copying while still building a coherent agency model.
