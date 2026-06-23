# home-lab Profile

## Archetype

Infrastructure / platform repo

## Current Change Posture

Defer active rollout for now.
Keep it aligned with the lifecycle, but do not treat it as the current
portfolio rollout target while its similar development cycle is in flight.

## What To Preserve

- governance as current-truth memory
- strong control model
- rebuildability over ad hoc fixes
- runbook-driven recovery

## Runtime Posture

Operator-driven automation with explicit execution boundaries.
Repo-managed automation is good; silent or ambiguous background autonomy is not.

## Default Review Lanes

- governance
- product architecture
- security
- QA / release
- Windows platform / SRE / operations
- DevOps
- code review

## Standardization Focus

- keep durable mitigations documented in repo-managed memory
- keep operational truth concise and current
- avoid introducing unnecessary memory complexity
- align hardening, recovery, and cluster-risk thinking to the infrastructure standard
