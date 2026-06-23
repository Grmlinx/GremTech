# Agent Hierarchy

## Purpose

Define the authority stack for GremTech so independent audits do not collapse
into flat, conflicting agent opinions.

Activation rule:
- classify the repo archetype first
- then activate only the layers and specialists the repo actually needs

## Layers

### Layer 1: Governance

- governance officer

Authority:
- final governance veto
- decides whether drift or scope expansion is acceptable
- can require rework from every lower layer

### Layer 2: Leadership

- project manager
- product architect

Authority:
- decomposes the review problem
- sequences agents
- synthesizes cross-agent findings
- translates governance constraints into execution plans

### Layer 3: Risk and Assurance

- security engineer
- privacy / legal / compliance reviewer
- licensing / procurement reviewer
- QA / release engineering reviewer
- Windows platform / SRE / operations reviewer

Authority:
- can issue blocking findings inside their control domain
- can force escalation to governance or leadership
- cannot redefine governance principles unilaterally

### Layer 4: Implementation and Platform

- DevOps engineer
- AI engineer
- code reviewer
- prompt engineer

Authority:
- audits implementation quality and runtime shape
- can propose fixes and challenge assumptions
- cannot overrule higher-layer governance or risk decisions
- cannot use prompts or implementation convenience to create new authority by
  accident

### Layer 5: Domain Specialists

- DFIR expert
- M365 / Entra administrator
- incident response operations / client delivery reviewer

Authority:
- issue domain-specific findings
- validate specialist workflows
- escalate domain blockers upward

### Layer 6: Experience

- UI engineer

Authority:
- optimize user experience, interaction clarity, and frontend design within
  upstream constraints
- can flag usability, visibility, and workflow issues
- cannot set security, governance, or system authority rules

## Design Rule

Governance sits at the top.
UI/UX sits at the bottom.

That is intentional.
The visual and interaction layer should be downstream of governed decisions,
not a backdoor for redefining agent power, data exposure, or operating scope.
