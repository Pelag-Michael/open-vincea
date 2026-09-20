# Error model

A useful integration should fail in ways that are understandable to both users and software.

## Recommended public error categories

### Invalid input

The request is understood, but one or more parameters are not acceptable.

### Unsupported operation

The requested action is not exposed by the integration.

### Missing application state

The request depends on state that is absent, such as no selected object or no active document.

### Application rejected operation

The integration attempted a valid host action, but the application rejected it.

### Compatibility issue

The installed application version or environment does not support the requested behavior.

### Permission or access issue

The operation requires access that is unavailable.

### Execution failure

An unexpected application-side failure occurred.

## Error response guidance

A useful error should answer:

1. What failed?
2. Why, if known?
3. Was anything changed?
4. Can the user recover?
5. Is retrying reasonable?

## Partial work

If an operation changes application state before later failing, the result should make that partial state explicit.

The public error model is intentionally descriptive rather than a production wire-format specification.
