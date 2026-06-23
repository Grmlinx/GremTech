# CTO Delivery Workflow

## Purpose

Define the default company-style workflow for `GremTech`.

The operator should be able to talk to one chat surface as if they were talking
to a CTO.
That surface should then:
- classify the request
- activate the right team
- run research and planning
- apply governance and risk gates
- coordinate implementation
- enforce QA and release checks
- return with outcomes, blockers, or decisions

## The User-Facing Surface

The front door is the `CTO Desk`.

The `CTO Desk` is not a separate sovereign role.
It is a governed orchestration surface that combines:
- project manager
- product architect
- governance officer

It may also activate:
- security
- QA / release
- DevOps
- code review
- prompt engineering
- domain specialists

depending on the repo profile and workstream.

## What The User Should Experience

The operator should be able to say things like:

- "Build this feature."
- "Fix this repo."
- "Standardize this workflow."
- "Research how we should do this."
- "Roll this out safely."
- "Audit this before we ship it."

The system should then decide:
- which repo is involved
- what kind of work this is
- what level of risk exists
- which roles need to participate
- what artifacts and gates are required

## Default Flow

### 1. Executive Intake

Owner:
- `CTO Desk`

Output:
- executive intake brief

Tasks:
- capture objective
- identify target repo or repos
- classify workstream
- identify urgency, constraints, and expected outcome

### 2. Triage And Team Activation

Owners:
- project manager
- product architect

Output:
- activated role set
- repo archetype and runtime posture confirmation

Tasks:
- classify the repo archetype
- classify the work as research, implementation, governance, release,
  onboarding, or incident-like remediation
- activate the smallest sufficient team

### 3. Research And Discovery

Owners:
- product architect
- code reviewer
- DevOps engineer
- relevant specialists

Output:
- research brief

Tasks:
- inspect repo reality
- identify current truth versus desired future state
- gather evidence
- identify reusable patterns and known constraints

### 4. Solution Design

Owners:
- product architect
- project manager

Supporting:
- security
- DevOps
- prompt engineer
- specialists as needed

Output:
- implementation plan

Tasks:
- define the proposed path
- define change boundaries
- identify dependencies
- identify which gates are required

### 5. Governance And Risk Gating

Owners:
- governance officer
- security engineer
- QA / release engineering reviewer

Output:
- governance decision
- gate requirements

Tasks:
- set non-negotiables
- confirm trust, runtime, and write boundaries
- block, narrow, or approve the plan

### 6. Implementation

Owners:
- implementation roles appropriate to the repo

Output:
- changed artifacts
- implementation handoffs

Tasks:
- execute the approved plan
- keep changes bounded
- update the right docs, templates, or memory surfaces

### 7. Verification And QA

Owners:
- code reviewer
- QA / release engineering reviewer
- DevOps engineer

Supporting:
- security
- UI
- specialists when needed

Output:
- QA gate record

Tasks:
- run tests, dry runs, or structured validation
- compare implemented behavior against documented intent
- identify regressions, gaps, and residual risks

### 8. Release / Adoption Decision

Owners:
- project manager
- governance officer

Supporting:
- QA / release
- product architect

Output:
- release decision

Tasks:
- decide whether the work is ready
- decide whether more rework is required
- state what follow-up remains

### 9. Closeout And Promotion

Owners:
- `CTO Desk`

Output:
- operator summary
- promoted standards, templates, or repo guidance if warranted

Tasks:
- summarize what happened
- state what is done
- record what future work should reuse

## When The System Keeps Going Without Asking

The system should continue autonomously when:
- repo context is available
- the workstream is classifiable
- implementation path is reasonably inferable
- no authority boundary is crossed
- no major business tradeoff is unresolved

## When The System Must Come Back To The User

The system should escalate back to the operator when:
- target repo or objective is genuinely ambiguous
- destructive action or dangerous authority is required
- scope, priority, or business intent is unclear
- two valid high-level directions exist with real tradeoffs
- governance blocks further work
- QA reveals a decision, not just a fix, is needed

## Governing Rule

The operator should feel like they are talking to one accountable executive
surface, not manually running a committee.

But the executive surface must still preserve:
- evidence
- explicit roles
- explicit gates
- explicit blockers
- explicit ownership
