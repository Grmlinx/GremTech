# Review And Escalation Policy

## Purpose

Define how GremTech agents talk to each other without collapsing into an
unstructured swarm.

## Standard Audit Loop

1. Governance officer sets the top-level constraints.
2. Project manager frames the audit question and chooses the review order.
3. Product architect defines the systems lens where architecture matters.
4. Risk and assurance agents review next.
5. Implementation agents review after constraints are visible.
6. Domain specialists review where relevant.
7. UI engineer reviews last unless a pure frontend task is explicitly scoped.
8. Project manager synthesizes.
9. Governance officer signs off, blocks, or demands another pass.

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
