# Harness Portability Model

## Purpose

Explain how `GremTech` wants repos to support multiple AI harnesses without
turning every repo into a maze of duplicated instructions.

## Model

The repo should hold durable behavior once.
Harnesses should adapt that behavior at the edge.

## Recommended Surface Stack

### Human Surface

- `README.md`

### Repo AI Surface

- `start.ai`

### Cross-Harness Surface

- `AGENTS.md` when the repo needs one universal bridge across multiple agent tools

### Harness Adapter Surfaces

- `.codex/`
- `.claude/`
- `.cursor/`
- `.opencode/`
- plugin manifests
- hook wiring

## What Should Stay Shared

Keep these shared:

- repo purpose
- operating rules
- workflow standards
- memory expectations
- review and escalation rules
- templates

## What Can Vary By Harness

Let these vary:

- config file format
- hook/event naming
- adapter packaging
- approval/sandbox syntax
- slash command registration

## Why This Matters

Without this separation, multi-harness support becomes:

- expensive to maintain
- easy to drift
- hard to audit
- inconsistent across repos

The portability rule keeps repo truth durable while still allowing tool-specific
edge behavior.
