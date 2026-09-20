# Testing strategy

Testing a professional-application integration is not only about checking the happy path. It should also establish that failures are predictable and side effects are controlled.

## Test layers

### Contract-level tests

Confirm that supported operations accept valid inputs and reject malformed or unsupported inputs.

### Application behavior tests

Verify that operations produce the expected application state.

### Compatibility tests

Check supported application versions and document version-specific limitations.

### Failure-path tests

Exercise cases such as:

- missing selection;
- closed or invalid document;
- inaccessible file;
- unsupported object type;
- application-side rejection;
- unavailable dependency.

### Destructive-operation tests

For save, overwrite, delete, replace, or batch-modification behavior, verify warnings and recovery expectations.

### Result-quality tests

Ensure integrations report enough information to understand what changed.

## Determinism

Where host behavior allows it, keep test fixtures small and repeatable.

## What public tests should demonstrate

Public test material should demonstrate engineering expectations without exposing non-public implementation details.

## Release gate

An integration should not be published merely because it works on one machine once. Compatibility, provenance, security, and repeatable behavior all matter.
