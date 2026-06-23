# Operator Surface Standard

## Purpose

Define which surfaces are allowed to initiate, approve, route, or display agent
work in a governed repo.

This standard is informed by `hermes-agent`'s explicit distinction between
local surfaces, editor surfaces, network surfaces, and messaging surfaces.

## Core Rule

Every operator surface must be named explicitly.

If a surface can:
- dispatch work
- resolve approvals
- expose output
- trigger scheduled tasks
- or route delegated agents

then it is part of the governed operator model and must be documented.

## Surface Classes

### Local Interactive Surfaces

Examples:
- terminal CLI
- desktop UI
- local TUI
- local browser dashboard bound to loopback

Use when:
- the operator is directly present
- OS-level user access is the main trust boundary

### Editor / IDE Surfaces

Examples:
- Codex
- Claude Code
- Cursor
- ACP or JSON-RPC editor adapters

Use when:
- the repo needs editor-native agent access
- the local user account remains the trust boundary

### Network / Messaging Surfaces

Examples:
- chat integrations
- HTTP APIs
- web dashboards exposed beyond loopback
- bots and messaging adapters

Use only when:
- authorization is explicit
- allowlists or equivalent boundary controls exist
- the repo genuinely needs remote dispatch

### Background Surfaces

Examples:
- scheduler
- dispatcher
- daemon
- queue worker

Use only when:
- the activation rule is explicit
- runtime limits are documented
- output routing is defined
- operator visibility exists

## Authorization Rule

The stronger the surface crosses a trust boundary, the stronger the explicit
authorization requirement must be.

- local-user surfaces rely on OS-level access control
- loopback-only surfaces should stay loopback by default
- network-exposed surfaces require explicit caller authorization

Do not treat a session id, task id, or opaque handle as authorization.

## Output Rule

A surface that can dispatch work should not silently hide the results.

Every operator surface should define:
- where output appears
- where errors appear
- whether it is ephemeral or durable
- who is expected to review it

## Default Bias

Prefer local, visible, operator-present surfaces before remote, background, or
message-driven ones.

Remote or hidden automation must justify itself.
