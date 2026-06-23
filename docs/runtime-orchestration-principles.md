# Runtime Orchestration Principles

## Purpose

Summarize the runtime ideas now forming inside `GremTech` before a concrete
execution engine exists.

## Principles

### Explicit Surfaces

Every runtime surface must be named:
- local UI
- CLI
- executive intake chat
- IDE adapter
- scheduler
- queue worker
- remote adapter

If it can dispatch, approve, or expose work, it is part of the governed model.

### Local-First By Default

Prefer visible, local, operator-present execution before remote or hidden
surfaces.

### Bounded Background Work

Cron jobs, dispatchers, and delegated workers must be:
- scoped
- interruptible
- observable
- separately recorded

### Capability Tiering

Not every workflow should be always-on.
Future runtime capabilities should declare whether they are:
- core
- optional
- compatibility-only

### Isolation Is External

The meaningful boundary is OS-level or equivalent external sandboxing.
In-process checks are still useful, but they do not count as containment.

### Config And Secrets Separation

Normal configuration should be easy to review.
Secrets should stay in secret-bearing surfaces.

### Profile Isolation

If the runtime supports named profiles, each profile must make its state
boundary explicit:
- config
- memory
- sessions
- scheduler state
- output routing

### Queue Before Swarm

If work becomes asynchronous, durable, or multi-actor, move it into an explicit
queue or work register rather than pretending chat continuity is enough.

### Flows Before Swarm

For production-critical execution, start with deterministic flows and explicit
state.

Introduce autonomous teams only where exploration, synthesis, or bounded
delegation materially improves the result.

### One Engine, Many Surfaces

The long-term target should be one governed runtime core with multiple surfaces
above it:
- CLI
- local UI
- API
- IDE or chat adapters
- enterprise or cloud control planes when justified

Do not let each surface invent its own workflow logic.

### Layered Runtime

Keep clear separation between:
- core runtime and state
- orchestration layer
- extensions and adapters
- user-facing surfaces

### One Executive Front Door

The operator should talk to one accountable executive surface.
That surface should decompose work internally rather than forcing the operator
to manually run a committee.

### Policy-Driven Activation

If a future runtime activates roles automatically, it should do so from
explicit routing policy and durable activation records, not from hidden prompt
intuition alone.

## Current Implication

`GremTech` should continue standardizing the contracts first:
- surfaces
- isolation
- scheduling
- delegation
- role activation
- output routing

before building a runtime that tries to execute them.
