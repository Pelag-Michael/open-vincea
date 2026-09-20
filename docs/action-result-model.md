# Action and result model

Vincea treats **requested action** and **observed result** as different objects conceptually.

## Requested action

A requested action expresses what the model wants to attempt:

```text
Capability
  rename the selected item

Input
  desired name = "Hero Camera"
```

This notation is illustrative only.

## Observed result

The integration reports what the application actually did:

```text
Outcome
  status = success
  summary = selected item renamed
  affected items = 1
```

A failed operation should instead describe the failure and whether any state changed.

## Why the separation matters

Model reasoning can be wrong, stale, incomplete, or based on missing application state.

The application integration is the source of truth for the execution outcome.

## Structured outcomes

Useful outcomes can include:

- success/failure;
- human-readable summary;
- affected scope;
- retryability;
- verification information;
- structured application data.

Public documentation intentionally omits the production serialization format.
