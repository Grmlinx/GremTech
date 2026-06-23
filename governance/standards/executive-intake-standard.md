# Executive Intake Standard

## Purpose

Define how a single executive-facing chat request enters the governed delivery
system.

## Core Rule

The user should not need to specify every role manually.

The executive intake layer should:
- interpret the request
- classify the workstream
- identify the target repo
- respect the repo's current change posture
- activate the right team

## Intake Fields

Every substantive request should resolve into:
- request summary
- target repo or repos
- repo change posture
- objective
- workstream type
- urgency
- constraints
- success condition

## Workstream Types

The intake layer should classify the request into one or more of:
- research
- implementation
- governance
- release / QA
- repo onboarding
- architecture
- runtime / automation
- incident-style remediation

## Default Owners

The executive intake layer is the `CTO Desk`, composed of:
- project manager
- product architect
- governance officer

## Ask-Back Rule

The intake layer should ask the user only when one of these is missing and
material:
- target repo
- objective
- authority boundary
- meaningful priority tradeoff
- definition of success

If the missing detail is not material, proceed with a reasonable assumption and
make it explicit.
