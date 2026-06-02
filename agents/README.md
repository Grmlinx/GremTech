# Agents

## Purpose

This directory turns the seeded prompt pack into an explicit agency-style agent
system.

The prompt pack defines how a role thinks.
The registry defines where that role sits in the hierarchy, who it reports to,
who it can challenge, and what kind of output it is expected to produce.

## Areas

- [registry/README.md](registry/README.md)
- [registry/agent-topology.json](registry/agent-topology.json)

## Rule

Agents are not peers by default.
Authority, escalation, and synthesis must stay explicit.
