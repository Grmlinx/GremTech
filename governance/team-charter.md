# Team Charter

## Purpose

Define the standard agency team used to develop and govern the portfolio.

The goal is not to throw every role at every repo.
The goal is to activate the smallest team that still preserves quality,
security, operational reality, and continuity.

Activation policy is defined in:
- [standards/role-activation-standard.md](standards/role-activation-standard.md)
- [standards/role-activation-matrix.json](standards/role-activation-matrix.json)

## User-Facing Front Door

The default operator-facing surface is the `CTO Desk`.

This is not a separate sovereign role.
It is a synthesis surface composed of:
- project manager
- product architect
- governance officer

Its job is to receive plain-English executive requests and route them through
the correct governed workflow without forcing the operator to manually assemble
the team.

## Core Delivery Cell

### Governance Officer

Owns:
- scope control
- drift prevention
- rule changes
- escalation decisions

Use when:
- a repo is gaining new powers
- write boundaries are changing
- governance or memory rules are in dispute

### Project Manager

Owns:
- sequencing
- milestone framing
- dependency visibility
- synthesis across reviewers

Use when:
- work spans multiple repos
- multiple roles are needed
- a roadmap or adoption path is needed

### Product Architect

Owns:
- repo archetype selection
- system boundaries
- structural coherence
- fit between docs, runtime, and operating model
- shared-source versus harness-adapter separation

Use when:
- introducing new top-level structures
- deciding how a repo should be shaped
- standardizing across repos with different purposes

### Security Engineer

Owns:
- trust boundaries
- authority surfaces
- secret handling
- unsafe defaults

Use when:
- automation, credentials, external systems, or elevated actions are involved

### QA / Release Engineering Reviewer

Owns:
- proof standards
- validation gates
- release discipline
- regression expectations

Use when:
- a repo ships code, tooling, or shared automation

### DevOps Engineer

Owns:
- build and release automation
- dependency discipline
- environment repeatability
- operational health signals
- install and packaging surface coherence across tools

Use when:
- packaging, CI, deployment, or bootstrap paths matter

### Code Reviewer

Owns:
- correctness
- maintainability
- implementation risk
- change clarity

Use when:
- code or scripts change

### Prompt Engineer

Owns:
- AI startup contracts
- prompt/runtime alignment
- wording-driven scope drift
- cross-harness instruction parity where multiple agent tools are supported

Use when:
- `start.ai`, role prompts, or governed AI behavior changes

## Specialist Overlays

Activate these only when the repo domain justifies them:

- Privacy / Legal / Compliance Reviewer
  - for regulated data, policy, or client-delivery exposure
- Licensing / Procurement Reviewer
  - for vendor lock-in, supportability, or redistribution questions
- Windows Platform / SRE / Operations Reviewer
  - for workstation, host, bootstrap, recovery, or runtime operations risk
- DFIR Expert
  - for forensic and defensibility-sensitive workflows
- M365 / Entra Administrator
  - for Microsoft cloud collection or tenant-governance workflows
- Incident Response Operations / Client Delivery Reviewer
  - for real-world delivery practicality and operator usability under pressure
- UI Engineer
  - for deliberate interface and interaction design after upstream constraints are set

## Default Activation By Repo

These are defaults, not mandatory full rosters for every task.
Final activation should still be narrowed by workstream and risk.

- `alfred`
  - governance officer, project manager, product architect, security engineer,
    QA / release engineering reviewer, DevOps engineer, code reviewer,
    prompt engineer, DFIR expert, M365 / Entra administrator
- `home-lab`
  - governance officer, project manager, product architect, security engineer,
    QA / release engineering reviewer, Windows platform / SRE / operations
    reviewer, DevOps engineer, code reviewer
- `Doofus`
  - project manager, product architect, code reviewer, QA / release
    engineering reviewer, DevOps engineer, UI engineer when operator
    experience changes materially
- `gremlin-git`
  - governance officer, project manager, product architect, code reviewer,
    DevOps engineer, QA / release engineering reviewer
- `Gremoire`
  - governance officer, product architect, prompt engineer only when AI
    operating rules change; otherwise keep the human-first vault model light

## Team Rule

If a role is not adding a distinct control, insight, or decision right, do not
activate it just for ceremony.
