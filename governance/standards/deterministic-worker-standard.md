# Deterministic Worker Standard

## Purpose

Define how governed repos should describe and constrain worker classes or
background handlers.

## Core Rule

Workers should be cataloged explicitly.

If background execution exists, the repo should be able to say:

- what each worker is for
- what it is allowed to do
- what execution mode it needs
- what locks or scarce resources it claims
- what boundaries it must preserve

## Required Worker Fields

Each worker class should usually define:

- id
- class
- accepted CLI or runtime names
- execution mode
- summary
- boundary statement
- capabilities
- default job types
- default locks

Use `templates/worker-classes.json` as the seed shape.

## Determinism Rule

Deterministic workers should:

- preserve source-versus-derived boundaries
- record what they did
- expose failures and limitations explicitly
- avoid hidden mutable side effects outside their allowed scope

## Scarce Resource Rule

If a worker consumes scarce or high-risk resources, such as:

- mount lanes
- privileged host tooling
- Docker daemon access
- externally rate-limited APIs

its locking and execution rules must be explicit.

## Approval Rule

Some workers may run as ordinary deterministic handlers.
Others may still require explicit approval because of execution mode or target
scope.

Worker existence is not blanket execution authority.

## Related Navigation

- [Control plane state standard](control-plane-state-standard.md)
- [Scheduled and delegated work standard](scheduled-and-delegated-work-standard.md)
- [Governed AI product platform standard](governed-ai-product-platform-standard.md)
