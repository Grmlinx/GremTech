# External Pattern Harvest 2026-06-14

## Purpose

Record the external online pattern scan used to improve `GremTech` beyond its
current local inspirations.

This is the practical application of the `Sword of Gryffindor` rule:
- absorb the strengthening traits
- reject the unnecessary baggage

## Sources Reviewed

### OpenHands

- source:
  - `https://github.com/All-Hands-AI/OpenHands`
- key patterns:
  - shared SDK as the engine
  - separate CLI, local GUI, cloud, and enterprise surfaces
  - evaluation infrastructure as a first-class companion surface
  - enterprise packaging separated from the open core
- absorb:
  - one core engine with multiple surfaces above it
  - evaluation and benchmark infrastructure as a planned Alfred-class layer
  - control-plane and enterprise packaging as optional outer layers, not the
    core architecture
- reject or avoid:
  - treating hosted/cloud packaging as the core product shape

### CrewAI

- source:
  - `https://github.com/crewAIInc/crewAI`
- key patterns:
  - `Crews` for autonomous teams
  - `Flows` for production, event-driven control
  - structured state inside flows
  - official skill distribution for coding-agent guidance
- absorb:
  - the autonomy-versus-flow distinction as explicit runtime vocabulary
  - structured state and explicit branching for production workflows
  - skill-pack distribution as a deliberate capability surface
- reject or avoid:
  - inheriting framework-specific language as the only vocabulary
  - treating product cloud/control-plane features as mandatory for the core

### MetaGPT

- source:
  - `https://github.com/geekan/MetaGPT`
- key patterns:
  - software company as multi-agent system
  - role-based assembly line
  - SOP-driven collaboration
  - requirement-to-artifact chain
- absorb:
  - SOP and artifact-chain discipline for product-manager, architect,
    engineer, QA, and governance role choreography
  - explicit mapping from request to intermediate artifacts, not only final
    output
- reject or avoid:
  - one-prompt product-generation framing as a serious delivery baseline

### AutoGen And Microsoft Agent Framework

- sources:
  - `https://github.com/microsoft/autogen`
  - `https://github.com/microsoft/agent-framework`
- key patterns:
  - layered architecture
  - event and message oriented core
  - extension surfaces
  - benchmarking surfaces
  - graph-based orchestration
  - durability, restartability, observability, and human-in-the-loop control
- absorb:
  - layered runtime shape
  - graph or handoff oriented orchestration vocabulary
  - provider flexibility and cross-runtime openness
  - production-first posture around observability and HITL control
- reject or avoid:
  - treating AutoGen itself as the preferred long-term foundation because it is
    now in maintenance mode

## Durable Improvements Added To GremTech

This scan directly motivated:

- `governance/standards/selective-assimilation-standard.md`
- `governance/standards/agent-orchestration-pattern-standard.md`
- `templates/external-pattern-assessment.md`

It also strengthens the case for future Alfred-class work to include:

- one core runtime with multiple surfaces
- explicit flow versus autonomous-team selection
- evaluation infrastructure as a first-class capability
- role-SOP and artifact-chain discipline
- lifecycle-aware upstream selection
