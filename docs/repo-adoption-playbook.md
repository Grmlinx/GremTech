# Repo Adoption Playbook

## Purpose

Give a concrete standardization path for the current portfolio.

`GremTech` can define the rules and templates here.
Each target repo should then adopt the relevant parts in its own tree.

## Alfred

Current posture:
- observe-only for now
- use as a benchmark and source of reusable operating ideas
- do not schedule active rollout work there until the operator reopens it
- treat it as managed in-place by its own lane while it approaches release

Current strengths:
- first repo in the portfolio at true Alfred-class scale
- strongest `start.ai` contract in the portfolio
- strongest memory model
- strongest governance separation
- strongest validation and readiness discipline
- strongest documentation-sync discipline
- strongest governed repo-audit control loop
- strongest explicit release-posture discipline
- strongest use of machine-readable policy surfaces

Adopt and preserve:
- treat Alfred-class as the starting baseline for future serious governed repos
- use as the benchmark for AI startup contracts
- use as the benchmark for full operational memory
- continue treating skills, runbooks, and governance as separate control layers
- use as the benchmark for layered proof gates and non-destructive smoke design
- use as the benchmark for documentation-sync enforcement on critical paths
- use as the benchmark for governed self-audit without hidden authority
- use as the benchmark for explicit release posture instead of vague readiness claims
- use as the benchmark for machine-readable control surfaces when they genuinely reduce ambiguity

Standardization next steps:
- parameterize expert-review prompts so they are not `alfred`-specific when
  reused from `GremTech`
- keep absorbing Alfred's rigor as shared standards and templates rather than
  as cargo-cult repo structure
- do not start subtractive cleanup from `GremTech` without Alfred's own
  management deciding how its interdependencies should be handled
- keep repo profile aligned from `GremTech` without treating Alfred as the next
  rollout target
- defer any Alfred repo-surface expansion until the operator explicitly
  reopens it

## home-lab

Current posture:
- defer active rollout for now
- keep aligned to the lifecycle while its own similar development cycle is in flight

Current strengths:
- strong operational `start.ai`
- governance used as current-truth memory
- clear control model and execution location

Adopt and preserve:
- keep governance-centered memory instead of forcing a heavier model
- keep rebuildability and repo-managed recovery as core standards

Standardization next steps:
- align role activation and review gates with the `GremTech` team charter
- keep decisions, known issues, and runbooks explicitly tied to durable fixes
- keep harness portability light unless there is a real multi-harness need
- align future hardening, recovery, and platform-risk reviews to
  `governance/standards/infrastructure-platform-standard.md`

## Doofus

Current posture:
- active rollout target
- current first-choice candidate for baseline adoption from `GremTech`

Current strengths:
- clear product-facing `README.md`
- practical workflow and install guidance

Gaps to close:
- no visible AI startup contract
- no explicit governance or decision surface
- no obvious release-governance layer

Standardization next steps:
- add `start.ai`
- add a light governance surface with decisions, backlog, and release rules
- add an explicit release posture that separates supported, approval-required,
  and out-of-scope capability
- add a docs front door that separates user docs from maintainer docs
- add `AGENTS.md` only if Doofus is meant to support multiple agent harnesses
- execute the active work package under
  `delivery/work-packages/doofus-governed-baseline/`

## gremlin-git

Current posture:
- classify before expanding
- use read-only assessment to understand promotion candidates before any major restructure

Current strengths:
- broad raw tool inventory
- clear evidence of reusable utility patterns
- strong signal for actual operator-tool preferences

Gaps to close:
- no visible governance layer
- no clear supported versus archived split
- no single product boundary

Standardization next steps:
- treat it as a script-garden consolidation program before adding more scope
- create a tool catalog with supported, incubating, and archived states
- promote the best tools into governed operator-tool repos over time
- avoid cloning the same instructions into multiple harness-specific surfaces
  before the supported tool set is clear
- use [gremlin-git-read-only-assessment.md](gremlin-git-read-only-assessment.md)
  to shape the CLI standard and promotion criteria

## Gremoire

Current strengths:
- clean human-first vault model
- good separation between inbox, notes, projects, and references
- clear AI operating rules

Adopt and preserve:
- keep the vault simple
- keep durable knowledge in `References/`
- keep AI behavior subordinate to human readability

Standardization next steps:
- use `GremTech` only for light-touch standards here
- avoid pushing software-product governance ceremony into the vault
- add a universal `AGENTS.md` surface only if the vault genuinely needs
  multi-harness AI support
