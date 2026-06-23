# Scheduled And Delegated Work Standard

## Purpose

Define how governed repos should handle cron-like work, background execution,
and delegated multi-agent tasks.

This standard is informed by `hermes-agent`'s scheduler, profile pinning,
bounded cron execution, and work-queue concepts.

## Core Rule

Scheduled or delegated work is not just "normal chat, later."

It must declare:
- who or what triggers it
- what context it loads
- what runtime it uses
- how long it may run
- where its output lands
- what happens on failure

## Scheduled Work

### Allowed Uses

Good fits:
- bounded audits
- health checks
- lightweight watchdogs
- recurring summaries
- queue dispatch
- no-agent script jobs for simple checks

Poor fits:
- unbounded autonomous exploration
- hidden privileged execution
- silent external mutation with no review lane

### Required Controls

Every scheduled job should define:
- schedule or trigger
- workdir or target scope
- capability set loaded
- timeout or hard interrupt
- output destination
- retry or catchup policy
- whether memory is loaded

### Memory Rule

Do not assume recurring jobs should load the full live memory surface.

Default to a minimal bounded context unless there is a reviewed reason to load
more.

### Serialization Rule

If a job mutates process-global state such as:
- working directory
- active profile
- runtime home
- shared mutable queue state

then that class of job should serialize rather than run in parallel.

## Delegated Work

### When To Delegate

Delegate only when:
- the task can be cleanly scoped
- the child capability set is narrower than the parent's
- the output contract is explicit

Do not delegate simply because "more agents feels stronger."

### Required Delegation Contract

Every delegated task should define:
- owner
- assigned capability or role
- target scope
- expected output
- timeout
- escalation path
- handoff destination

### Queue / Board Rule

If delegated work becomes durable or multi-actor, move it onto an explicit task
surface such as a queue, board, or work register.

Do not rely on ambient chat memory once delegation becomes asynchronous.

## Output Rule

Scheduled and delegated work should not silently blend into the main operator
session.

Its outputs should land in:
- a dedicated run record
- a queue item
- a report artifact
- or another explicit durable surface

## Failure Rule

After repeated failures, background work should block or surface for operator
review rather than looping forever.

If the system can fail repeatedly without attracting attention, it is not
governed enough.
