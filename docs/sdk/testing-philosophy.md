# SDK testing philosophy

Public SDK documentation should make testing expectations clear even when the implementation itself is not published.

## Core expectations

An integration should be tested for:

- valid capability execution;
- invalid parameter rejection;
- unsupported operation handling;
- missing application state;
- host-application failures;
- version compatibility;
- side-effect reporting;
- destructive-operation safeguards.

## Contract tests

For each capability, tests should establish that the documented inputs and outputs match observed behavior.

## Host tests

Where practical, verify the resulting application state rather than only checking that a function returned successfully.

## Regression tests

When a real integration bug is fixed, add coverage that reproduces the failure condition.

## Release confidence

Testing should support a clear public claim such as:

"These capabilities were verified against these application versions under these conditions."

Avoid unsupported universal compatibility claims.
