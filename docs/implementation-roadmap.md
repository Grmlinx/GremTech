# Implementation Roadmap

## Phase 1: Portfolio Baseline

- define team charter
- define repo archetypes
- define memory-model standard
- define onboarding standards
- define portfolio profiles and registry
- define reusable templates

## Phase 2: Review Contracts

Contracts now defined in repo:
- `CTO Desk` executive intake
- role-activation policy and machine-readable routing
- blocking and escalation rules
- shared-source versus harness-adapter contracts
- capability tiering
- config and secrets boundaries
- operator surfaces
- isolation posture
- profile isolation
- scheduled and delegated work rules
- validation and readiness gates
- documentation-sync enforcement
- repo-audit control loop

Remaining work:
- parameterize the prompt pack by target repo and archetype
- define agent invocation format
- define audit run record format
- define inter-agent message schema
- formalize blocking and escalation state transitions for runtime execution
- define machine-readable gate-checklist and audit-run schemas if runtime
  automation needs them
- keep recommendation issue-map and backlog workflows aligned with actual audit
  usage
- decide where the first Alfred-class generic platform implementation should
  live

## Phase 3: Repo Adoption

- roll the startup contract and onboarding standard into target repos
- align repo-local governance and memory surfaces to the chosen archetype
- promote the best script-garden utilities into governed tool repos

## Phase 4: Orchestration

- choose backend runtime
- add persistent state
- add queueing and scheduling
- add audit session tracking
- add repo-target onboarding flow
- add scheduled task and delegated-work contracts
- keep local-first persistence and thin operator surfaces explicit
- add explicit queue or board contracts before multi-actor runtime expansion
- add evaluation harnesses for repo-owned skills and review surfaces

## Phase 5: Delivery And Hardening

- add recommendation synthesis views
- add machine-readable recommendation workflows only if dashboards or runtime
  automation truly need them
- add auth and access control
- add audit logging
- add policy enforcement
- add regression testing for hierarchy and drift rules
- add compatibility-retirement review into release and audit cycles
