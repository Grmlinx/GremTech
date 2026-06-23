# Alfred Read-Only Recommendations Pass 03

## Purpose

Capture the next deeper Alfred recommendations that emerged from a read-only
pass over proof coverage, route-surface contracts, operator UI hierarchy, and
platform API maintainability.

This is still not a request to modify Alfred from outside its own management
lane.
It is an evidence-based recommendation set for post-release stewardship and for
`GremTech` to absorb into future Alfred-class builds.

## Source Surfaces Reviewed

- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\.github\workflows\alfred-validation.yml`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\memory\working\current_state.md`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\governance\standards\alfred-surface.json`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\governance\standards\documentation-sync-contract.json`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\webUI\README.md`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\webUI\src\app\router.tsx`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\webUI\src\pages\CaseWorkspacePage.tsx`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\webUI\src\pages\CasesDashboardPage.tsx`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\webUI\src\pages\ApprovalCentrePage.tsx`
- `C:\Users\anand\OneDrive\Study\Cybersecurity\GitHub\alfred\src\platform_api\app.py`

## Executive Verdict

Alfred still looks strong.
The deeper gap is no longer missing governance or missing proof discipline.
It is that some of the strongest truths are still expressed across several
surfaces instead of one canonical contract:

- CI proof versus supported proof
- WebUI route shape versus redirect compatibility
- source-boundary status versus handoff guidance
- platform API boundary layer versus dashboard assembly

That is the kind of drift pressure Alfred-class repos should remove after
stabilization.

## Recommendations

### 1. Align CI truth with supported proof truth

The current validation workflow proves useful structural and repo-health layers:

- WebUI lint
- WebUI typecheck
- WebUI build
- tool catalog validation
- repo doctor
- repo validate

That is good evidence.
It is not the full supported proof story Alfred now tells about itself.

The deeper mismatch is:

- `current_state.md` treats `repo alpha-smoke --json` as the real synthetic
  operator-path proof
- `alfred.py` exposes `repo alpha-smoke` as a dedicated root-CLI wrapper around
  `scripts/control/alfred_alpha_smoke.py`
- `current_state.md` describes that harness as non-destructive, timeout-bounded,
  and isolated to repo-local scratch roots
- `current_state.md` treats Docker-backed WebUI validation plus
  `Test-AlfredWebUi.ps1` as the supported WebUI proof lane on the reviewed
  machine
- the CI workflow does not currently run either of those proof paths

Recommendation:

- keep CI structural proof exactly because it is fast and deterministic
- add an explicit proof-path register that classifies what CI does and does not
  prove
- because `repo alpha-smoke --json` is already framed as a non-destructive,
  synthetic root-CLI proof path, treat it as normal CI-grade proof unless a
  specific hidden environmental dependency still blocks that
- if Docker-backed WebUI route smoke is the supported production-style proof
  lane, either run that in a dedicated CI/pre-release job or record it as a
  separate required gate with durable evidence

The goal is not "put every heavy proof step into CI."
The goal is "do not let CI green status silently stand in for the full supported
proof posture."

### 2. Put the WebUI route and redirect model behind one canonical contract

The route truth currently spans at least three surfaces:

- `webUI/src/app/router.tsx` hardcodes route definitions and redirect targets
- `webUI/README.md` describes the case-first route shape and lists retired
  routes that should redirect
- the WebUI smoke contract checks route shells and redirect behavior by reading
  `router.tsx` directly and regex-matching specific redirect patterns

`alfred-surface.json` correctly points at the smoke script as an entrypoint,
but it does not appear to hold the route contract itself.

Recommendation:

- add a machine-readable route contract for the operator UI
- include active routes, case-scoped routes, compatibility redirects,
  privileged or opt-in routes, and expected smoke coverage
- treat README prose, smoke expectations, and router implementation as derived
  from that contract or at least synced against it

This would reduce drift when a route is renamed, retired, re-scoped, or moved
behind a different boundary.

### 3. Reduce duplicated boundary readouts in the case workspace

`CaseWorkspacePage.tsx` is doing the right thing at the trust-boundary level.
It repeats that the browser is read-only, shows source-boundary references, and
keeps the handoff visible.

The improvement opportunity is more specific than "make it prettier."

Right now the same two path-level items are repeated in both:

- `Case Folder`
- `Case Handoff`

Those are:

- original evidence folder
- registered parser input folder

Recommendation:

- keep one canonical source-boundary block
- reference that block from the handoff section instead of repeating the raw
  path readout twice
- extract the source-boundary readout into a dedicated component so the page
  keeps its honesty while reducing scan noise

This preserves the safety signal and improves operator scanability.

### 4. Budget platform API extraction by responsibility boundary

`src/platform_api/app.py` is currently carrying several stable concerns in one
file:

- boundary-safe artifact preview
- knowledge and administration payloads
- dashboard composition
- case workspace assembly
- HTTP transport and auth handling

That does not mean the API is wrong.
It means the next maintainability win is now clear.

Recommendation:

- split HTTP transport and auth from payload assembly
- split case workspace assembly from broader dashboard aggregation
- keep browser-safe redaction and boundary-sensitive helpers in an explicit
  boundary layer
- preserve current payload shape while shrinking the number of reasons one file
  must change

This is the API equivalent of the earlier `alfred.py` and case-workspace
modularization recommendation, but now with a more defensible split line.

### 5. Preserve the read-only honesty as a non-negotiable invariant

The deeper UI pass reinforced something Alfred is already doing well:

- empty states are explicit
- approval pages state that browser writes are not enabled
- route shells remain visible without implying authority they do not have

Recommendation:

- treat these not as incidental page copy but as product invariants
- carry them into future route contracts, proof-path registers, and review
  platform standards
- do not add browser write capability until the audit record, approval record,
  and support posture for that lane are all equally explicit

This is more a rule to preserve than a bug to fix, but it is important enough
to record as a recommendation.

## GremTech Absorption

`GremTech` should absorb these lessons as first-class Alfred-class rules:

- supported proof needs explicit classes, not one undifferentiated green state
- operator UI routes need a canonical contract when redirects and case scoping
  matter
- dense operator pages should keep trust-boundary honesty while reducing
  repeated readouts
- post-release modularization should split by boundary and responsibility, not
  by arbitrary line count
- read-only review honesty is part of the product contract

## Related GremTech Targets

- `governance/standards/proof-path-classification-standard.md`
- `governance/standards/operator-route-contract-standard.md`
- `templates/proof-path-register.json`
- `templates/operator-route-contract.json`
- `docs/alfred-class-platform-blueprint.md`
