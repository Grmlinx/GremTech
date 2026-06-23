# Review Platform Standard

## Purpose

Define the boundaries for review APIs and review UIs in governed repos.

## Core Rule

A review platform is for navigating recorded outcomes, not for silently
becoming the execution or approval surface.

## Default Bias

Read-only review is the default.

If a browser or API surface needs mutation, approval, or execution power, that
must be separately justified and governed.

## Review Surface Responsibilities

A review platform may expose:

- work-unit summaries
- derived records
- findings or decisions
- timelines and activity
- worker state
- approval state
- diagnostics
- report or export artifacts

## Review Surface Non-Goals

A review platform should not casually become:

- raw evidence browser
- model-provider configuration surface
- hidden command runner
- arbitrary file server
- silent approval interface
- substitute for the canonical work-unit records

## Derived Review Contract

If a repo uses a structured review pack, it should define:

- what the pack contains
- where it lives
- what generated it
- what it does not prove by itself

Use `templates/review-pack.json` as the seed shape.

## API Rule

Browser-facing APIs should normally:

- expose derived records and control-plane state
- preserve repo and work-unit boundaries
- reject unsafe path traversal or arbitrary file access
- make fallback or degraded state visible when the preferred derived record is
  missing

## UI Rule

The UI should make its posture visible:

- review-only
- last refreshed
- limited preview
- blocked
- fallback

It should not imply powers it does not actually possess.

## Related Navigation

- [Operator surface standard](operator-surface-standard.md)
- [Governed AI product platform standard](governed-ai-product-platform-standard.md)
- [Machine-readable control surface standard](machine-readable-control-surface-standard.md)
