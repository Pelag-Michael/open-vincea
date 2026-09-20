# Integration authoring guide

This is a developer-facing conceptual guide. It is not a production SDK specification.

## 1. Define the host boundary

Identify:

- target application;
- tested versions;
- supported operating systems;
- available scripting/extension APIs;
- which state is useful to inspect;
- which actions are appropriate to expose.

## 2. Define bounded capabilities

Prefer workflow-oriented actions with clear inputs and outcomes.

Avoid generic unrestricted execution surfaces when a narrower operation can express the real need.

## 3. Preserve application truth

The host application should determine whether an operation succeeded.

Return enough structured information for Vincea to understand what changed.

## 4. Validate inputs

Validate values before handing them to the host application.

Model-produced arguments should be treated as untrusted until checked.

## 5. Design verification

For actions that mutate a project, define how success can be observed afterward.

## 6. Design failure behavior

Document:

- invalid state;
- unsupported versions;
- unavailable dependencies;
- destructive side effects;
- partial completion.

## 7. Test the real host

Unit tests are useful, but professional application integrations also need behavior checks against the host environment.

## 8. Prepare for public release

Complete provenance, licensing, security, privacy, and independence review before source is published.
