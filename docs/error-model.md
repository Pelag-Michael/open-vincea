# Error model

Creative automation needs errors that explain both **what failed** and **what may have changed**.

## Useful public categories

### Invalid input

The capability is known, but one or more values are not acceptable.

### Unsupported operation

The active integration does not expose the requested behavior.

### Missing application state

The operation depends on state that is absent, such as a selection or active document.

### Application rejection

The request reached the host application, but the host could not complete it.

### Compatibility issue

The behavior is unavailable in the current application version or environment.

### Permission or approval required

The operation cannot proceed until the user grants access or confirms the action.

### Execution failure

The integration encountered an unexpected runtime problem.

### Cancelled or interrupted

The user or runtime stopped work before normal completion.

## Good error responses

A good error should answer:

1. What failed?
2. Why, if known?
3. Did anything change?
4. Can the user recover?
5. Is retrying appropriate?

Partial work should never be silently presented as complete.
