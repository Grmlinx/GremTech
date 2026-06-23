# Explicit Compatibility Ledgers

## Lesson

Compatibility surfaces should be treated as governed product state, not as
invisible implementation residue.

## Why It Matters

Without an explicit ledger, migration shims, redirects, fallback lanes, and
deprecated parameters quietly become normal product truth.

## Reuse Rule

Future Alfred-class builds should:

1. label compatibility paths clearly
2. record why they still exist
3. define exit criteria
4. review them during release and audit cycles

## Promotion Targets

- `governance/standards/compatibility-retirement-standard.md`
- `docs/alfred-read-only-recommendations-pass-02.md`
