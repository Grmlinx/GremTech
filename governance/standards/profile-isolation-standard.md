# Profile Isolation Standard

## Purpose

Define how named profiles, workspaces, or tenant-like runtime contexts should
be isolated in a governed agent system.

This standard is informed by `hermes-agent`'s profile model, where each profile
has its own home, config, memory, sessions, and runtime state.

## Core Rule

If the system supports multiple named profiles, those profiles must have
explicit isolation semantics.

A profile is not just a label.
It is a boundary for state, context, and routing.

## What A Profile May Isolate

A profile may isolate:
- config
- secrets source
- memory
- sessions
- logs
- scheduler state
- queue or board state
- operator surfaces

Which of those are isolated must be stated clearly.

## Minimum Isolation Expectation

At minimum, profile boundaries should prevent accidental mixing of:
- memory
- session history
- credential context
- output routing

If those can bleed across profiles implicitly, the profile model is unsafe.

## Scheduling Rule

If scheduled jobs can pin themselves to a profile:

- the profile must already exist
- loading rules must be explicit
- failures should degrade visibly rather than corrupt another profile's state

If profile switching mutates process-global state, profile-pinned jobs should
serialize instead of racing in parallel.

## Delegation Rule

Delegated workers should inherit profile context only when that is the explicit
desired boundary.

Do not assume child work should see every parent memory or credential surface.

## Queue Rule

If a board or queue spans multiple profiles or tenants, define which boundary is
hard and which is soft.

Examples:
- board isolation
- tenant namespace isolation inside a board
- shared versus private worker fleets

If this is not explicit, multi-actor routing will become ambiguous.

## Naming Rule

Profile names should be stable, operator-readable, and meaningful.

Do not overload one profile to mean:
- environment
- tenant
- security posture
- persona

without documenting which meaning actually applies.

## Review Rule

Any profile system should answer:
- what state is isolated
- what state is shared
- how jobs pin to a profile
- how fallback behaves when a profile is missing
- how outputs are routed

If those answers are missing, the profile model is incomplete.
