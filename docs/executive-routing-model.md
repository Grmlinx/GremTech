# Executive Routing Model

## Purpose

Explain how a plain-English operator request becomes governed company work
inside `GremTech`.

This is the routing layer behind the `CTO Desk`.

## Core Model

The operator speaks to one surface:
- `CTO Desk`

The `CTO Desk` then performs four things before deep implementation starts:
- interpret the request
- classify the workstream
- activate the smallest sufficient team
- declare the artifacts and gates that now govern the work

This prevents two bad failure modes:
- the operator having to micromanage every role
- the system pretending to be autonomous while hiding who decided what

## The Request Path

1. The operator gives a plain-English request.
2. The `CTO Desk` writes an executive intake brief.
3. The request is classified by repo, workstream, and risk triggers.
4. The role activation standard selects the smallest sufficient team.
5. A role-activation record declares:
   - active roles
   - active gates
   - required artifacts
   - phase owners
6. For major work, the research phase should include a project inspiration scan
   using relevant local and external references.
7. Those artifacts are grouped into a work package when the effort is
   substantive.
8. The work proceeds through the delivery pipeline.
9. Blocking gates either stop the work or return a short decision request to
   the operator.

## Team Activation Logic

The routing layer should think in this order:

1. What repo is this?
2. What kind of work is this?
3. Does it change trust, runtime, policy, release risk, or operator experience?
4. Which roles are required to cover those risks exactly once?

It should not think:
- who has not been invited yet
- how to make the process look busy

## Decision Rights

The routing layer does not erase decision rights.

It must preserve that:
- repo owners own priorities and exception approval
- governance owns drift and policy boundaries
- project management owns sequencing and synthesis
- architecture owns structural coherence
- QA owns validation and release evidence
- security owns trust and authority concerns

See:
- [../governance/decision-rights.md](../governance/decision-rights.md)
- [../governance/review-and-escalation-policy.md](../governance/review-and-escalation-policy.md)

## Durable Artifacts

Every substantive request should be able to leave behind:
- work package
- executive intake brief
- role-activation record
- project inspiration scan
- research brief
- implementation plan
- governance decision
- QA gate
- release decision

This is how the workflow stays inspectable and later automatable.

## Machine-Readable Surface

The future runtime should use:
- [../governance/standards/role-activation-standard.md](../governance/standards/role-activation-standard.md)
- [../governance/standards/role-activation-matrix.json](../governance/standards/role-activation-matrix.json)
- [../governance/standards/executive-request-workflow.json](../governance/standards/executive-request-workflow.json)
- [../governance/standards/work-package-standard.md](../governance/standards/work-package-standard.md)
- [../governance/standards/project-inspiration-standard.md](../governance/standards/project-inspiration-standard.md)

The prose defines intent.
The JSON files define execution policy.
