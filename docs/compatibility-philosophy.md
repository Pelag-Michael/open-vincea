# Compatibility philosophy

Professional creative applications evolve quickly. Integrations should treat compatibility as an explicit engineering concern.

## Supported versions

Each public integration should state the application versions it is known to support.

Avoid vague claims such as "works everywhere."

## Capability differences

When host versions expose different functionality, document the difference instead of pretending the behavior is identical.

## Graceful degradation

If a feature is unavailable in an older or restricted environment, the integration should fail clearly or expose a narrower capability set.

## Compatibility matrix

A public integration may maintain a table such as:

| Application version | Core actions | File operations | Notes |
| --- | --- | --- | --- |
| Version A | Supported | Supported | Baseline |
| Version B | Supported | Limited | One API difference |

Actual values should come from tested integration behavior.

## Environment assumptions

Document dependencies that materially affect operation, such as:

- application edition;
- required extension APIs;
- supported operating systems;
- required plugin state;
- optional external tools.

Compatibility claims should reflect tested reality.
