# Operator Routes Need Canonical Contracts

## Lesson

Complex operator UIs should not leave route truth split across prose, router
code, and smoke scripts without one canonical contract.

## Why It Matters

Case-scoped routes, redirects, read-only boundaries, and smoke expectations
change together.
Without a shared contract, drift is predictable.

## Reuse Rule

Future Alfred-class builds should:

1. keep a machine-readable route contract when route complexity justifies it
2. record redirect targets and compatibility status explicitly
3. mark which routes must fully smoke and which are shell-only
4. make route existence separate from authority

## Promotion Targets

- `governance/standards/operator-route-contract-standard.md`
- `templates/operator-route-contract.json`
- `docs/alfred-read-only-recommendations-pass-03.md`
