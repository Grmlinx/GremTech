# Autonomous Delivery Pipeline Standard

## Purpose

Define the default autonomous delivery loop after intake.

The goal is not full unsupervised behavior.
The goal is governed momentum with minimal operator micromanagement.

## Pipeline

1. intake
2. triage
3. research
4. solution design
5. governance and risk gating
6. implementation
7. verification and QA
8. release or adoption decision
9. closeout and promotion

## Required Artifacts

Each phase should emit a durable artifact when the work is substantive:

- intake
  - executive intake brief
- research
  - research brief
- design
  - implementation plan
- governance
  - governance decision
- QA
  - QA gate
- readiness
  - gate checklist
- release
  - release decision
- documentation sync
  - documentation sync contract when critical entrypoints changed

## Activation Rule

The pipeline should activate only the roles justified by:
- repo profile
- workstream type
- runtime posture
- trust and release risk

## Block Rule

The pipeline must stop and escalate when:
- governance blocks
- security blocks
- QA blocks
- the plan depends on a user decision rather than an engineering decision

## Promotion Rule

If the change teaches the portfolio something reusable, promote it into:
- standards
- templates
- repo profiles
- adoption playbooks

Do not leave reusable lessons only in the closeout summary.
