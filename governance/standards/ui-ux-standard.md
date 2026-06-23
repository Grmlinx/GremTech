# UI UX Standard

## Purpose

Define the default quality bar for user-facing interfaces in the portfolio.

This applies to:
- web UI
- desktop UI
- local TUI
- rich REPL surfaces
- setup and approval flows that behave like interfaces

## Core Rule

UI is not decoration.
It is an operator control surface.

The standard should optimize for:
- clarity
- accessibility
- safe operation
- fast comprehension
- low cognitive load

## Normative Baselines

### Accessibility

Use:
- WCAG 2.2 AA as the default accessibility baseline for UI-bearing products

This should influence:
- keyboard access
- contrast
- focus order and visibility
- labels and instructions
- error messaging
- responsive behavior

### Usability Heuristics

Use established usability heuristics as review gates.

Minimum recurring checks:
- visibility of system status
- match between the system and the real world
- user control and freedom
- consistency and standards
- error prevention
- recognition over recall
- flexibility and efficiency
- minimalist design
- useful error recovery
- help and documentation

### Interaction Psychology

Use Laws of UX as inspiration, not as a substitute for accessibility or
testing.

The most relevant recurring laws here are:
- Hick's Law
- Jakob's Law
- Fitts's Law
- Tesler's Law
- Doherty Threshold
- Peak-End Rule
- Law of Proximity
- Law of Similarity

## Product Rules

### Operator Tools

For operator-facing tools:
- prefer obvious controls over novelty
- bias toward dense clarity rather than marketing polish
- make destructive actions explicit
- show progress and outcome state clearly
- keep instructions close to the action

### Administrative Or Governance Surfaces

For approval, review, or governance UI:
- show current state clearly
- show what action is being approved
- show scope and risk before action
- make undo, cancel, or abort paths obvious when possible

### Multi-Step Flows

For setup or execution flows:
- reduce decision count per step
- keep the user oriented on where they are
- expose progress and next steps
- avoid forcing memory of previous hidden decisions

## Anti-Patterns

Do not:
- use visual novelty to hide weak information architecture
- treat accessibility as optional polish
- force users to memorize system state
- hide critical actions behind vague labels
- create UI that looks sophisticated but weakens operator confidence

## Review Rule

If a task materially changes a user-facing surface, the `ui-engineer` lane
should review it against:
- WCAG expectations
- usability heuristics
- operator workflow clarity

## Repo Archetype Rule

Not every repo needs a heavy UI standard.

Use the full UI review depth only when the repo actually exposes a meaningful
interactive surface.
