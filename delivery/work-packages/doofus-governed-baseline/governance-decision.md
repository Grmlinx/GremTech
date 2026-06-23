# Governance Decision

## Request

Use `Doofus` as the first active rollout target for the lightweight
`GremTech` baseline.

## Decision

Approved.

`Doofus` is the current active rollout target.
`alfred` is observe-only.
`home-lab` is not the active rollout target for the time being.

## Allowed Scope

- `start.ai`
- light governance and release surfaces
- maintainer-facing docs front door
- bounded QA and release decision surfaces

## Non-Negotiables

- keep `Doofus` lightweight
- preserve its practical operator-tool posture
- do not introduce hidden runtime power or background autonomy
- do not add `AGENTS.md` unless there is a real multi-harness need
- do not copy heavier portfolio ceremony into the repo without proof it helps

## Blockers

- any plan that expands `Doofus` into a broader runtime platform without a new
  governance decision
- any change that alters packaging or release behavior without QA proof
- any attempt to treat `alfred` or `home-lab` as the rollout target instead
  of `Doofus`

## Required Follow-Up Gates

- structural change gate
- AI contract gate
- runtime or automation gate
