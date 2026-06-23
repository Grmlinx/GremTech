# Skill Registry

## Purpose

This folder holds the current repo-owned skill packs for `GremTech`.

Each skill pack should normally live in its own folder and include:

- `SKILL.md`

It may also include:

- `scripts/`
- `references/`
- `assets/`
- `agents/openai.yaml`

## Change Rule

When adding or materially changing a skill pack:

1. update the skill pack itself
2. update [skill-catalog.json](../../governance/standards/skill-catalog.json)
3. validate the pack against
   [skill-pack-standard.md](../../governance/standards/skill-pack-standard.md)
4. add or update supporting templates, references, or standards if the skill
   teaches something reusable beyond the pack itself

## Current Packs

- [repo-semantic-auditor](repo-semantic-auditor/SKILL.md)
- [release-proof-and-readiness-auditor](release-proof-and-readiness-auditor/SKILL.md)
- [repo-owned-skill-pack-authoring](repo-owned-skill-pack-authoring/SKILL.md)
- [operator-ui-product-review](operator-ui-product-review/SKILL.md)
- [governed-runtime-core-builder](governed-runtime-core-builder/SKILL.md)
- [compatibility-retirement-planner](compatibility-retirement-planner/SKILL.md)
- [pattern-assimilation-analyst](pattern-assimilation-analyst/SKILL.md)
