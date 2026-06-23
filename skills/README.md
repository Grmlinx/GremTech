# Skills

## Purpose

This directory holds repo-owned skill packs for `GremTech`.

These are reusable agent-facing capability assets.
They are not automatically authoritative just because they exist, and they are
not automatically installed into the local Codex environment.

## Role

Use skill packs when repeated work needs:

- bounded procedural knowledge
- reusable evaluation workflow
- repeatable design or implementation discipline
- supporting scripts, references, or assets that belong with an agent-facing
  capability surface

Use standards, docs, templates, or runtime code instead when those are the
better canonical home.

## Structure

- [registry/README.md](registry/README.md)
  - current skill-pack registry
- [../governance/standards/skill-catalog.json](../governance/standards/skill-catalog.json)
  - machine-readable index of registered packs

## Governing Rules

- use [skill-pack-standard.md](../governance/standards/skill-pack-standard.md)
  for lifecycle and validation
- use [workflow-surface-policy.md](../governance/standards/workflow-surface-policy.md)
  to decide whether a skill is the right canonical surface
- use [capability-tiering-standard.md](../governance/standards/capability-tiering-standard.md)
  to decide whether a skill is core, optional, or compatibility-only
