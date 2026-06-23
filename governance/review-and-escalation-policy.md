# Review And Escalation Policy

## Purpose

Define how GremTech agents talk to each other without collapsing into an
unstructured swarm.

The operator should normally interact with the `CTO Desk`, not with each role
individually.

## Standard Audit Loop

1. Project manager identifies the target repo and intended workstream.
2. Product architect classifies the repo archetype if it is not already clear.
3. Governance officer sets the top-level constraints.
4. Project manager chooses the smallest sufficient review order.
5. Risk and assurance agents review before implementation approval.
6. Implementation agents review after constraints are visible.
7. Specialist roles review only where the repo profile justifies them.
8. UI engineer reviews last unless a pure frontend task is explicitly scoped.
9. Project manager synthesizes.
10. Governance officer signs off, blocks, or demands another pass.

## Front Door Rule

Plain-English operator requests should enter through the `CTO Desk`.
The `CTO Desk` then decides:
- which roles activate
- what research is needed
- which gates apply
- whether the system should keep going or escalate back to the operator

For substantive work, record that activation explicitly using:
- `templates/role-activation-record.md`
- `governance/standards/role-activation-standard.md`
- `governance/standards/role-activation-matrix.json`

## Allowed Communication Pattern

- Any agent may send findings upward.
- Lateral discussion is allowed when mediated by the project manager or product
  architect.
- Blocking findings must be escalated upward immediately.
- Lower layers may challenge higher layers with evidence, but may not overrule
  them.

## Conflict Rule

When two agents disagree:
- first compare repo evidence
- then classify whether the disagreement is governance, risk, architecture,
  implementation, or UX
- escalate to the highest relevant upstream owner

## Drift Rule

If a new capability, prompt, runtime surface, or output path changes the system
meaningfully, governance must either:
- explicitly absorb it, or
- reject it and narrow the system back down

## Portfolio Rule

When the task touches a profiled repo, read the matching file under
`portfolio/profiles/` before expanding scope beyond local implementation.
