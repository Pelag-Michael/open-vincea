# Runtime concepts

Vincea's runtime is built for agent-style work inside stateful creative environments.

## Jobs

A job represents one accepted unit of user work.

A job can move through states such as queued, running, paused, waiting for user involvement, completed, failed, or cancelled.

The public concept matters more than the exact internal state machine: long-running work remains observable and controllable instead of occupying an opaque request.

## Runtime events

Jobs can emit ordered progress events. The desktop experience can use those events to show what phase of work is occurring without exposing private model reasoning.

## Tool loop

The model can perform multiple turns of:

1. inspect context;
2. request an action;
3. receive the actual result;
4. decide whether more work is required.

The loop ends when the task is complete, cancelled, blocked, or reaches a runtime limit.

## Capability surface

The available action surface combines:

- application-specific capabilities;
- global workspace capabilities;
- knowledge and context capabilities;
- visual/media capabilities;
- generative asset capabilities.

The exact surface can vary with the active application and runtime context.

## User checkpoints

Some operations require explicit approval or missing user input. These checkpoints are runtime events, not informal text conventions.

## Verification

The runtime distinguishes "an action was requested" from "the intended result was observed." This distinction is especially important after mutations to a scene, document, file, or project.
