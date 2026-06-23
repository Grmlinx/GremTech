# Infrastructure Platform Standard

## Purpose

Define the standard model for infrastructure and platform repos such as
`home-lab`.

These repos are not generic application repos.
Their primary operating problem is safe change, reproducibility, recovery, and
ongoing operational truth.

## Core Rule

For infrastructure repos, correctness is not enough.

The repo must make it clear:
- what the source of truth is
- where execution happens
- how drift is detected
- how recovery is performed
- how proof is recorded

## External Baselines

The preferred external alignment for infrastructure repos is:
- CIS Controls and CIS Benchmarks for baseline hardening and secure configuration
- NIST SP 800-34 Rev. 1 for contingency planning and recovery thinking
- NIST SP 800-61 Rev. 3 for incident-response and recovery discipline
- NIST SP 800-190 for container and orchestrator security concerns
- NIST SP 800-207 and, when relevant, SP 800-207A for zero-trust and cloud-native access boundaries

These are alignment targets, not certification claims.

## Required Traits

An infrastructure repo should normally have:
- human `README.md`
- strong `start.ai`
- explicit current-state memory
- deployment and recovery documentation
- execution-boundary rules
- durable action or chronology surfaces
- verification or baseline-check paths where practical

## Source Of Truth Rule

The repo should state which surfaces are authoritative for:
- desired configuration
- current operational state
- known issues
- action history
- recovery procedure

Do not let those concerns blur together casually.

## Change Rule

Prefer:
- declarative or repeatable change
- narrow host-specific mitigations when warranted
- promotion of proven fixes into durable repo-managed state

Avoid:
- chat-only operations habits
- undocumented hotfixes
- silent divergence between repo intent and live systems

## Recovery Rule

Every meaningful platform component should have a recoverability story.

That story should cover, as appropriate:
- rebuild
- restore
- rollback
- fallback or degraded mode
- verification after recovery

## Verification Rule

Infrastructure changes should not stop at "command succeeded."

Proof should prefer:
- post-change verification commands
- baseline verification scripts
- runbook updates
- known-issue and action-log updates when the change teaches something durable

## Security And Hardening Rule

Infrastructure repos should treat hardening as a baseline concern, not a late add-on.

Apply the depth proportionally, but consider:
- host and OS hardening
- network exposure and segmentation
- secrets placement
- privileged execution boundaries
- dependency and image provenance
- cluster and container security when applicable

## Container And Cluster Rule

If the repo operates container or Kubernetes-style platforms:
- use NIST SP 800-190 as the baseline risk vocabulary
- use applicable CIS Benchmarks for configuration guidance
- keep image, registry, runtime, and orchestration risks explicit

## Incident And Operations Rule

Infrastructure repos should preserve operational learning.

If an outage or mitigation reveals a reusable lesson:
- document it
- make it durable when feasible
- wire it into verification or runbooks where appropriate

## Anti-Patterns

Do not:
- force product-style release ceremony where operational validation is the real need
- treat mutable host fixes as complete without persistence
- assume cluster symptoms are always primary when host evidence points lower
- overcomplicate current-state memory just because the repo is operationally important
