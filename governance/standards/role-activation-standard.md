# Role Activation Standard

## Purpose

Define how the `CTO Desk` activates the smallest sufficient delivery team for a
request.

## Core Rule

Every substantive request starts at the `CTO Desk`.

The system should then add only the roles needed to cover:
- planning
- architecture
- governance
- implementation
- validation
- domain-specific risk

Do not activate roles for ceremony alone.

## Activation Inputs

Role activation should consider:
- target repo and repo profile
- repo archetype
- repo change posture
- workstream type
- runtime posture
- trust and authority impact
- release exposure
- domain-specific constraints

## Repo Change Posture Rule

If the target repo is marked observe-only or otherwise not open for active
rollout work, the `CTO Desk` should:
- avoid scheduling repo-mutation work there by default
- treat the repo as a reference or research source when possible
- route active rollout work toward an allowed target instead
- escalate only if the operator explicitly wants to reopen that repo

## Minimum Control Coverage

Before implementation begins, the active team should cover:
- one owner for sequencing
- one owner for structural coherence
- one owner for governance and drift control when scope or power changes
- one owner for validation before release or adoption

## Default Workstream Packs

### Research

Default:
- `project-manager`
- `product-architect`
- `code-reviewer`

Add when justified:
- `devops-engineer`
- `security-engineer`
- domain specialists

### Implementation

Default:
- `project-manager`
- `product-architect`
- `code-reviewer`
- `qa-release-engineering-reviewer`

Add when justified:
- `devops-engineer`
- `security-engineer`
- `prompt-engineer`
- `ui-engineer`
- domain specialists

### Governance

Default:
- `governance-officer`
- `project-manager`
- `product-architect`

Add when justified:
- `security-engineer`
- `qa-release-engineering-reviewer`
- `privacy-legal-compliance-reviewer`
- `licensing-procurement-reviewer`

### Release Or QA

Default:
- `qa-release-engineering-reviewer`
- `project-manager`
- `code-reviewer`

Add when justified:
- `devops-engineer`
- `governance-officer`
- `security-engineer`

### Repo Onboarding

Default:
- `project-manager`
- `product-architect`
- `governance-officer`

Add when justified:
- `prompt-engineer`
- `devops-engineer`
- `security-engineer`

### Runtime Or Automation

Default:
- `project-manager`
- `product-architect`
- `devops-engineer`
- `security-engineer`
- `qa-release-engineering-reviewer`

Add when justified:
- `governance-officer`
- `windows-platform-sre-operations-reviewer`
- `prompt-engineer`

### Incident-Style Remediation

Default:
- `project-manager`
- `security-engineer`
- `windows-platform-sre-operations-reviewer`
- `devops-engineer`

Add when justified:
- `code-reviewer`
- `dfir-expert`
- `incident-response-operations-client-delivery-reviewer`
- `governance-officer`

## Trigger-Based Additions

Add roles when these conditions exist:

- `security-engineer`
  - credentials, secrets, authority, trust boundaries, or external systems are involved
- `devops-engineer`
  - packaging, CI, runtime, environment bootstrap, or deployment behavior changes
- `prompt-engineer`
  - `start.ai`, `AGENTS.md`, role prompts, or AI operating rules change
- `ui-engineer`
  - the operator-facing experience changes materially
- `governance-officer`
  - scope, power, policy, write boundaries, or durable standards change
- `windows-platform-sre-operations-reviewer`
  - workstation, host, scheduler, or recovery behavior matters
- `privacy-legal-compliance-reviewer`
  - regulated data or policy obligations matter
- `licensing-procurement-reviewer`
  - dependency licensing, vendor choice, or supportability matters
- `dfir-expert`
  - defensibility, evidence handling, or forensics-sensitive workflows matter
- `m365-entra-administrator`
  - M365 or Entra integration matters
- `incident-response-operations-client-delivery-reviewer`
  - incident-delivery practicality matters

## Required Output

Each substantive request should resolve into a durable role-activation record
stating:
- active roles
- why they are active
- who owns each phase
- which artifacts are required
- which gates can block progress

Use [../../templates/role-activation-record.md](../../templates/role-activation-record.md).

## Stop Rule

If every live risk surface is already covered by the current team, stop adding
roles.
