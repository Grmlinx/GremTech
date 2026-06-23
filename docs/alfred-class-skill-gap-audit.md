# Alfred-Class Skill Gap Audit

## Purpose

Identify the Codex skill and evaluation gaps that matter if `GremTech` is
going to build, audit, and evolve Alfred-class systems responsibly.

This is about the current working environment and the portfolio's future
skill-pack surface, not just one repo.

## Current Useful Surface

The current Codex environment already has helpful generic capabilities for this
class of work:

- browser control for local UI verification
- Chrome and desktop automation when browser or OS interaction matters
- GitHub repo and PR tooling
- document, spreadsheet, and presentation artifact tooling
- `skill-creator` for building custom skills
- image generation/editing when visual assets or mockups matter

This is enough for broad delivery work.
It is not enough to treat Alfred-class evaluation as a mature reusable
discipline yet.

## Available But Bounded

This environment also exposes multi-agent tooling, but it is explicitly
permission-bounded.

That matters because Alfred-class work benefits from independent audit passes,
but those passes should remain governed and intentional rather than becoming an
always-on reflex.

## Priority Skill Gaps

### 1. Repo Semantic Auditor

Needed for:

- comparing code, docs, catalogs, validators, startup contracts, and review
  surfaces
- finding semantic drift across machine-readable and prose surfaces
- checking that support posture, naming, and route boundaries stay aligned

Why it matters:

Alfred-class repos are not validated by tests alone.
They need cross-surface consistency audits.

### 2. Governed Runtime Core Builder

Needed for:

- control-plane state design
- work-unit scaffold design
- deterministic worker boundaries
- typed action-request and approval lanes
- local runtime authority boundaries

Why it matters:

`GremTech` currently has strong standards for these, but not a reusable build
skill for implementing them cleanly.

### 3. Operator UI Product Review

Needed for:

- review-workbench information architecture
- dense operator interface design
- accessibility and usability checks on operational UIs
- derived-versus-source-data boundary review
- case-board, approval-centre, and workspace UX audit patterns

Why it matters:

Normal frontend skills are too generic for Alfred-class operational surfaces.
These are not marketing sites or consumer apps.

### 4. Release Proof And Readiness Auditor

Needed for:

- executable readiness evidence planning
- release-posture review
- documentation-sync contract review
- proof-path classification
- support-state and deprecation review

Why it matters:

Alfred-class repos need a reusable way to audit the truth of a release claim,
not just produce release prose.

### 5. Repo-Owned Skill Pack Authoring

Needed for:

- building repo-local skill packs as governed capability surfaces
- deciding when a skill is the right artifact versus a standard, runbook,
  worker, or template
- validating `SKILL.md` quality, forward-testing, and lifecycle state
- keeping skill packs bounded and non-authoritative where they should be

Why it matters:

If `GremTech` wants to keep learning and to develop the way Alfred learned, it
needs skills as a governed product surface, not just ad hoc prompts.

### 6. Compatibility Retirement Planner

Needed for:

- tracking migration shims and fallback lanes
- documenting why each compatibility surface still exists
- setting exit criteria and removal phases
- preventing temporary support paths from becoming permanent product truth

Why it matters:

The deeper Alfred pass shows this is one of the easiest places for complexity
to persist after the real reason is gone.

## Recommended Order

Build or formalize these skill surfaces in this order:

1. repo-semantic-auditor
2. release-proof-and-readiness-auditor
3. repo-owned-skill-pack-authoring
4. operator-ui-product-review
5. governed-runtime-core-builder
6. compatibility-retirement-planner

This order improves evaluation depth before implementation ambition.

## Immediate Portfolio Actions

From this audit, `GremTech` should:

- define a standard for repo-owned skill packs
- define a standard for compatibility retirement
- expand the capability model so product design, enterprise architecture, and
  skill-surface development are explicit domains
- treat missing skills as product backlog items, not only personal notes

## Current Bootstrap

`GremTech` now has the first drafted repo-owned packs for this lane:

- [repo-semantic-auditor](../skills/registry/repo-semantic-auditor/SKILL.md)
- [release-proof-and-readiness-auditor](../skills/registry/release-proof-and-readiness-auditor/SKILL.md)
- [repo-owned-skill-pack-authoring](../skills/registry/repo-owned-skill-pack-authoring/SKILL.md)
- [operator-ui-product-review](../skills/registry/operator-ui-product-review/SKILL.md)
- [governed-runtime-core-builder](../skills/registry/governed-runtime-core-builder/SKILL.md)
- [compatibility-retirement-planner](../skills/registry/compatibility-retirement-planner/SKILL.md)

They are indexed in
[skill-catalog.json](../governance/standards/skill-catalog.json) and backed by
[skill-pack-standard.md](../governance/standards/skill-pack-standard.md).

## Suggested First Skill Blueprints

If these are later turned into real Codex skills, start with:

- `repo-semantic-auditor`
- `release-proof-and-readiness-auditor`
- `repo-owned-skill-pack-authoring`

Those three would improve both Alfred-class review work and general portfolio
quality fastest.
