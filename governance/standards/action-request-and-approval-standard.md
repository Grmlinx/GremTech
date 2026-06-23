# Action Request And Approval Standard

## Purpose

Define how authority-bearing work should be requested, approved, recorded, and
executed in a governed runtime.

## Core Rule

Authority-bearing work must not travel as a vague chat intention.

It should become a typed action request before execution.

## When This Applies

Use this standard when work may:

- authenticate to a platform
- mutate external state
- run privileged host actions
- launch non-trivial automation outside ordinary read-only review
- cross a trust boundary that deserves explicit approval

## Required Action Request Fields

An action request should usually include:

- action request id
- work-unit id
- work-unit root
- purpose
- authority basis
- operator or requestor
- target scope summary
- time window or time basis when relevant
- operation class
- allowlisted action id
- expected outputs
- credential boundary statement
- approval required flag
- limitations

Use `templates/action-request.json` as the seed shape.

## Forbidden Request Content

Action requests should not contain fields such as:

- raw passwords
- API keys
- access tokens
- refresh tokens
- client secrets
- arbitrary shell payloads
- unbounded target lists when scope should be explicit

## Approval Rule

If approval is required, the approval record should bind to the exact request
being approved.

An approval record should usually include:

- approval id
- request id
- decision
- approver
- decision basis
- approval timestamp
- expiry or freshness boundary when relevant
- exact request hash or equivalent binding

Use `templates/approval-record.json` as the seed shape.

## Execution Rule

Execution should run only:

- allowlisted actions
- against the approved request
- through a visible or reviewable execution lane

Do not convert the approval system into a general shell.

## Review Rule

Action requests, decisions, and outputs should be durable and reviewable.

## Related Navigation

- [Operator surface standard](operator-surface-standard.md)
- [Release posture standard](release-posture-standard.md)
- [Governed AI product platform standard](governed-ai-product-platform-standard.md)
