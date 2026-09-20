# Adapter concepts

An adapter is the developer-facing concept that translates between Vincea-style application actions and the host application's own extension surface.

This document is explanatory only.

## Conceptual responsibilities

An adapter should know:

- what application it targets;
- which capabilities it supports;
- how to validate capability parameters;
- how to perform supported host operations;
- how to report results.

## Illustrative interface

```text
ApplicationAdapter
  describe_capabilities()
  validate(action)
  execute(action)
  report(result)
```

This is pseudocode for discussion, not a production interface.

## Keep host behavior local

Application-specific assumptions should remain inside the integration layer rather than leaking into unrelated higher-level logic.

## Avoid generic escape hatches

A strong adapter exposes meaningful application operations rather than one unrestricted execution function.

## Results matter

The adapter should report application reality: success, failure, warnings, and affected scope.
