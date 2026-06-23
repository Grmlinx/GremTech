# Repo Onboarding Standard

## Purpose

Define how a repo joins the agency operating model.

Onboarding does not mean cloning the same folder tree everywhere.
It means making the repo governable, reviewable, and maintainable.

## Minimum Onboarding Outputs

Every governed repo should have:

1. A human entrypoint
   - usually `README.md`
2. An AI entrypoint
   - `start.ai`
3. An identified repo archetype
4. An explicit control surface
   - `governance/` or equivalent operating-rules location
5. A chosen memory pattern
6. A documentation front door
   - `docs/README.md` or equivalent
7. Repeatable operational guidance when execution exists
   - `runbooks/` or equivalent
8. A place for decisions, backlog, or future commitments
9. A `GremTech` portfolio profile
10. Machine-readable control surfaces when the repo depends on validation,
    routing, or support-state clarity
   - for example a documentation-sync contract, support-state catalog, or
     repo-surface manifest

## Onboarding Sequence

1. Classify the repo archetype.
2. Document what already works and should be preserved.
3. Add only the missing mandatory surfaces.
4. Capture the repo profile in `portfolio/profiles/`.
5. Record the adoption gaps in the playbook.
6. Reuse templates instead of inventing one-off scaffolding.

## What Not To Do

- do not force the `alfred` memory model onto every repo
- do not create governance directories with no clear purpose
- do not turn a human note vault into a bureaucratic software platform
- do not standardize by deleting useful repo-specific behavior

## Success Criteria

A repo is successfully onboarded when:

- a new human can orient safely
- an AI assistant has a clear startup contract
- current truth is findable
- durable changes can be reviewed and proven
- support boundaries are explicit when the repo exposes meaningful capability
- future changes can reuse established templates
