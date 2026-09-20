# Compatibility philosophy

Creative applications, operating systems, and provider APIs evolve independently. Vincea treats compatibility as an explicit engineering responsibility.

## Per-application support

Each public integration should identify the application versions it was actually tested against.

## Different host mechanisms

Different applications may use different extension technologies. That is expected.

Public compatibility should describe user-visible behavior rather than pretending every host has the same implementation shape.

## Graceful degradation

When a capability is unavailable in a specific environment, the integration should expose a smaller honest surface or fail clearly.

## Cross-platform behavior

Shared behavior should remain conceptually consistent across operating systems while platform-specific application integration details stay isolated.

## Compatibility claims

Use language such as:

- tested;
- experimental;
- partial;
- unavailable in this edition/version.

Avoid universal claims without evidence.
