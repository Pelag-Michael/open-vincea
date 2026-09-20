# Product overview

Vincea is a local-first AI operator for professional creative software.

The core product idea is simple: a user should be able to describe creative work in natural language while the AI understands enough of the active application's real state to perform useful work inside it.

## Why this is different from generic computer use

Creative applications contain domain structure that pixels alone do not explain:

- scene graphs and 3D objects;
- materials, cameras, modifiers, and animation;
- layers and document objects;
- timelines and clips;
- CAD entities;
- project assets and render settings.

Vincea therefore prefers application-aware integrations that can inspect and manipulate domain state directly.

Screen-based interaction remains useful as a fallback for tasks that are not exposed through a deeper application integration.

## Local-first model

The creative workflow is designed to run on the user's machine. Project context, sessions, application interaction, and locally created assets are part of that local working environment.

Calls to external AI or media providers depend on the provider chosen by the user.

## Multi-step work

Vincea is designed for tasks that may require:

- understanding current application state;
- planning a sequence of actions;
- performing one or more operations;
- asking the user for approval or missing input;
- checking the result;
- continuing from the observed state.

This is why the product is structured around sessions and jobs instead of only single-turn chat responses.
