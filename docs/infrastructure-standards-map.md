# Infrastructure Standards Map

## Purpose

Explain how `GremTech` expects infrastructure repos such as `home-lab` to map
their operating model to external standards and practical controls.

## Baseline Areas

### Secure Configuration And Hardening

Use:
- CIS Controls
- CIS Benchmarks

Apply to:
- hosts
- operating systems
- Kubernetes or related control planes when relevant
- cloud or platform components where applicable

### Recovery And Contingency

Use:
- NIST SP 800-34 Rev. 1

Apply to:
- backup and restore thinking
- rebuild and rollback planning
- recovery testing expectations

### Incident Response And Operational Learning

Use:
- NIST SP 800-61 Rev. 3

Apply to:
- preparation
- response workflow
- recovery discipline
- post-incident learning capture

### Container And Orchestrator Security

Use:
- NIST SP 800-190
- relevant CIS Kubernetes Benchmarks when Kubernetes is in scope

Apply to:
- images
- registries
- runtime boundaries
- orchestrator configuration

### Identity And Access Boundaries

Use:
- NIST SP 800-207
- NIST SP 800-207A when cloud-native access patterns are in scope

Apply to:
- explicit trust boundaries
- service-to-service policy
- hybrid or multi-location access assumptions

## home-lab Implication

For `home-lab`, this means the repo should continue emphasizing:
- runbook-driven recovery
- repo-managed durable mitigations
- explicit execution boundaries
- host and cluster verification after changes
- concise current-state governance surfaces

It should not be pushed toward:
- unnecessary product-style ceremony
- hidden automation
- complex memory structures that obscure current truth
