# Capability design

A capability is a bounded operation that Vincea can reason about independently of a specific provider.

Examples at a public level include:

- inspect workspace state;
- inspect selected entities;
- execute a supported application action;
- capture visual state;
- verify a change;
- read or modify workspace files;
- create or inspect generated media.

## Properties of a good capability

A capability should be:

- **purposeful** — it maps to a real workflow need;
- **bounded** — it does not silently grant unrelated authority;
- **validatable** — its inputs can be checked before execution;
- **observable** — the result can be inspected;
- **documented** — side effects and limitations are understandable.

## Application-specific resolution

Different applications can satisfy the same high-level intent through different APIs or extension mechanisms.

The public model therefore separates the capability from the concrete host operation.

## Mutations and verification

Capabilities that change state should make it possible to verify the resulting state.

That may mean structured application inspection, visual inspection, or another application-appropriate check.

This repository does not publish Vincea's production capability schemas.
