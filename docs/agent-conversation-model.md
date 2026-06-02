# Agent Conversation Model

## Purpose

Provide a future runtime contract for how agents should exchange findings.

## Conversation Types

1. Upward escalation
   - lower layer sends findings to a higher layer
2. Lateral clarification
   - two same-layer or adjacent-layer agents compare evidence
3. Leadership synthesis
   - project manager or product architect consolidates conflicts
4. Governance ruling
   - governance officer decides whether drift or scope expansion is acceptable

## Required Message Fields

Every future inter-agent message should carry:
- sender
- recipient
- target repo
- review scope
- finding summary
- evidence references
- severity
- blocking or advisory state
- requested action

## Blocking Rule

A blocking finding must always move upward.
It should never die inside a lateral conversation.
