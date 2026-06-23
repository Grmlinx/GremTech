# Agent Orchestration Pattern Standard

## Purpose

Define the main orchestration shapes `GremTech` should recognize when building
or evaluating Alfred-class systems and related governed agent products.

## Core Rule

Do not treat every multi-agent problem as the same shape.

Choose the orchestration pattern that matches the work:
- deterministic flows for governed execution
- bounded autonomous teams for exploratory or synthesis-heavy work
- explicit handoffs when responsibility changes
- one shared runtime core powering multiple user surfaces

## Pattern 1: Deterministic Flows

Use flows when the work needs:

- explicit state transitions
- durable execution records
- conditional branching
- restartability
- stable production behavior

Flows are the default production shape for:
- release gates
- approval-bound work
- scheduled jobs
- stateful delivery workflows

## Pattern 2: Autonomous Teams

Use bounded agent teams when the work benefits from:

- role specialization
- exploration
- synthesis from multiple perspectives
- dynamic delegation inside a bounded lane

Autonomous teams are strongest when:
- the problem is under-specified
- multiple expert roles should contribute
- the output still returns to a governed review or flow surface

Do not let team autonomy replace explicit approval and release boundaries.

## Pattern 3: Explicit Handoffs

Use handoffs when:

- authority changes
- domain ownership changes
- review turns into implementation
- implementation turns into QA or release

Handoffs should be:
- visible
- durable
- attributable
- bounded by clear next action

## Pattern 4: One Core Engine, Many Surfaces

The strongest long-term shape is:
- one governed runtime core
- several surfaces on top of it

Typical surfaces:
- CLI
- local UI
- API
- IDE adapter
- cloud or enterprise control plane

Those surfaces should share the same core contracts instead of reimplementing
the workflow logic independently.

## Pattern 5: Layered Runtime

Prefer a layered model:

1. core runtime and state
2. orchestration and interaction layer
3. integrations, tools, and adapters
4. user-facing surfaces

This keeps:
- runtime state durable
- orchestration explicit
- adapters replaceable
- surfaces thinner

## Pattern 6: Evaluation And Observability

Production-oriented agent systems should treat evaluation and observability as
first-class capabilities, not optional afterthoughts.

That includes:
- benchmark or evaluation harnesses
- run records
- traces or observable events
- clear support posture
- human-in-the-loop checkpoints where needed

## Pattern Selection Rule

When designing a new runtime or product lane:

- use flows first for production-critical execution
- introduce autonomous teams where they materially improve discovery or quality
- keep handoffs explicit
- keep the runtime core separate from UI or cloud packaging choices

## Non-Goals

Do not:

- confuse a studio or no-code surface with the runtime core
- make cloud packaging the primary architecture
- let one framework's terminology dictate the whole product model

## Related Navigation

- [Runtime orchestration principles](../../docs/runtime-orchestration-principles.md)
- [Governed AI product platform standard](governed-ai-product-platform-standard.md)
- [Operator surface standard](operator-surface-standard.md)
- [Deterministic worker standard](deterministic-worker-standard.md)
