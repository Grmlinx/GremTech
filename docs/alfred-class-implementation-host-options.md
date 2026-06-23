# Alfred-Class Implementation Host Options

## Purpose

Compare the realistic places where the first generic Alfred-class core could be
implemented.

## Option 1: Build It Inside GremTech

Pros:

- governance standards already live here
- templates and work-package model already live here
- no new repo setup required

Cons:

- mixes governance/orchestration and runtime-product concerns
- risks turning the portfolio control repo into the product repo
- makes it harder to keep `GremTech` generic and reusable

Verdict:

- possible
- not preferred for the long term

## Option 2: Build It Inside Doofus

Pros:

- active rollout target
- already a tool product

Cons:

- wrong archetype
- would distort a lightweight operator-tool repo into a heavy governed platform
- would compete with the current Doofus baseline adoption effort

Verdict:

- not recommended

## Option 3: Build It Inside home-lab

Pros:

- already has operational rigor

Cons:

- wrong problem domain
- infra repo should not become the host for a generic Alfred-class platform
- already in a similar development cycle elsewhere

Verdict:

- not recommended

## Option 4: Build It Inside Gremoire

Pros:

- none that justify it

Cons:

- completely wrong archetype
- would damage the human-first vault model

Verdict:

- reject

## Option 5: Create A New Dedicated Platform Repo

Pros:

- clean separation between governance/orchestration and runtime product
- generic core can be built without inheriting the baggage of another repo
- optional domain packs can be added later from a stable base
- easiest place to prove an Alfred-class core honestly

Cons:

- requires explicit repo creation and initial setup
- one more managed repo in the portfolio

Verdict:

- recommended

## Recommendation

If the goal is to genuinely recreate an Alfred-class governed AI product
platform, the cleanest path is:

1. keep `GremTech` as the standards and orchestration layer
2. create a new dedicated implementation repo for the generic runtime core
3. add optional domain packs later instead of forcing them into the core first

## Non-Recommendation

Do not treat `Doofus` as the Alfred-class core host.

It should stay on the lightweight operator-tool baseline path.
