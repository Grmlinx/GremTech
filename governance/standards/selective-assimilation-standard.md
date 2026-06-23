# Selective Assimilation Standard

## Purpose

Define how `GremTech` should absorb strengths from external systems without
copying their whole architecture, support model, or baggage.

## Core Rule

`GremTech` should absorb strengthening traits, not whole stacks.

Internal shorthand:
- the `Sword of Gryffindor` rule

Meaning:
- absorb what makes the system stronger
- reject what would add weight without durable value

## Source Assessment Rule

Before borrowing from an external project, assess:

1. relevance
   - does it solve the same class of problem?
2. lifecycle state
   - active, maintenance-only, migrating, experimental, or abandoned
3. support model
   - community, vendor-backed, enterprise-backed, or source-available hybrid
4. control model
   - where authority, review, execution, and state actually live
5. hidden cost
   - lock-in, complexity, product assumptions, runtime assumptions, or
     maintenance burden

## Assimilation States

Use these states when recording an external pattern:

- `observed`
- `trial-worth`
- `absorbed`
- `deferred`
- `rejected`
- `retired`

The point is to make adoption explicit instead of relying on memory or taste.

## Borrowing Rule

When a source is worth learning from:

- extract the specific pattern
- record why it is strong
- record what should not be copied
- adapt it to the repo archetype and change posture
- promote only the durable local form into standards, templates, docs, skills,
  or runtime work

Do not let a source repo become an invisible architecture dependency unless it
is deliberately adopted as one.

## Lifecycle Rule

A good pattern can still come from a source that should not be the foundation.

Example classes:
- maintenance-mode source with strong architectural lessons
- active enterprise source with good production posture but too much product
  baggage
- research-heavy source with useful ideas but weak operational guarantees

Record those distinctions directly.

## Output Rule

Substantive external pattern scans should normally produce:

- an updated inspiration scan or external-pattern harvest note
- a `memory/References/` record
- any needed `memory/long-term/` lesson
- durable repo-owned updates where the pattern is truly worth keeping

## Non-Goals

Do not use assimilation to justify:

- copying vendor roadmaps blindly
- inheriting another system's governance vocabulary unchanged
- adopting a tool because it is popular
- adopting a runtime because it has a nice demo surface

## Related Navigation

- [Agency learning standard](agency-learning-standard.md)
- [Project inspiration standard](project-inspiration-standard.md)
- [Agent orchestration pattern standard](agent-orchestration-pattern-standard.md)
- [External pattern assessment template](../../templates/external-pattern-assessment.md)
