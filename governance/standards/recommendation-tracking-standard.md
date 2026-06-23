# Recommendation Tracking Standard

## Purpose

Define how `GremTech` should track expert findings, overlaps, and follow-up
work so recommendations do not disappear into one-off notes.

## Core Rule

If a review produces a recommendation note, the recommendation must also be
checked against:

- the current issue map
- the current recommendation backlog

Do not let the note be the only durable place where the issue exists.

## Required Surfaces

The minimum recommendation-tracking surface is:

1. recommendation notes
   - dated or scoped findings with evidence and recommended actions
2. issue map
   - the deduplicated view of underlying issues and overlaps
3. backlog
   - the cross-note follow-up work that still needs action

The note explains the finding.
The issue map explains overlap.
The backlog explains what is still open.

## Issue Map Rule

The issue map should record:

- stable issue id
- short issue summary
- current status
- related recommendation notes
- overlap type when a new note hits an existing issue

Use overlap labels such as:

- `duplicate`
- `partial`
- `conflicting`
- `additive`

## Backlog Rule

Any recommendation that implies real follow-up should create or update a
backlog item unless the action is already completed in the same change.

Each backlog item should usually state:

- stable backlog id
- short summary
- priority
- status
- owner role
- source issue or recommendation note
- next durable target such as a standard, template, skill, doc, or runtime
  change

## Status Rule

Recommended issue statuses:

- `open`
- `watching`
- `planned`
- `in-progress`
- `resolved`
- `superseded`

Recommended backlog statuses:

- `open`
- `planned`
- `in-progress`
- `blocked`
- `done`
- `deferred`

Do not use "noted" as a substitute for a real state.

## Update Workflow

When a new recommendation arrives:

1. check the issue map for overlap
2. update or create the mapped issue entry
3. check whether the implied follow-up already exists in backlog
4. update the backlog instead of duplicating the item
5. link the note, issue, and backlog item together

## Scope Rule

Use the lightest tracking surface that still preserves continuity:

- repo-wide issue map and backlog for portfolio-level recurring review themes
- work-package-local tracking when the issue belongs only to one initiative
- both, when a local issue also teaches a shared portfolio lesson

## Machine-Readable Rule

Do not add a machine-readable recommendation ledger until automation actually
needs it.

Markdown issue maps and backlogs are sufficient until validators, dashboards,
or runtime code depend on structured fields.

## Promotion Rule

Promote a recommendation into standards, templates, skills, docs, or runtime
code when:

- the issue is real and evidenced
- the overlap is understood
- the action is broader than one note
- future work would benefit from a durable canonical surface

## Related Navigation

- [Repo audit control standard](repo-audit-control-standard.md)
- [Machine-readable control surface standard](machine-readable-control-surface-standard.md)
- [Work package standard](work-package-standard.md)
- [Issue map template](../../templates/recommendation-issue-map.md)
- [Backlog template](../../templates/recommendation-backlog.md)
