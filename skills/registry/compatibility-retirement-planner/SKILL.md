---
name: compatibility-retirement-planner
description: Track, classify, and retire compatibility shims, redirects, fallback lanes, and legacy support surfaces without breaking live support posture. Use when auditing cleanup candidates, planning post-release simplification, or deciding whether a path is still load-bearing.
---

# Compatibility Retirement Planner

## Purpose

Plan subtractive cleanup without breaking real support, proof, or migration
needs.

## Workflow

1. Start with the current compatibility surfaces and support-state claims.
2. Classify why each surface still exists and what still depends on it.
3. Separate live support value from historical residue and convenience.
4. Define exit criteria, proof expectations, and staged retirement order.
5. Record the result in a backlog or ledger instead of leaving it as a chat
   opinion.

## Use This Skill For

- auditing redirects, fallback lanes, legacy parameters, and transition-only
  support paths
- planning post-release simplification without damaging support posture
- deciding whether a compatibility surface is still load-bearing

## Do Not Use It For

- deleting compatibility paths because they look untidy
- treating an unexamined compatibility surface as safe to remove

## References

- [../../../governance/standards/compatibility-retirement-standard.md](../../../governance/standards/compatibility-retirement-standard.md)
- [../../../governance/standards/release-posture-standard.md](../../../governance/standards/release-posture-standard.md)
- [../../../governance/standards/proof-path-classification-standard.md](../../../governance/standards/proof-path-classification-standard.md)
- [../../../governance/standards/operator-route-contract-standard.md](../../../governance/standards/operator-route-contract-standard.md)
- [../../../docs/alfred-read-only-recommendations-pass-02.md](../../../docs/alfred-read-only-recommendations-pass-02.md)
- [../../../docs/alfred-read-only-recommendations-pass-03.md](../../../docs/alfred-read-only-recommendations-pass-03.md)
- [../../../delivery/work-packages/alfred-class-platform-blueprint/candidate-simplification-zones-2026-06-08.md](../../../delivery/work-packages/alfred-class-platform-blueprint/candidate-simplification-zones-2026-06-08.md)

## Validation

- verify every retirement suggestion checks current support value first
- verify proof and route dependencies are considered before recommending
  removal
- verify the result produces a staged plan or durable backlog item
