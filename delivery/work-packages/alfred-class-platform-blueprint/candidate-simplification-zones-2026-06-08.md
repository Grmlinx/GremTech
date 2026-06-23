# Alfred Candidate Simplification Zones

## Purpose

Capture the Alfred post-release simplification zones that appear plausible from
read-only review.

This is an internal `GremTech` learning note, not an external instruction to
change Alfred now.

## Boundary

Do not treat this as a recommendation to strip Alfred during its current
production-bound phase.

Any subtractive change inside Alfred still belongs to Alfred's own management,
after release stability, dependency mapping, and support posture are clear.

## Candidates

### 1. Alpha-era proof surfaces and naming

Why this is a candidate:

- Alfred's current state says `repo alpha-smoke`, `repo alpha-status`,
  `repo validate`, `repo doctor --deep`, and tool validation are green, with no
  alpha blockers and no unchecked gate items.
- The repo still carries active `alpha` command surfaces and
  `memory/prospective/alpha-execution-program` proof sources.

Evidence:

- `alfred/memory/working/current_state.md`
- `alfred/alfred.py`

Possible strip-back:

- archive or reclassify alpha-only execution-packet material once it is purely
  historical
- rename surviving operational surfaces if they are no longer genuinely
  alpha-scoped

Keep until:

- Alfred's own release and support model no longer depends on alpha-language
  gates as the authoritative proof surface

### 2. Compatibility-only startup parameters and root fallback paths

Why this is a candidate:

- `OpenOperatorConsole` is still accepted by case startup, but the startup rule
  explicitly says it is accepted for compatibility and ignored
- control-root autodiscovery and projects/tool root fallback are explicitly
  described as legacy or compatibility-only paths
- the controlled production-style stage already treats compatibility fallback
  roots as preflight failures unless the operator uses an explicit override

Evidence:

- `alfred/scripts/control/Start-AlfredCaseSession.ps1`
- `alfred/alfred.py`
- `alfred/memory/working/current_state.md`

Possible strip-back:

- remove compatibility-only parameters after all supported callers migrate
- quarantine legacy fallback paths behind lab-only tooling instead of normal
  operator surfaces

Keep until:

- Alfred management confirms that no supported host, helper, or chat lane still
  relies on those compatibility paths

### 3. Explicit RunAs fallback for Windows image analysis

Why this is a candidate:

- the Windows image lane prefers the reviewed scheduled-task/elevated-worker
  path
- explicit RunAs fallback is disabled by default and framed as a fallback, not
  the normal path

Evidence:

- `alfred/alfred.py`
- `alfred/memory/working/current_state.md`

Possible strip-back:

- retire the RunAs fallback if the supported privileged Windows image workflow
  is fully covered by the scheduled-task/elevated-worker path across real
  operator contexts

Keep until:

- Alfred has enough production evidence to prove that the supported privileged
  image lane does not need the fallback for recovery or host variance

### 4. Legacy review projections and older derived-artifact inference

Why this is a candidate:

- `case-review-pack.v1` is now the intended shared review contract and is
  proven on current Windows-image and M365 practice lanes
- Alfred still keeps projection and fallback behavior when durable records are
  missing

Evidence:

- `alfred/README.md`
- `alfred/webUI/README.md`
- `alfred/memory/working/current_state.md`

Possible strip-back:

- narrow projection/fallback review behavior to legacy-case compatibility only
- move supported current cases toward fail-closed or explicit degraded-mode
  handling when durable review records are missing

Keep until:

- every supported case family reliably emits the durable records the WebUI and
  review surfaces expect

### 5. Transitional WebUI route and mock-mode scaffolding

Why this is a candidate:

- retired global/control routes are still being explicitly redirected
- mock mode is still retained as a staged backend fallback

Evidence:

- `alfred/webUI/README.md`

Possible strip-back:

- remove retired redirect routes when they are no longer needed for support or
  migration
- narrow mock mode to explicit development use once the supported backend path
  is stable everywhere Alfred expects it to be stable

Keep until:

- Alfred management has enough operational confidence that those transitions are
  no longer carrying real support value

## Not Recommended For Removal

Do not treat the following as obvious simplification targets from outside:

- validation and semantic invariant checks
- documentation-sync controls
- machine-readable control surfaces
- approval records and action-request discipline
- control-plane state and worker policy
- case-review-pack as the shared review contract
- AI assurance inventories and fallback-rule visibility

Those read as core Alfred-class controls, not incidental scaffolding.

## Use In GremTech

The main lesson for `GremTech` is not "make Alfred smaller now."

The lesson is:

- build Alfred-class systems with fewer temporary compatibility surfaces
- prefer one authoritative review contract early
- keep fallback lanes explicit and removable
- make transitional proof scaffolding easy to archive once it stops being
  authoritative
