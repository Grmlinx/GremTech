# CLI Tool Standard

## Purpose

Define the standard model for command-line and operator-tool products in the
portfolio.

This is especially relevant to repos like `Doofus` and to scripts promoted out
of `gremlin-git`.

## Core Rule

A good CLI in this portfolio should be:
- human-first
- composable
- file and folder aware
- safe by default
- explicit about outcomes

## Product Shape

Choose one of these intentionally:

### Single-Purpose Utility

Use when:
- the task is narrow
- the operator need is obvious
- promotion into a larger tool would add more ceremony than value

### Multi-Command Operator Tool

Use when:
- the tasks share a domain
- consistent I/O and help surfaces matter
- common packaging, release, and settings behavior is worth standardizing

This is the preferred promotion target for the best `gremlin-git` utilities.

## Interaction Model

### Human-First But Scriptable

The CLI should accept flags and arguments normally.

For operator-first tools, it may also prompt interactively when required input
is missing.

Do not force prompt-only interaction when the tool should also compose cleanly
in scripts.

### Discovery

Every substantive command should provide:
- `--help`
- concise default help when run incorrectly
- one or more examples
- clear subcommand naming

### Input Modes

Prefer explicit support for:
- single file
- folder per-file processing
- folder combined processing

These patterns are strongly present in both `Doofus` and `gremlin-git`.

### Output Behavior

The tool should:
- make output paths explicit
- avoid hidden in-place mutation by default
- support machine-readable output where practical
- provide logs and operator messaging without polluting machine output

### Safety

For risky actions:
- require explicit confirmation or flags
- support dry-run where feasible
- explain what will happen before it happens

## UX Rules For CLI

The CLI should:
- use familiar verbs and nouns
- speak the operator's language
- show progress for long-running tasks
- explain errors in operational language
- return zero exit code on success and non-zero on failure
- separate primary output from diagnostics

## Packaging Rule

Windows-first packaging is acceptable and often desirable in this portfolio.

Acceptable surfaces include:
- source install
- packaged executable
- release ZIP
- install and uninstall helper scripts

But packaging should not replace:
- help text
- documentation
- repeatable build logic

## Promotion Rule From Script Garden To Product

Promote a `gremlin-git` style script into a governed tool when it has:
- repeated operator value
- a clear domain boundary
- stable enough inputs and outputs
- worthiness for docs, packaging, and QA

Do not promote every useful one-off into a product.

## Signals From Existing Repos

Observed operator preferences in the portfolio include:
- Windows-first practicality
- direct file and folder operations
- CSV, Excel, PDF, ZIP, and reporting workflows
- optional interactive prompting for missing inputs
- visible progress and concrete output artifacts
- pragmatic packaging into EXE or release bundles when it helps operators

## Non-Goals

Do not force every CLI to become:
- a daemon
- a web app
- a plugin ecosystem
- a full-screen terminal UI

Keep the tool proportional to the job.
