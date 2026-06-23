# Alfred Read-Only Recommendations Pass 02

## Purpose

Capture the deeper Alfred recommendations that emerge from read-only review
after the Alfred-class baseline and simplification-zone work.

This is not a request to modify Alfred from outside its own management lane.
It is an evidence-based recommendation set for post-release stewardship and for
`GremTech` to absorb into future Alfred-class builds.

## Source Surfaces Reviewed

- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\memory\working\current_state.md`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\alfred.py`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\src\platform_api\app.py`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\docs\operator-surfaces.md`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\governance\standards\development-review-deployment-gate.md`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\governance\standards\documentation-sync.md`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\governance\standards\alfred-surface.json`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\webUI\README.md`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\webUI\src\app\router.tsx`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\webUI\src\layouts\AppShell.tsx`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\webUI\src\pages\CasesDashboardPage.tsx`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\webUI\src\pages\CaseWorkspacePage.tsx`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\webUI\src\pages\ApprovalCentrePage.tsx`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\webUI\src\services\httpClient.ts`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\webUI\src\services\platformService.ts`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\webUI\src\styles\index.css`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\.github\workflows\alfred-validation.yml`

## Recommendations

### 1. Add an explicit compatibility and deprecation ledger

Alfred has several paths that are clearly marked as compatibility or staged
fallback surfaces:

- `OpenOperatorConsole` is accepted and ignored by case startup
- control-root autodiscovery is legacy/local compatibility only
- projects/tool-root compatibility fallback is blocked in production-style
  preflight unless explicitly overridden
- WebUI mock mode remains an intentional staged backend fallback
- retired global/control routes are still being redirected

That is not a problem by itself.
The gap is portfolio-wide discipline around how those surfaces are tracked and
retired.

Recommendation:

- keep every compatibility path in a named deprecation ledger
- give each one an owner, rationale, support value, and exit criteria
- review them on the release cadence instead of only when they become annoying

### 2. Separate historical alpha proof from active production language

Alfred now has both:

- an active production-promotion summary
- green alpha proof surfaces with no remaining alpha blockers

That suggests the underlying quality bar is strong, but the language is in a
mixed state.

Recommendation:

- after the current release lane stabilizes, decide which alpha surfaces remain
  truly operational
- archive or rename any remaining alpha-only surfaces that are now historical
- keep only the proof surfaces that still carry live support meaning

The goal is not to erase proof history.
The goal is to keep support posture legible for future operators and maintainers.

### 3. Budget post-release modularization for the current monoliths

Alfred has a few files that are now large enough to create review and change
friction even when the architecture is sound:

- `alfred.py`: 11,602 lines
- `src/platform_api/app.py`: 3,356 lines
- `webUI/src/pages/CaseWorkspacePage.tsx`: 644 lines
- `webUI/src/styles/index.css`: 1,537 lines

The recommendation is not "split them immediately during release hardening."
The recommendation is:

- create a post-release modularization budget
- split by stable responsibility boundaries, not arbitrary size targets
- preserve current behavior and validation proof while reducing maintenance
  pressure

The two highest-value splits appear to be:

- platform API boundary/auth/router concerns versus dashboard composition and
  case-review assembly
- case workspace shell/orchestration versus section-level panels and view-model
  mapping

### 4. Keep pushing supported review lanes toward durable records only

Alfred already has the right direction:

- `case-review-pack.v1` is the intended shared review contract
- durable `findings-records.json` and `approval-records.json` are preferred
- fallback and projection states are visible instead of hidden

Recommendation:

- keep projection and older derived-artifact inference only as explicit
  degraded or legacy compatibility modes
- move supported current workflows toward durable-record-only review paths
- fail clearly when a supported case surface should have emitted durable review
  records but did not

That keeps the review workbench honest and makes missing records a fixable
product issue instead of a soft inference path forever.

### 5. Make the supported WebUI proof path brutally explicit

The current state says Docker-backed WebUI validation is the supported proof
path on the reviewed machine, while host `npm run build` is blocked by PATH
Node 16.15.0.

Recommendation:

- keep supported proof paths explicit in release and onboarding surfaces
- do not let unsupported local-host build paths look like normal expectations
- classify host build, Docker build, and mock mode clearly as supported,
  maintainer-only, or transition-only where appropriate

This is a release-posture clarity issue, not just a developer convenience issue.

### 6. Do not strip the load-bearing control surfaces

The deeper pass does not support subtracting these:

- validator and semantic invariant checks
- documentation-sync contracts
- machine-readable control catalogs
- typed approval and action-request discipline
- review-pack contracts
- read-only review boundaries
- assurance inventories and fallback visibility

Those are Alfred-class strengths, not obvious overbuild.

## GremTech Absorption

`GremTech` should absorb these lessons as first-class rules for future
Alfred-class builds:

- compatibility paths must be explicit, owned, and removable
- production naming should not drift with historical buildout language
- large core surfaces need planned decomposition after they stabilize
- durable review contracts should become the normal path, not a side path
- supported proof paths must be obvious for operators and maintainers

## Related GremTech Targets

- `governance/standards/compatibility-retirement-standard.md`
- `governance/standards/governed-ai-product-platform-standard.md`
- `docs/alfred-class-skill-gap-audit.md`
- `delivery/work-packages/alfred-class-platform-blueprint/candidate-simplification-zones-2026-06-08.md`
