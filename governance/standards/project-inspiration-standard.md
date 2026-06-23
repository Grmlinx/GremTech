# Project Inspiration Standard

## Purpose

Define how `GremTech` should research similar projects before shaping a new
product, major feature set, or repo baseline.

## Core Rule

Do not begin from a blank mental slate when strong prior work likely exists.

Before major design work, perform an inspiration scan and record:
- local analogues
- external references
- source lifecycle and support posture
- patterns to borrow
- patterns to reject

## When Required

Use an inspiration scan when the work involves:
- a new tool or product surface
- a major repo onboarding or baseline rollout
- a new runtime or operator surface
- a significant UI or CLI redesign
- a new infrastructure pattern worth standardizing

## Research Order

1. current target-repo reality
2. local portfolio analogues
3. script-garden or historical internal examples
4. external project references
5. official standards or vendor documentation where relevant

## Output

Create:
- `project-inspiration-scan.md`

Use:
- [../../templates/project-inspiration-scan.md](../../templates/project-inspiration-scan.md)

## Borrowing Rule

Do not cargo-cult whole systems.

Instead:
- identify the specific good parts
- identify the hidden costs
- identify whether the source is active, maintenance-only, or transitional
- adapt them to the repo archetype and change posture

## Memory Rule

Durable sources and exemplars should be recorded in:
- `memory/References/`

Validated reusable lessons should be promoted into:
- `memory/long-term/`
- standards
- templates
- docs

## Evidence Rule

A good inspiration scan should say:
- what was examined
- why it was relevant
- what the source's lifecycle posture looked like
- what was actually absorbed
- what was deliberately rejected
