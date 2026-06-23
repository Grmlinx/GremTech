# Development Lifecycle

## Purpose

Define the standard build loop for portfolio work.

This lifecycle applies to:
- new repos
- structural refactors
- shared automation
- AI operating-contract changes
- memory-model changes

## Standard Flow

1. Classify
   - identify the target repo
   - choose the repo archetype
   - classify the change as governance, implementation, release, memory, or onboarding
2. Frame
   - define scope
   - define constraints
   - define the smallest team that must review the change
3. Design
   - prefer templates and existing standards first
   - decide what belongs in the target repo versus in `GremTech`
4. Implement
   - make the smallest coherent change set
   - keep repo-specific truth inside the target repo
   - keep shared standards and templates inside `GremTech`
5. Prove
   - run layered validation, smoke checks, dry runs, or structured manual verification
   - verify critical entrypoint docs stay aligned when startup or operator
     behavior changed materially
   - separate implemented from merely documented
6. Promote
   - update docs, templates, runbooks, decisions, or memory surfaces that changed materially
   - update the target repo profile when new expectations are now durable
7. Close
   - record what future repos should reuse
   - leave the adoption path clearer than before

## Mandatory Gates

### Structural Change Gate

Required when:
- top-level directories change
- a repo changes archetype
- a new long-term surface is introduced

Minimum reviewers:
- product architect
- governance officer

### Runtime / Automation Gate

Required when:
- scripts, builds, CI, packaging, deployment, or execution surfaces change

Minimum reviewers:
- code reviewer
- DevOps engineer
- QA / release engineering reviewer

### AI Contract Gate

Required when:
- `start.ai`
- prompt packs
- governed role contracts
- model-facing workflow instructions

Minimum reviewers:
- prompt engineer
- governance officer
- product architect

### Trust Boundary Gate

Required when:
- secrets
- elevated execution
- external platforms
- tenant access
- new write surfaces

Minimum reviewers:
- security engineer
- governance officer
- relevant specialist

## Promotion Rule

Do not promote a local workaround, chat habit, or one-off success into a
portfolio standard without proof that it is:
- reusable
- understandable
- safer than the status quo
- worth carrying across repos
