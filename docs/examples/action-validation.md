# Action validation example

This example shows the reasoning pattern for validating an application action before execution.

It is intentionally pseudocode.

```text
receive proposed action

if operation is not supported:
    return unsupported_operation

if required input is missing:
    return invalid_input

if current application state does not satisfy preconditions:
    return missing_application_state

if parameters violate application constraints:
    return invalid_input

perform supported host operation

return structured result
```

## Why this pattern matters

Model output can be syntactically plausible while still being inappropriate for the current application state.

Validation separates:

- what the model wants to do;
- what the integration supports;
- what the host application can actually do right now.

The result should always describe the observed outcome rather than assuming success.
