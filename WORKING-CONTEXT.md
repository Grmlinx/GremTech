# Working Context

Last updated: 2026-06-07

## Purpose

Active execution context for the `GremTech` portfolio operating system.

Keep this file focused on:
- current truth
- active queues
- current constraints
- the next useful moves

## Current Truth

- `GremTech` now has a repo-level startup contract in `start.ai`
- the portfolio baseline exists:
  - team charter
  - repo archetypes
  - development lifecycle
  - memory-model standard
  - onboarding standard
  - target repo registry
  - repo profiles
  - onboarding templates
- the current profiled repos are:
  - `alfred`
  - `home-lab`
  - `Doofus`
  - `gremlin-git`
  - `Gremoire`
- the base audit contract is now portfolio-generic
- most role-specific audit prompts are still Alfred-seeded and need later parameterization

## Current Constraints

- there is still no runtime orchestration engine
- target repos have not yet fully adopted the new `GremTech` baseline
- `alfred` is reference-only for now and should not be used as an active rollout
  target until reopened
- harness portability is now part of the model, but only the standards/templates exist so far
- future runtime inspiration now includes capability tiering and explicit
  config/secrets boundaries
- explicit operator surfaces, isolation posture, and scheduled/delegated work
  are now part of the model
- future profile isolation semantics are now part of the runtime contract set
- `GremTech` still has a lightweight memory surface rather than a full active-control-plane memory model
- `home-lab` is not the active rollout target for the time being because it is
  already in a similar development cycle elsewhere
- external framework alignment, UI/UX baseline, and CLI-tool baseline now have
  explicit standards
- a read-only pass over `gremlin-git` now exists as evidence for tool-pattern
  standardization
- `GremTech` now has explicit agency-learning and project-inspiration standards
- a richer hybrid memory model with `References/` and `long-term/` is now part
  of the intended operating system
- a read-only benchmark pass over `alfred` now exists for delivery rigor,
  validation, QA, and audit-control patterns
- validation/readiness, documentation-sync, and repo-audit control now have
  explicit standards and templates in `GremTech`
- explicit release-posture and machine-readable-control-surface standards now
  exist based on deeper Alfred proof-surface patterns
- an Alfred-class platform blueprint and archetype standard now exist inside
  `GremTech`
- Alfred-class runtime-core standards now exist for work units, control-plane
  state, approvals, workers, and review platforms
- Alfred-class is now treated as the named baseline and minimum floor for
  future serious governed repos, while Alfred itself stays in its own
  management lane

## Active Queues

- parameterize the role-specific audit prompt pack
- execute the `Doofus` governed baseline work package
- catalog and classify `gremlin-git` into supported, incubating, and archived lanes using the new read-only assessment
- keep `alfred` as the strongest benchmark for startup contracts and memory discipline without scheduling repo changes there
- use the Alfred benchmark pass to harden proof gates, documentation sync, and
  audit control for future repo rollouts
- use the deeper Alfred pass to shape release posture, support-state catalogs,
  and future repo-surface manifests
- use the Alfred-class blueprint to decide whether the first implementation
  should be a new dedicated repo or a future managed rollout target
- turn the new runtime-core standards into the first generic implementation
  contract set for a future Alfred-class core
- keep Alfred external to that build path unless Alfred's own management
  reopens structural work there
- keep `home-lab` aligned to the lifecycle without treating it as the active rollout target
- keep `Gremoire` intentionally light and human-first
- parameterize the prompt pack so repo-specific Alfred wording no longer leaks into shared roles
- start populating `memory/References/` and `memory/long-term/` with curated project lessons instead of leaving them empty

## Next Useful Moves

1. Execute the `delivery/work-packages/doofus-governed-baseline/` package when the `Doofus` repo is opened for write work.
2. Create a governed tool-catalog path for `gremlin-git` from the read-only assessment.
3. Treat `alfred` as reference-only until the operator reopens it for active rollout work.
4. Keep `home-lab` aligned without selecting it as the current rollout target.
5. Decide which repos should expose `AGENTS.md` in addition to `start.ai`.
6. Parameterize role prompts so audits are repo-aware by default.
7. Populate project inspiration scans and durable reference notes from active work packages.
8. Turn the external-framework alignment and the new proof-gate standards into
   concrete release and security checklists where needed.
9. Decide which future runtime surfaces are local-only, loopback-only, or network-exposed by design.
10. Decide whether future multi-profile support is actually needed, and what it must isolate if it exists.
11. Decide where repo-surface manifests and support-state catalogs become
    mandatory instead of optional.
12. Decide where the first generic Alfred-class core implementation should live.
13. Decide which runtime-core schema gets implemented first: work-unit scaffold,
    control-plane state, or action-request lane.

Current recommendation:
- a new dedicated platform repo is the cleanest host for the first generic
  Alfred-class core

## Update Rule

Keep this file current for the active buildout only.
Promote durable policy into `governance/standards/` and durable portfolio truth into
`portfolio/` or `docs/`.
