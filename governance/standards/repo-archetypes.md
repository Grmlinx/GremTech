# Repo Archetypes

## Purpose

Standardize the portfolio without pretending every repo should look the same.

Each target repo should be classified into an archetype first.
Structure, memory, review depth, and required surfaces follow from that choice.

## Archetypes

### Governed AI Product Platform

Examples:
- `alfred`

Required traits:
- strong `start.ai`
- explicit governance and standards
- explicit memory model
- runbooks for operator paths
- bounded AI and execution surfaces
- release and proof gates
- machine-readable control surfaces where validators or runtime code depend on them

### Infrastructure / Platform Repo

Examples:
- `home-lab`

Required traits:
- human `README.md`
- strong `start.ai`
- current-state memory
- deployment and recovery documentation
- rules for source-of-truth and execution location
- action log or chronology surface

### Operator Tool / Product Repo

Examples:
- `Doofus`
- curated future state for `gremlin-git`

Required traits:
- human `README.md`
- `start.ai`
- implementation docs
- release and validation workflow
- decisions and backlog surfaces
- minimal but explicit governance
- explicit release posture when capability boundaries matter

### Legacy Tool Estate / Script Garden

Examples:
- current `gremlin-git`

Required traits:
- tool catalog or inventory
- supported versus archived split
- onboarding path for promoting scripts into governed tools
- explicit archive policy
- machine-readable support-state or catalog surface once consolidation begins

This archetype is transitional.
The goal is usually to consolidate it into a cleaner operator-tool shape.

### Human-Managed Knowledge Vault

Examples:
- `Gremoire`

Required traits:
- simple human-first operating rules
- durable reference area
- inbox or intake path
- lightweight AI contract that protects human readability

Do not force software-product governance ceremony onto this archetype.

### Governance / Orchestration Layer

Examples:
- `GremTech`

Required traits:
- team charter
- cross-repo standards
- templates
- portfolio profiles
- adoption playbooks
- explicit decision rights and escalation rules

## Selection Rule

If a repo mixes multiple concerns, choose the dominant operating problem first.

Examples:
- if the repo's main risk is operator execution and recovery, treat it as
  infrastructure first
- if the repo's main value is durable human knowledge, treat it as a vault
  first
- if the repo's main value is reusable shipped tooling, treat it as an
  operator tool first

Do not choose an archetype based on aspiration alone.
Choose it based on how the repo is actually used.
