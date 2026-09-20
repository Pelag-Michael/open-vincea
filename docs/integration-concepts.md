# Integration concepts

Vincea is most useful when it can interact with a creative application through that application's own extension or scripting surface.

## Integration responsibilities

A good application integration should provide:

- application identity;
- readable application context;
- bounded actions;
- structured results;
- compatibility information;
- safe failure behavior.

## Direct application understanding

Where possible, Vincea should work with domain objects instead of only pixels.

Examples include:

- scene objects and materials;
- document layers and selections;
- timeline clips;
- CAD entities;
- render or export state.

## Thin host bridge, rich runtime semantics

Application-side code should stay focused on interacting with the host application.

Higher-level reasoning, user interaction, safety policy, and cross-cutting runtime behavior belong outside the host application whenever practical.

## Screen-based fallback

Some workflows do not expose a sufficient application API. Screen interaction can provide a fallback, but it carries different reliability and safety characteristics and should not be confused with deep application integration.

## Integration maturity

Having an integration directory or prototype does not prove equal depth across applications. Public support claims should reflect tested reality.
