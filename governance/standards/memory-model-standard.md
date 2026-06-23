# Memory Model Standard

## Purpose

Standardize how portfolio repos preserve truth, continuity, and durable
knowledge.

The portfolio does not use one memory shape everywhere.
It uses a small set of approved memory patterns chosen by repo archetype.

## Universal Rules

- Separate stable control from live working context.
- Separate current truth from chronology.
- Separate durable knowledge from future commitments.
- Promote lessons deliberately instead of hiding them in chat history.
- Keep human-readable entry points even when the repo is AI-assisted.

## Approved Memory Patterns

### Full Operational Memory

Use when:
- the repo is an AI-heavy platform
- multi-session continuity is central
- reusable knowledge must be strongly classified

Pattern:
- `sensory/`
- `working/`
- `short-term/`
- `long-term/`
- `prospective/`
- `consolidation/`

Examples:
- `alfred`

### Agency Learning Memory

Use when:
- the repo is a governance or orchestration layer
- it is expected to improve through many projects
- references, long-term lessons, and future bets all matter

Pattern:
- `sensory/`
- `working/`
- `References/`
- `long-term/`
- `prospective/`
- `consolidation/`

Examples:
- `GremTech`

### Governance-Centered Operational Memory

Use when:
- the repo is primarily infrastructure or operational automation
- current state, decisions, backlog, and actions matter more than abstract
  memory theory

Pattern:
- `governance/context/`
- `governance/todo/`
- `governance/decisions/`
- `governance/experience/`
- `governance/actions/`

Examples:
- `home-lab`

### Human Vault Memory

Use when:
- the repo is a human-managed knowledge base
- simplicity and readability matter more than heavy governance ceremony

Pattern:
- `Inbox/`
- `Notes/`
- `Projects/`
- `References/`

Examples:
- `Gremoire`

### Lightweight Product Memory

Use when:
- the repo is a tool or application
- durable repo knowledge is needed, but a full multi-layer memory model would
  be heavier than the product justifies

Pattern:
- `governance/` or equivalent control surface
- `docs/`
- `decisions/`
- backlog or roadmap surface
- release and validation notes

Examples:
- `Doofus`
- future curated `gremlin-git`

## Placement Test

Ask what role the information plays.

- stable constraint or rule:
  - governance
- active implementation context:
  - working or context
- future commitment or deferred work:
  - prospective, todo, backlog, or revisit register
- durable lesson:
  - experience, references, or semantic memory
- historical record:
  - actions, episodic memory, or dated logs

## Anti-Patterns

- putting stable rules inside short-term notes
- using action logs as the only memory source
- forcing a full six-layer memory model onto a human note vault
- leaving durable lessons only in chat transcripts
- hiding current truth across too many parallel files

## Selection Rule

Choose the lightest memory pattern that still preserves:
- current truth
- durable lessons
- future commitments
- operator orientation

More structure is not automatically better.
The correct structure is the one that preserves useful truth with the least
ongoing friction.
