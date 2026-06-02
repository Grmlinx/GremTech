# GremTech Governance Principles

## Purpose

Keep GremTech aligned as a governed agency model instead of letting it drift
into an unbounded multi-agent experiment.

## Principles

1. Governance first
   - Governance defines what is allowed before implementation agents optimize
     how to do it.
2. Target repo is the source of truth
   - GremTech reviews, plans, and records recommendations. It does not redefine
     client-repo truth by itself.
3. No hidden authority
   - Every agent must have clear powers, limits, and escalation paths.
4. No silent scope creep
   - New review surfaces, agent powers, or workflow breadth must be explicitly
     absorbed into governance or rejected.
5. Recommendations are traceable
   - Findings, conflicts, and backlog items must remain linkable and reviewable.
6. Upstream agents can block downstream work
   - Governance, security, privacy, and QA can block.
   - UI/UX, code, and prompt roles can recommend, but not overrule.
7. Runtime and prompts must stay aligned
   - If the future runtime behaves more loosely than the prompt contract, the
     runtime is wrong or the contract must be updated deliberately.
8. Boring architecture beats clever ambiguity
   - Prefer explicit orchestration, explicit queues, explicit outputs, and
     explicit review state.
