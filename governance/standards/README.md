# Standards

## Purpose

This directory holds machine-readable or reusable control surfaces for
GremTech.

## Current Standards

- [repo-archetypes.md](repo-archetypes.md)
  - approved portfolio repo classes
- [development-lifecycle.md](development-lifecycle.md)
  - standard build and promotion loop
- [executive-intake-standard.md](executive-intake-standard.md)
  - how a CTO-style request enters the system
- [autonomous-delivery-pipeline-standard.md](autonomous-delivery-pipeline-standard.md)
  - the default delegated company workflow after intake
- [validation-and-readiness-standard.md](validation-and-readiness-standard.md)
  - how repos prove readiness through layered executable evidence
- [documentation-sync-standard.md](documentation-sync-standard.md)
  - how critical operator and maintainer docs stay aligned with real behavior
- [repo-audit-control-standard.md](repo-audit-control-standard.md)
  - the governed self-audit loop for repo drift, growth, and readiness review
- [recommendation-tracking-standard.md](recommendation-tracking-standard.md)
  - how recommendation notes, issue maps, and backlogs should stay linked
- [release-posture-standard.md](release-posture-standard.md)
  - how repos state supported, bounded, approval-required, and blocked capability
- [proof-path-classification-standard.md](proof-path-classification-standard.md)
  - how repos classify structural proof, smoke proof, supported proof, and compatibility proof
- [machine-readable-control-surface-standard.md](machine-readable-control-surface-standard.md)
  - when policy should have a structured companion surface instead of prose only
- [operator-route-contract-standard.md](operator-route-contract-standard.md)
  - when complex operator UI routes and redirects need a canonical machine-readable contract
- [compatibility-retirement-standard.md](compatibility-retirement-standard.md)
  - how compatibility shims, fallback lanes, and redirects stay explicit and removable
- [governed-ai-product-platform-standard.md](governed-ai-product-platform-standard.md)
  - the Alfred-class baseline for the deepest governed product archetype
- [skill-pack-standard.md](skill-pack-standard.md)
  - how repo-owned skill packs are created, validated, and maintained
- [skill-catalog.json](skill-catalog.json)
  - machine-readable index of repo-owned skill packs
- [agent-skill-separation-standard.md](agent-skill-separation-standard.md)
  - when to add a skill pack versus when to add a new agent
- [work-unit-record-standard.md](work-unit-record-standard.md)
  - the durable per-unit record model for governed runtime work
- [control-plane-state-standard.md](control-plane-state-standard.md)
  - the state classes and authority model for governed runtime coordination
- [action-request-and-approval-standard.md](action-request-and-approval-standard.md)
  - typed authority-bearing requests, approvals, and execution boundaries
- [deterministic-worker-standard.md](deterministic-worker-standard.md)
  - how worker classes should be cataloged and constrained
- [review-platform-standard.md](review-platform-standard.md)
  - the boundary model for read-only review APIs and UIs
- [role-activation-standard.md](role-activation-standard.md)
  - how the CTO Desk chooses the smallest sufficient team
- [work-package-standard.md](work-package-standard.md)
  - how substantive requests become durable execution packets
- [agency-learning-standard.md](agency-learning-standard.md)
  - how GremTech should learn and improve through project work
- [project-inspiration-standard.md](project-inspiration-standard.md)
  - how major work should compare similar local and external projects first
- [selective-assimilation-standard.md](selective-assimilation-standard.md)
  - how GremTech should absorb strengths from outside systems without cargo-culting them
- [agent-orchestration-pattern-standard.md](agent-orchestration-pattern-standard.md)
  - how GremTech should distinguish flows, autonomous teams, handoffs, and shared runtime surfaces
- [human-escalation-standard.md](human-escalation-standard.md)
  - when the system must return to the operator
- [external-framework-alignment.md](external-framework-alignment.md)
  - how internal governance maps to external quality, security, and delivery baselines
- [infrastructure-platform-standard.md](infrastructure-platform-standard.md)
  - the standard model for infrastructure and platform repos
- [memory-model-standard.md](memory-model-standard.md)
  - approved memory patterns by repo type
- [ui-ux-standard.md](ui-ux-standard.md)
  - the usability and accessibility baseline for user-facing surfaces
- [cli-tool-standard.md](cli-tool-standard.md)
  - the standard model for command-line and operator-tool products
- [capability-tiering-standard.md](capability-tiering-standard.md)
  - core, optional, and compatibility capability packaging
- [config-and-secrets-boundary.md](config-and-secrets-boundary.md)
  - keep secrets separate from normal config surfaces
- [operator-surface-standard.md](operator-surface-standard.md)
  - define allowed dispatch, approval, and output surfaces
- [runtime-isolation-standard.md](runtime-isolation-standard.md)
  - what isolation does and does not mean
- [profile-isolation-standard.md](profile-isolation-standard.md)
  - how named profiles or tenants should separate state and routing
- [scheduled-and-delegated-work-standard.md](scheduled-and-delegated-work-standard.md)
  - rules for cron, background jobs, and delegated work
- [executive-request-workflow.json](executive-request-workflow.json)
  - machine-readable phase model for the CTO-style workflow
- [role-activation-matrix.json](role-activation-matrix.json)
  - machine-readable routing policy for role activation, artifacts, and gates
- [repo-onboarding-standard.md](repo-onboarding-standard.md)
  - required surfaces for onboarding a repo
- [repo-startup-contract.md](repo-startup-contract.md)
  - minimum `start.ai` contract
- [harness-portability-standard.md](harness-portability-standard.md)
  - keep durable behavior shared and harness adapters thin
- [workflow-surface-policy.md](workflow-surface-policy.md)
  - canonical workflow source first, compatibility shims second
- [expert-audit-prompts/README.md](expert-audit-prompts/README.md)
  - seeded expert prompt pack plus future review-contract surface
- [../../agents/registry/agent-topology.json](../../agents/registry/agent-topology.json)
  - current machine-readable agent hierarchy and reporting relationships

## Rule

Standards should be stable, explicit, and usable by future runtime code.
