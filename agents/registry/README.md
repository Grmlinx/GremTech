# Agent Registry

## Purpose

Define the named GremTech agents, their prompt source, hierarchy placement,
and reporting relationships.

## Current Model

- one seeded prompt file per role under `governance\standards\expert-audit-prompts`
- one machine-readable topology file: `agent-topology.json`
- one profile file per agent for human review and future runtime mapping

## Rule

A role is not a runtime just because a prompt exists.

The registry is the bridge between:
- prompts
- authority
- orchestration
- outputs
- escalation
