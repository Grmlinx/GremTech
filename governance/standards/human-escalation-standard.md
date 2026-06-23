# Human Escalation Standard

## Purpose

Define when the autonomous workflow must return to the operator.

## Core Rule

Do not escalate just because work is hard.
Escalate when the remaining problem is a human decision, authority boundary, or
business tradeoff.

## Escalate To The User When

- destructive action needs approval
- authority-bearing work exceeds the current mandate
- multiple valid high-level directions exist with real tradeoffs
- repo choice or scope is materially ambiguous
- governance blocks and cannot be resolved with evidence alone
- QA exposes a product or risk decision, not just a defect
- the required success condition is unclear

## Do Not Escalate For

- ordinary implementation difficulty
- need for research
- internal role disagreement that can be resolved by evidence
- routine testing and QA findings
- normal documentation updates

## Response Shape

When escalating, state:
- what decision is needed
- why the system cannot decide it safely alone
- what options exist
- what tradeoff matters

Keep it short and decision-oriented.
