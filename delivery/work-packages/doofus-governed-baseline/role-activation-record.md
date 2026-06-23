# Role Activation Record

## Request

- summary: baseline-govern `Doofus` as the first active rollout target
- repo: `Doofus`
- workstream: `repo onboarding` plus `light governance adoption`

## Core Owners

- executive surface: `CTO Desk`
- sequencing owner: `project-manager`
- architecture owner: `product-architect`
- governance owner: `governance-officer`
- QA or release owner: `qa-release-engineering-reviewer`

## Activated Roles

- `project-manager`
  - why active: this is the first active rollout package and needs sequencing
- `product-architect`
  - why active: the repo needs new durable surfaces without breaking its product shape
- `governance-officer`
  - why active: new startup and governance surfaces change the repo control model
- `code-reviewer`
  - why active: implementation changes in `Doofus` should stay bounded and coherent
- `qa-release-engineering-reviewer`
  - why active: build, smoke-test, and release proof need an explicit gate
- `devops-engineer`
  - why active: install, build, packaging, and release scripts already exist and should stay coherent

## Required Artifacts

- executive intake brief
- research brief
- implementation plan
- governance decision
- QA gate
- release decision

## Blocking Gates

- structural change gate:
  - blocker owner: `governance-officer`
- AI contract gate:
  - blocker owner: `governance-officer`
- runtime or automation gate:
  - blocker owner: `qa-release-engineering-reviewer`

## Escalation Triggers

- operator decision required when:
  - `Doofus` would need more than a light governance baseline
  - multi-harness support becomes a real requirement
  - release workflow changes imply new trust or authority boundaries

## Next Phase

- current phase: `research-and-design`
- next owner: `product-architect`
