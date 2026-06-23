# Runtime Isolation Standard

## Purpose

Define what actually counts as isolation for governed agent systems.

This standard is informed by `hermes-agent`'s explicit security stance: the
real boundary is the operating system or an equivalent external sandbox, not an
in-process approval UI, hook, or scanner.

## Core Rule

In-process controls are governance aids, not hard containment.

Real isolation comes from:
- OS-level boundaries
- container boundaries
- remote-host boundaries
- cloud-sandbox boundaries
- explicit network and filesystem policy

## Non-Boundaries

These do not count as isolation by themselves:
- prompt instructions
- tool allowlists
- pattern scanners
- output redaction
- approval popups
- in-process plugin checks

They are still useful, but they are not containment.

## Isolation Postures

### Host-Native

The agent runs with the operator's normal host access.

Use only when:
- the trust envelope is understood
- the accessible files, network, and credentials are acceptable for the task

### Terminal / Tool Backend Isolation

Shell and file actions are routed through a container, remote host, or sandbox.

Use when:
- risky execution should be narrower than the host itself
- repo work needs filesystem or network limits

### Whole-Process Isolation

The entire agent process tree runs inside a sandbox with explicit policy.

Use when:
- higher-risk automation is needed
- multiple external surfaces or plugins exist
- stronger containment is worth the extra operational cost

## Trust Envelope Rule

Every governed runtime should define its trust envelope:

- what files can it reach
- what networks can it reach
- what credentials can it read
- what external surfaces can it talk to

If the trust envelope is unclear, the runtime posture is incomplete.

## Plugin Rule

Plugins and extensions inherit the runtime's privileges unless a stronger
boundary exists outside the process.

Do not describe plugins as safely isolated just because they are optional.

## Governance Rule

When a repo grows from local operator tooling into a more persistent runtime,
reassess:
- operator surfaces
- isolation posture
- secrets exposure
- plugin trust
- background jobs

Do not reuse the same trust assumptions by inertia.
