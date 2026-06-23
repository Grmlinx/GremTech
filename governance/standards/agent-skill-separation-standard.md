# Agent Skill Separation Standard

## Purpose

Define when `GremTech` should add a new agent versus when it should add a new
skill pack.

## Core Rule

Add a new skill pack by default.
Add a new agent only when accountability, authority, or review boundaries
change.

## Add A Skill Pack When

Use a skill pack when the repo needs:

- a repeatable method
- a bounded evaluation workflow
- a reusable build or review discipline
- a domain-specific operating pattern inside an existing accountability lane
- supporting scripts, references, or assets for repeated work

## Add A New Agent When

Use a new agent only when the repo needs:

- a distinct decision-rights boundary
- a different escalation path
- an independent review function that should be able to disagree
- a genuinely separate accountability lane such as governance, product,
  architecture, legal, QA, or specialist operations

## Anti-Patterns

Do not add a new agent because:

- a new tool appeared
- a new file type appeared
- a new UI screen appeared
- a repeated task happened twice
- a skill pack, runbook, or workflow profile would solve the problem cleanly

Do not use agent count as a proxy for capability depth.

## Product Rule

Agents own:

- accountability
- synthesis
- escalation
- challenge and approval boundaries

Skill packs own:

- repeatable method
- bounded procedural knowledge
- reusable agent-facing capability

## Review Rule

Before adding a new agent, answer:

- what accountability boundary does this add
- why can an existing agent not use a skill pack instead
- what decision-rights or escalation change justifies the new role

If those answers are weak, add or improve a skill pack instead.

## Related Navigation

- [Skill pack standard](skill-pack-standard.md)
- [Role activation standard](role-activation-standard.md)
- [Workflow surface policy](workflow-surface-policy.md)
