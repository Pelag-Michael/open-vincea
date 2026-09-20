# Action validation example

Illustrative pseudocode:

```text
receive action request

if capability is unavailable:
    return unsupported

if required input is invalid:
    return invalid_input

if application preconditions are not met:
    return missing_state

if user approval is required:
    pause for approval

perform host operation

observe resulting application state

return structured outcome
```

## Why validation matters

A model can produce a plausible operation that is wrong for the current application state.

Validation separates:

- what the model wants;
- what Vincea currently exposes;
- what the user has approved;
- what the host application can actually do;
- what the application ultimately reports.
