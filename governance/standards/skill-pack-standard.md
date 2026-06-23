# Skill Pack Standard

## Purpose

Define how repo-owned skills should be created, reviewed, validated, and
maintained as reusable capability surfaces.

## Core Rule

A skill pack is not just a prompt.

It is a bounded reusable capability surface that helps future agents perform a
class of work more reliably without bypassing governance, runtime boundaries,
or human decision rights.

## When To Use A Skill Pack

Use a skill pack when work repeatedly needs:

- a specialized workflow
- domain-specific evaluation rules
- reusable scripts or references
- bounded procedural knowledge
- consistent artifact or control-surface handling

Do not create a skill pack when a normal standard, runbook, template, or one
small script is the better fit.

## Shape

A skill pack should normally contain:

- `SKILL.md`

It may also contain:

- `scripts/`
- `references/`
- `assets/`
- `agents/openai.yaml`

Keep the main skill contract lean.
Put detailed references or deterministic helpers in the supporting folders.

## Required Contract

Every substantial skill pack should make these clear:

- what the skill does
- when it should be used
- what inputs it expects
- what outputs it should produce
- what it is allowed to do
- what it must not do
- what approval or authority boundaries still apply
- what supporting scripts, references, or assets it relies on

## Lifecycle

Use these lifecycle states:

- proposed
- drafted
- available
- proven
- deprecated

## Promotion Requirements

Before a skill pack is treated as `available`, it should have:

- a clear trigger description
- stable scope
- explicit boundaries
- at least one realistic usage pattern
- validation of the skill structure

Before a skill pack is treated as `proven`, it should have:

- repeated successful use
- known limitations
- failure behavior
- tested scripts where scripts exist
- forward-testing for complex skills when practical

## Validation Rule

Skill packs should be validated, not just written.

At minimum:

- validate structure and frontmatter
- run representative scripts if scripts exist
- check that references and assets still match the skill contract

For complex skills:

- forward-test them on realistic tasks
- keep validation honest by avoiding leaked answers or hidden ground truth

## Boundary Rule

Skill packs do not:

- authorize privileged execution
- override governance gates
- replace standards
- replace runbooks where runbooks are the canonical operator surface
- silently widen repo scope

If a workflow becomes authority-bearing or runtime-critical, pair the skill
with the relevant standards, validators, and approval surfaces.

## Canonical Placement Rule

Use a skill pack as the canonical home when the reusable behavior is primarily
agent-facing procedural knowledge.

Use standards, docs, templates, or runtime code as the canonical home when the
behavior is primarily policy, operator guidance, reusable document structure,
or executable system behavior.

## Review Rule

Review new or materially changed skill packs against:

- governance boundaries
- repo archetype fit
- duplication with existing standards or runbooks
- maintenance burden
- validation integrity

## Catalog Rule

If a repo uses multiple skill packs, maintain a machine-readable catalog so the
surface is discoverable without scanning the whole repo.

## Related Navigation

- [skill-catalog.json](skill-catalog.json)
- [Agency learning standard](agency-learning-standard.md)
- [Project inspiration standard](project-inspiration-standard.md)
- [Workflow surface policy](workflow-surface-policy.md)
- [Capability tiering standard](capability-tiering-standard.md)
