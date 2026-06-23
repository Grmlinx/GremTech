# gremlin-git Read Only Assessment

## Purpose

Record what a read-only pass over `gremlin-git` says about the user's tool
preferences and what should be standardized from that estate.

## Snapshot

Observed top-level structure:
- `Python-Projects`
- `python-scripts`
- `Powershell-scripts`
- `_old`
- `dist`

Observed file-volume signal:
- `Python-Projects`: 8083 files
- `python-scripts`: 74 files
- `Powershell-scripts`: 17 files
- `_old`: 13 files

There is no obvious root `README.md` front door.

## Dominant Tool Themes

The estate is heavily centered on:
- CSV and Excel manipulation
- PDF splitting, parsing, OCR, and optimization
- ZIP and directory listing workflows
- M365 and O365 collection or reporting
- document ID, hyperlinking, and evidence-processing utilities
- network parsing and scan post-processing

## What This Suggests About Tool Preferences

### Strong Operator Pragmatism

The estate prioritizes:
- getting a job done quickly
- direct path-based input
- concrete output artifacts like CSV, XLSX, or processed files

### Windows-First Reality

There is a strong Windows and PowerShell bias, even when Python is used.
Packaging into executable form is also a recurring pattern.

### File And Folder First

Many tools assume one of:
- a dropped file
- an entered path
- a batch folder

This is a strong signal for the CLI model.

### Interactive Prompting Is Acceptable

Many scripts use `input(...)` or interactive PowerShell messaging instead of
strict argument-only interfaces.

This suggests the user tolerates:
- guided prompting
- operational conversational flow

as long as the task stays practical.

### Progress And Feedback Matter

The PowerShell scripts frequently use:
- `Write-Host`
- `Write-Progress`

This suggests the tools should keep operators informed during longer work.

### Evolutionary Tooling Path

The estate shows a recurring progression:
- one-off script
- better script
- packaged executable
- larger project when value persists

That is a useful promotion model for `GremTech`.

## Example Signals

- `python-scripts/csv-splitter.py`
  - extremely direct CSV utility with prompt-driven input
- `Powershell-scripts/advanced-robocopy.ps1`
  - practical operations automation with progress visibility
- `Python-Projects/Find-Doc-ids/Doc-id-finder-Final.py`
  - more mature packaged desktop-style tool with hardened parsing and GUI
- `Python-Projects/PDF-tools/from-doofus.py`
  - evidence that `Doofus` is already acting as a curation path for some
    promoted utilities

## Risks In The Current Estate

- support status is not obvious
- maturity varies widely
- packaging artifacts and source are mixed together
- archival versus active tools are not clearly separated
- there is no single product boundary

## Standardization Implication

`gremlin-git` should not be treated as a product to expand blindly.

It should be treated as:
- a script-garden evidence base
- a quarry for promotion candidates
- a source of operator-pattern truth for CLI standards

## Recommended Next Moves

1. Build a governed tool catalog for `gremlin-git`.
2. Mark tools as supported, incubating, or archived.
3. Promote the strongest repeated workflows into curated operator-tool repos.
4. Use `Doofus` as the first modern CLI baseline for that promotion path.
