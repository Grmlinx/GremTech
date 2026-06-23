# Config And Secrets Boundary

## Purpose

Define how governed repos should separate normal configuration from secrets and
sensitive credentials.

This standard is informed by `hermes-agent`'s explicit split between config
files and secret-bearing environment variables.

## Core Rule

Secrets belong in secret-bearing surfaces.
Normal settings belong in normal configuration.

Do not mix them casually.

## Secrets

Secrets include:
- API keys
- tokens
- passwords
- private credentials
- signing secrets
- client secrets

Store these in:
- environment variables
- secret managers
- untracked local secret files
- approved credential stores

Do not store them in:
- tracked config files
- repo docs
- example files as real values
- working context notes

## Normal Configuration

Normal configuration includes:
- thresholds
- timeouts
- model choices
- feature flags
- paths
- display preferences
- non-sensitive integration settings

These belong in:
- tracked config schema
- documented settings files
- startup contracts
- repo-owned standards or templates where appropriate

## Bridging Rule

If older code expects an environment variable for a non-secret setting,
bridge it deliberately from the canonical config source.

Do not let compatibility bridges become the new source of truth.

## Multi-Surface Rule

If a repo has multiple execution surfaces such as:
- CLI
- web UI
- background worker
- gateway
- scheduled automation

then config loading must be reviewed across all of them.

If one surface sees a setting and another does not, the config model is not
done.

## Example Rule

Tracked example files may show:
- placeholder names
- expected variable names
- documented shapes

They must not contain:
- live secrets
- copied production values
- misleading pseudo-real credentials

## Review Rule

Every new config surface should answer:
- what is the canonical config source
- where do secrets live
- how do other runtime surfaces read it
- what compatibility bridges exist

If those answers are unclear, the config change is incomplete.
