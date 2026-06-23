---
name: repo-owned-skill-pack-authoring
description: Design, create, review, or evolve repo-owned skill packs with clear trigger conditions, lifecycle state, supporting assets, and validation discipline. Use when repeated repo work deserves an agent-facing capability surface instead of prose alone, or when an existing skill pack needs to be tightened, cataloged, or validated.
---

# Repo-Owned Skill Pack Authoring

## Purpose

Create or improve a repo-owned skill pack as a governed capability surface.

## Workflow

1. Decide whether a skill pack is the right artifact.
   Prefer standards, docs, templates, or runtime code when those are the
   better canonical home.
2. Choose a bounded scope.
   Give the pack one clear job, explicit trigger language, and a lifecycle
   state.
3. Keep the main skill contract lean.
   Put detailed references, deterministic scripts, or assets in supporting
   folders only when they materially help.
4. State the boundaries explicitly.
   Define what the skill may do, what it must not do, and what approval or
   governance lanes still apply.
5. Register and validate the pack.
   Update the machine-readable catalog, test representative scripts if they
   exist, and forward-test complex packs when practical.

## Use This Skill For

- evaluation workflows that recur across repos
- product or enterprise review skills
- authoring skills that wrap repeated design or audit patterns
- tightening an existing skill pack whose scope or trigger is too vague

## Do Not Use It For

- replacing a standard with a prompt
- hiding runtime authority in an agent-facing pack
- duplicating broad repo documentation inside `SKILL.md`
- creating skills that exist only because a one-off task happened twice

## References

Read these when working in `GremTech`:

- [../../../governance/standards/skill-pack-standard.md](../../../governance/standards/skill-pack-standard.md)
- [../../../governance/standards/workflow-surface-policy.md](../../../governance/standards/workflow-surface-policy.md)
- [../../../governance/standards/capability-tiering-standard.md](../../../governance/standards/capability-tiering-standard.md)
- [../../../docs/alfred-class-skill-gap-audit.md](../../../docs/alfred-class-skill-gap-audit.md)
- [../../../templates/skill-pack/SKILL.md](../../../templates/skill-pack/SKILL.md)

## Validation

- verify that the skill pack has a narrow, defensible scope
- verify that the description says when to use it
- verify that supporting files exist only when justified
- verify that the catalog entry and lifecycle state match the pack
