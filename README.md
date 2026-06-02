# GremTech

GremTech is the seed repository for a governed software-development agency
model.

Its job is to hold the role system, prompt pack, hierarchy, review contracts,
and output scaffolding for multi-agent software audits, architecture reviews,
and delivery oversight across other repositories.

The target repositories remain the source of truth.
GremTech is the governance and orchestration layer around those repos.

## Current Scope

This scaffold is the first pass only.

It currently provides:
- a copied expert prompt pack seeded from Alfred
- an agent registry built from those prompts
- a hierarchy with governance at the top and UI/UX at the bottom
- recommendation intake and issue-mapping structure
- documentation for how agents should audit independently, escalate, and talk
  to each other

It does not yet provide:
- a runtime orchestration service
- autonomous agent execution
- persistent queue management
- database-backed audit state
- inter-agent messaging infrastructure

## Operating Principles

- governance first
- target repo is the source of truth
- no hidden authority
- no silent scope creep
- recommendations must be traceable
- blockers must escalate upward
- downstream implementation agents do not overrule upstream governance agents

## Structure

```text
GremTech/
- agents/
  - registry/
- docs/
- governance/
  - standards/
    - expert-audit-prompts/
- memory/
  - sensory/
    - Recommendations/
- templates/
```

## Agent Layers

1. Governance
   - governance officer
2. Leadership
   - project manager
   - product architect
3. Risk and assurance
   - security engineer
   - privacy / legal / compliance reviewer
   - licensing / procurement reviewer
   - QA / release engineering reviewer
   - Windows platform / SRE / operations reviewer
4. Implementation and platform
   - DevOps engineer
   - AI engineer
   - code reviewer
   - prompt engineer
5. Domain specialists
   - DFIR expert
   - M365 / Entra administrator
   - incident response operations / client delivery reviewer
6. Experience
   - UI engineer

Governance sits at the top.
UI/UX sits at the bottom by design, because presentation and interaction should
consume already-approved constraints rather than define them.

## Recommendation Output Path

Recommendation notes produced by agents should land in:
- `memory\sensory\Recommendations`

Before creating a new recommendation file, agents should:
- check the issue map
- check the recommendation README
- reference existing findings where possible
- create a new note only for a materially new review angle

## Start Here

- [governance/principles.md](governance/principles.md)
- [governance/agent-hierarchy.md](governance/agent-hierarchy.md)
- [agents/registry/agent-topology.json](agents/registry/agent-topology.json)
- [governance/standards/expert-audit-prompts/README.md](governance/standards/expert-audit-prompts/README.md)
- [memory/sensory/Recommendations/README.md](memory/sensory/Recommendations/README.md)
- [docs/implementation-roadmap.md](docs/implementation-roadmap.md)
