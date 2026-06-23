# Agent Registry

## Purpose

Define the named GremTech agents, their prompt source, hierarchy placement,
and reporting relationships.

## Current Model

- one seeded prompt file per role under `governance\standards\expert-audit-prompts`
- one machine-readable topology file: `agent-topology.json`
- one profile file per agent for human review and future runtime mapping
- repo-owned skill packs under `..\..\skills\registry\` for reusable methods
- role activation depth guided by the repo profiles under `..\..\portfolio\profiles\`

## Rule

A role is not a runtime just because a prompt exists.

The registry is the bridge between:
- prompts
- skills
- authority
- orchestration
- outputs
- escalation

Add a new agent only when the review or accountability boundary changes.
If the need is repeatable method inside an existing role, add or improve a
skill pack instead.
