# External Framework Alignment

## Purpose

State which external frameworks `GremTech` aligns to when defining governance,
security, quality, and delivery rules.

## Core Rule

`GremTech` currently uses an internal governance model.

It is not claiming formal certification against ISO, NIST, or OWASP programs.
But the internal model should deliberately align to strong external baselines
instead of inventing everything from scratch.

## Primary External Baselines

### Quality And Management System Thinking

Use:
- ISO 9000 family
- especially ISO 9001 quality-management principles

Use it for:
- documented responsibilities
- repeatable process design
- review and approval gates
- customer or operator outcome focus
- continual improvement

Inside `GremTech`, this should shape:
- work-package flow
- lifecycle standards
- change and release discipline

### Information Security Management

Use:
- ISO/IEC 27001 concepts

Use it for:
- risk-based thinking
- explicit control ownership
- confidentiality, integrity, and availability concerns
- change control around trust boundaries
- continual review of security posture

Inside `GremTech`, this should shape:
- secrets and config boundaries
- operator-surface rules
- runtime-isolation rules
- governance decisions for new powers

### Secure Software Development

Use:
- NIST SSDF
- OWASP SAMM

Use them for:
- secure SDLC expectations
- verification discipline
- code and dependency hygiene
- vulnerability-prevention thinking
- maturity progression over time

Inside `GremTech`, this should shape:
- implementation and QA gates
- release readiness rules
- future secure-development checklists

### Web And API Security

Use when the repo actually exposes those surfaces:
- OWASP ASVS for application verification expectations
- OWASP Top 10 as a common risk vocabulary

Do not force web-app controls onto repos that are primarily CLI tools,
infrastructure repos, or knowledge vaults.

### Infrastructure And Platform Operations

For infrastructure and platform repos, additionally align to:
- CIS Controls
- CIS Benchmarks
- NIST SP 800-34 Rev. 1
- NIST SP 800-61 Rev. 3
- NIST SP 800-190
- NIST SP 800-207 and, when relevant, SP 800-207A

These are governed further in:
- [infrastructure-platform-standard.md](infrastructure-platform-standard.md)

## Experience And Accessibility Baselines

For UI-bearing tools, align to:
- WCAG 2.2 AA as the accessibility baseline
- usability heuristics for interaction quality
- Laws of UX as a design-pattern inspiration source

These are governed further in:
- [ui-ux-standard.md](ui-ux-standard.md)

## CLI Baseline

For operator tools and command-line products, align to:
- command-line best practices such as human-first and composable CLI design
- the actual operator patterns visible in `Doofus` and `gremlin-git`

These are governed further in:
- [cli-tool-standard.md](cli-tool-standard.md)

## Scope Rule

Not every repo should inherit every control at the same depth.

Apply external baselines according to:
- repo archetype
- runtime posture
- change posture
- trust and release risk

## Claim Rule

Do not claim:
- ISO certification
- NIST conformity
- OWASP compliance

unless there is real evidence and formal scope to support the claim.

Use the language:
- aligned to
- informed by
- mapped against

unless stronger proof exists.
