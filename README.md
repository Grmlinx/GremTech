# GremTech

`GremTech` is the governance and orchestration layer for the wider development
portfolio.

Its job is to standardize how repos such as `alfred`, `home-lab`, `Doofus`,
`gremlin-git`, and `Gremoire` are:
- classified
- governed
- reviewed
- documented
- given durable memory and startup contracts

The managed repos remain their own source of truth.
`GremTech` carries the reusable operating system around them.

## What Exists Now

`GremTech` now provides:
- an explicit agency team and decision model
- an explicit CTO Desk routing and role-activation model
- a delivery work-package lane for active rollout targets
- explicit validation, readiness, and release-gate standards
- documentation-sync discipline for critical startup and operator paths
- a governed repo-audit control loop for portfolio self-review
- explicit release-posture rules for supported versus bounded capability
- a standard for when governance surfaces should become machine-readable
- an Alfred-class platform blueprint for future governed AI product builds
- runtime-core standards for work units, control-plane state, approvals,
  workers, and review platforms
- explicit external-framework, UI/UX, and CLI-tool standards
- an explicit infrastructure-platform standard for repos like `home-lab`
- an agency-learning memory model with references and long-term lessons
- repo archetypes and onboarding standards
- a development lifecycle for cross-repo work
- a standard for memory-model selection
- a harness portability and workflow-surface policy
- a machine-readable portfolio registry
- target-repo profiles for the current repo estate
- reusable templates for startup contracts and onboarding
- a seeded expert-audit prompt pack and agent registry

It does not yet provide:
- a runtime orchestration service
- autonomous agent execution
- persistent queue management
- database-backed audit state
- parameterized prompt rendering across every role prompt
- inter-agent messaging infrastructure

## Portfolio Targets

Current profiled repos:
- `alfred`
- `home-lab`
- `Doofus`
- `gremlin-git`
- `Gremoire`

See:
- [portfolio/README.md](portfolio/README.md)
- [portfolio/targets.json](portfolio/targets.json)
- [docs/repo-adoption-playbook.md](docs/repo-adoption-playbook.md)

## Cross-Harness Lane

`GremTech` now also treats cross-harness support as a first-class concern.

See:
- [AGENTS.md](AGENTS.md)
- [WORKING-CONTEXT.md](WORKING-CONTEXT.md)
- [governance/standards/harness-portability-standard.md](governance/standards/harness-portability-standard.md)
- [governance/standards/workflow-surface-policy.md](governance/standards/workflow-surface-policy.md)
- [docs/harness-portability-model.md](docs/harness-portability-model.md)

## Structure

```text
GremTech/
- agents/
  - registry/
- delivery/
  - work-packages/
- docs/
- governance/
  - standards/
    - expert-audit-prompts/
- memory/
  - sensory/
  - working/
  - References/
  - long-term/
  - prospective/
  - consolidation/
- portfolio/
  - profiles/
- templates/
```

## Operating Rule

Do not standardize by flattening every repo into the same tree.
Standardize by:
- choosing the right archetype
- activating the right review lanes
- using the right memory pattern
- reusing the right templates

## Start Here

- [start.ai](start.ai)
- [governance/README.md](governance/README.md)
- [governance/team-charter.md](governance/team-charter.md)
- [docs/cto-delivery-workflow.md](docs/cto-delivery-workflow.md)
- [docs/executive-routing-model.md](docs/executive-routing-model.md)
- [memory/README.md](memory/README.md)
- [governance/standards/README.md](governance/standards/README.md)
- [docs/README.md](docs/README.md)
- [portfolio/README.md](portfolio/README.md)
- [delivery/README.md](delivery/README.md)
