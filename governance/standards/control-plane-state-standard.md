# Control Plane State Standard

## Purpose

Define the durable local state that a governed runtime should expose for
coordination, visibility, and safe restart behavior.

## Core Rule

If a repo grows beyond single-shot scripts and into multi-step governed runtime
behavior, it should expose control-plane state explicitly.

The control plane is the durable coordination layer, not an invisible internal
detail.

## Required State Classes

Strong governed runtimes should expose durable state for:

- work units
- jobs
- workers
- locks
- tasks
- diagnostics
- approvals when authority-bearing work exists

Not every repo needs every class at the same maturity.
An Alfred-class platform does.

## Authority Rule

The runtime must define:

- which root or roots are authoritative
- which are machine-local overrides only
- what operations fail closed when authority context is missing

Do not allow mutating operations to silently pick an arbitrary runtime root.

## Restart Rule

Control-plane state should be durable enough that:

- a restart does not erase active coordination state
- stale locks, jobs, and worker residue can be reviewed explicitly
- fresh sessions can see current reality without relying on memory alone

## Visibility Rule

The operator should be able to inspect the control plane through governed
surfaces such as:

- root CLI status commands
- diagnostics views
- read-only review API
- read-only review UI

## Machine-Readable Rule

If the control plane is part of the supported runtime, define a structured
manifest for the state classes and their bindings.

Use `templates/control-plane-manifest.json` as the seed shape.

## Related Navigation

- [Governed AI product platform standard](governed-ai-product-platform-standard.md)
- [Operator surface standard](operator-surface-standard.md)
- [Scheduled and delegated work standard](scheduled-and-delegated-work-standard.md)
