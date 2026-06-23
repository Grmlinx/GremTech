# Repo Audit Control Standard

## Purpose

Define the governed self-audit loop `GremTech` should use to review repo drift,
growth, readiness, and alignment.

## Scope

Use this control loop when the question is about:

- governance drift
- scope creep
- architecture growth
- trust-boundary expansion
- validation quality
- release readiness
- startup-contract quality
- documentation drift
- whether a repo still fits its intended archetype

This is not the same as normal feature delivery.
It is the portfolio's self-review lane.

## Core Rule

Repo audit work must be durable, role-aware, and evidence-backed.

Substantive findings should not live only in an ad hoc chat thread.

## Required Top Band

For substantive repo audit work, include both:

- `product-owner`
- `governance-officer`

The product owner frames intended scope, acceptance meaning, and product fit.

The governance officer sets non-negotiable constraints, alignment decisions,
and block or allow outcomes.

Lower-layer reviewers do not bypass that top band.

## Control Model

Audit roles:

- provide findings
- sequence review
- synthesize recommendations
- shape work packages
- re-check implemented fixes

Audit roles do not:

- create hidden execution authority
- silently widen runtime power
- treat a recommendation as approval
- convert an operator override into normal governance approval

## Standard Loop

1. frame the audit objective and target repo
2. classify the repo archetype and milestone being assessed
3. open a durable audit run record
4. activate the smallest sufficient review set
5. collect findings with explicit evidence
6. synthesize findings into work packages, gaps, or decisions
7. route approved work through normal implementation and QA gates
8. re-check the implemented outcome
9. promote reusable lessons into standards, templates, docs, profiles, or
   long-term memory

## Output Rule

Audit output should prefer:

- findings first
- evidence-backed claims only
- explicit blockers
- explicit residual risks
- explicit next owner

Before creating a new recommendation note, check whether the same issue already
exists in the current audit or backlog surface.

## Standard Artifacts

Use or update these when the audit is substantive:

- `templates/audit-run.md`
- `templates/recommendation-note.md`
- `templates/work-package.md`
- `templates/governance-decision.md`
- `templates/qa-gate.md`
- `templates/release-decision.md`
- `templates/learning-promotion-note.md`

An audit run should be able to show:

- planned agents
- opened agents
- completed agents
- implementation-gate status
- exception state
- operator override state

## Override Rule

If governance blocks a change and the operator still wants to continue, record
that as an operator override.

Do not relabel an override as normal governance approval.

## Related Navigation

- [Role activation standard](role-activation-standard.md)
- [Work package standard](work-package-standard.md)
- [Agency learning standard](agency-learning-standard.md)
- [Human escalation standard](human-escalation-standard.md)
