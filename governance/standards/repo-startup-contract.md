# Repo Startup Contract

## Purpose

Define the minimum contract every governed repo should expose to an AI
assistant.

## Required File

Use `start.ai` at the repo root.

## Required Sections

Every `start.ai` should state:

- the repo purpose
- the operating principles
- the required read order
- the control model, if execution or deployment exists
- the memory model or current-truth surfaces
- expected change behavior
- a session close rule
- a definition of done

## Style Rule

`start.ai` should be:
- explicit
- operational
- repo-specific
- short enough to read at session start

It should not be:
- a marketing page
- a vague values statement
- a hidden replacement for real docs and runbooks

## Portfolio Rule

`README.md` is the human-facing front door.
`start.ai` is the AI-facing front door.

Both are required for governed repos unless the archetype is intentionally
human-only and the repo profile records that exception.
