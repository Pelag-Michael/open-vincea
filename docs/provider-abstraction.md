# Provider abstraction

Vincea is designed so the creative application layer does not depend on a single AI provider.

## Why this matters

Different users may care about:

- model capability;
- latency;
- context length;
- cost;
- privacy terms;
- organizational policy;
- local vs hosted execution.

The runtime therefore treats provider/model execution as a separate responsibility from application integration.

## Provider-facing responsibilities

At a public level, the provider layer is responsible for:

- submitting model input;
- translating available capabilities into the provider's supported tool format;
- returning model text and action requests;
- preserving provider-appropriate conversation context;
- reporting usage and failure information.

## Application independence

A Blender operation should still be a Blender operation whether the reasoning model comes from one provider or another.

This repository does not publish private authentication, token-storage, or provider-specific production internals.
