# Design principles

## Application state is first-class

Creative software has domain state that should be understood directly whenever possible.

## Capability before tool name

The runtime should reason about what needs to be done, while application-specific integration resolves how that capability is expressed in a particular host.

## Intent is not authority

A model may propose an operation. Policy and application state still determine whether it can run.

## Observe after mutation

A successful call does not automatically prove the desired creative result. Important changes should be checked against observed state.

## Long-running work must remain controllable

Progress, cancellation, user input, and approval are product concerns, not debugging extras.

## Local-first by default

Creative work belongs close to the user's applications, files, and project context.

## Provider independence

Application integrations should not need to be redesigned for every model provider.

## Safe failure beats ambiguous success

If the system cannot establish what happened, it should report uncertainty rather than invent completion.

## Public/private separation

Public developer material should explain responsibilities and engineering principles without exposing proprietary production implementation.
