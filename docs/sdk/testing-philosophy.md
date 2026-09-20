# SDK testing philosophy

A public integration contract is only useful when its observable behavior can be tested.

## Contract tests

Confirm that documented capabilities accept valid inputs and reject invalid inputs.

## Host behavior tests

Verify application state after execution, not only a successful return value.

## Failure tests

Cover missing selections, closed documents, incompatible versions, permission problems, and host-side rejection.

## Mutation tests

For operations that change state, verify both the intended result and failure recovery expectations.

## Compatibility tests

Record which application versions and environments were actually exercised.

## Regression tests

When a real integration bug is fixed, keep a test that reproduces the previous failure condition.
