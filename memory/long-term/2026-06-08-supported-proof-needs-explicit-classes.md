# Supported Proof Needs Explicit Classes

## Lesson

Serious repos should not treat all proof as one undifferentiated green state.

## Why It Matters

Structural validation, synthetic smoke, supported operator proof,
environment-bound proof, and compatibility proof answer different questions.
When they are flattened together, release posture becomes easier to misread.

## Reuse Rule

Future Alfred-class builds should:

1. classify proof paths explicitly
2. state where each path runs
3. say which paths are release-required
4. keep CI truth and supported-proof truth clearly separated

## Promotion Targets

- `governance/standards/proof-path-classification-standard.md`
- `docs/alfred-read-only-recommendations-pass-03.md`
