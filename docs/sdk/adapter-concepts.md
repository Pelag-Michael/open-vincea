# Adapter concepts

An adapter is the public concept of a component that translates a Vincea capability into behavior supported by a particular host application.

## Responsibilities

An adapter should know:

- what application it targets;
- which capabilities it supports;
- how to validate application-specific inputs;
- how to call the host application's extension surface;
- how to convert host results into understandable outcomes.

## Conceptual shape

```text
Application Adapter
  describe capabilities
  validate request
  execute supported action
  observe result
```

This is explanatory notation only.

## Keep the host boundary narrow

The adapter should not own model-provider logic, cross-application product policy, or unrelated product state.

## Prefer application semantics

A useful adapter exposes meaningful application operations and inspection rather than forcing every workflow through generic screen coordinates.
