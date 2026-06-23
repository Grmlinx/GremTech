# GremTech Agent Instructions

This file is the universal cross-harness agent surface for this repo.

`start.ai` remains the canonical startup contract.
Use this file when the harness prefers `AGENTS.md`-style instructions.

## Purpose

`GremTech` is the portfolio operating system for the wider repo estate.

It exists to standardize:
- governance
- onboarding
- memory models
- review sequencing
- reusable development practices
- cross-harness agent behavior
- executive intake and delegated delivery

## Required Read Order

1. `AGENTS.md`
2. `start.ai`
3. `README.md`
4. `WORKING-CONTEXT.md`
5. `memory/README.md`
6. `governance/README.md`
7. `governance/team-charter.md`
8. `governance/standards/README.md`
9. `portfolio/README.md`
10. the relevant file under `portfolio/profiles/` when a known target repo is involved
11. the relevant file under `delivery/work-packages/` when the task belongs to an active rollout package

## Core Rules

- Keep shared standards in `GremTech`; keep repo-local truth in the target repo.
- Choose the repo archetype before adding structure.
- Prefer thin harness adapters over duplicating workflow logic per tool.
- Treat `README.md` as the human front door and `start.ai` as the repo AI front door.
- Use `AGENTS.md` as the cross-harness bridge only where it adds portability value.
- Do not broaden runtime power, write surfaces, or AI authority silently.
- Route normal operator requests through the `CTO Desk` workflow instead of
  exposing raw committee behavior.

## Workflow Surface Policy

- Canonical durable behavior belongs in shared source surfaces such as:
  - `governance/standards/`
  - `docs/`
  - `portfolio/`
  - `delivery/`
  - `memory/`
  - `templates/`
- Harness-specific files should adapt loading, packaging, or event shape at the edge.
- If the same workflow must be edited in multiple harness copies, move the durable behavior back into a shared source.

## Working Context Rule

Use `WORKING-CONTEXT.md` for:
- current truth
- active queues
- current constraints
- next portfolio adoption moves

Do not turn it into a long-term archive.

## Done Rule

A change is complete only when:
- the repo archetype is respected
- cross-harness duplication is not increased
- standards and templates match the new truth
- the adoption path for other repos is clearer than before
