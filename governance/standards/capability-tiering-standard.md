# Capability Tiering Standard

## Purpose

Define how reusable capabilities should be packaged so repos do not drown in
always-on context, unnecessary dependencies, or half-supported workflow packs.

This standard is informed by systems such as `hermes-agent` and
`everything-claude-code`, where not every capability is active by default.

## Core Rule

Not every capability belongs in the default active surface.

Classify capabilities into tiers and make the activation rule explicit.

## Tiers

### Core

Use for:
- always-needed operating rules
- load-bearing standards
- default startup contracts
- essential workflow surfaces

Core capabilities should be:
- low-surprise
- low-dependency
- broadly reusable
- safe to load by default

### Optional

Use for:
- niche domains
- heavier dependencies
- specialized workflows
- operator lanes not justified for every repo

Optional capabilities should be:
- opt-in
- clearly labeled
- documented with prerequisites
- separable without breaking core operation

### Legacy / Compatibility

Use for:
- migration shims
- older command surfaces
- backward-compatibility wrappers

These should:
- point to the canonical source
- be reviewed periodically
- be removable once migration pressure is gone

## Placement Rule

When adding a new reusable workflow or capability, ask:

- is this essential for normal repo operation
- is this niche or heavy enough to stay optional
- is this only here to preserve compatibility with an older surface

If the answer is unclear, default away from always-on.

## Why This Matters

Without capability tiering:

- prompt context grows without discipline
- install surfaces become bloated
- optional workflows get mistaken for guaranteed baselines
- repos carry more operational risk than they need

## Review Rule

Every capability should declare:
- tier
- canonical source
- prerequisites
- activation rule

If those are missing, the capability is not ready for portfolio-wide reuse.
