# Operator Route Contract Standard

## Purpose

Define when an operator-facing UI should keep its route and redirect truth in a
canonical contract instead of scattering it across router code, smoke scripts,
and prose.

## Core Rule

If an operator UI has any combination of:

- case-scoped routes
- compatibility redirects
- opt-in or gated routes
- read-only versus write boundaries
- route-smoke expectations

then the repo should keep a canonical route contract.

## Why It Matters

Complex operator UIs often drift in one of three ways:

- docs describe routes that router code no longer serves
- redirects keep working but no longer reflect an intentional migration model
- smoke checks continue to assert route behavior that no longer matches the
  product contract

A route contract keeps the truth legible.

## Minimum Route Fields

A machine-readable route contract should usually include:

- stable route id
- path pattern
- surface kind such as `dashboard`, `workspace`, `review`, `admin`, or
  `redirect`
- scope such as `global` or `case-scoped`
- access mode such as `read-only`, `operator-write`, `admin`, or `opt-in`
- redirect target when relevant
- smoke requirement such as `required`, `shell-only`, `warning-only`, or
  `not-smoked`
- notes about transition-only or compatibility status where relevant

## Pairing Rule

The preferred pattern is:

- markdown explains the route model, operator expectations, and safety
  boundaries
- router code implements the route behavior
- smoke tests assert the important route and redirect expectations
- the route contract provides canonical stable truth for those surfaces

The contract should reduce drift, not add ceremony for its own sake.

## Compatibility Rule

Retired or redirected routes should stay in the route contract until they are
removed.

Each compatibility route should have:

- explicit redirect target
- support-state note
- removal trigger or exit criteria when known

## Boundary Rule

A route contract should make authority boundaries obvious.

If a route is read-only, case-scoped, admin-only, opt-in, or intentionally
shell-only under certain conditions, the contract should say so directly.

Do not let route existence imply write authority or full feature support.

## Smoke Rule

When route smoke exists, the contract should identify:

- which routes must fully render
- which routes are expected to render shell-only
- which redirects must remain intentional
- which routes may warn instead of pass when upstream state is absent

That keeps smoke semantics aligned with the product surface.

## Promotion Rule

Use a route contract when it materially improves:

- route-shape clarity
- compatibility tracking
- smoke stability
- future runtime or UI review automation

Do not add it to a trivial UI with three obvious routes and no compatibility
state.

## Related Navigation

- [Operator surface standard](operator-surface-standard.md)
- [Review platform standard](review-platform-standard.md)
- [Machine-readable control surface standard](machine-readable-control-surface-standard.md)
- [UI UX standard](ui-ux-standard.md)
