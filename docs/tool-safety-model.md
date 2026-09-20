# Tool safety model

Vincea's safety model starts from a simple rule:

> Model-generated intent is not equivalent to permission to execute.

## Bounded capability surface

The model can only request capabilities intentionally exposed by the active runtime context.

## Runtime policy

Before execution, the runtime can apply policy based on the operation, the application context, the route, and the current job/session.

## Human approval

Higher-risk operations can stop at an approval checkpoint before continuing.

Approval is treated as scoped runtime state rather than as a vague assumption that a user "probably agreed."

## Destructive file recovery

File-changing workflows should preserve a recovery path where practical before destructive modification.

## Application verification

After important mutations, the runtime can inspect structured or visual state to determine whether the requested outcome was actually achieved.

## Failure discipline

Blocked or ambiguous work should remain explicit. The system should not turn a failed operation into a successful-sounding final answer.

This document describes the public safety model, not Vincea's private authorization implementation.
