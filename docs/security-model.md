# Security model

Vincea is powerful because it can affect real creative work. The public security model therefore focuses on constraining and observing authority rather than pretending the environment has no risk.

## Capability minimization

Only expose operations needed for the workflow.

## Validation

Check model-produced inputs before host execution.

## User checkpoints

Require explicit user involvement where the operation carries meaningful risk or needs clarification.

## Session and job isolation

Runtime work should remain bound to the intended session and application context.

## Recovery

Destructive workflows should preserve a practical recovery path where possible.

## Verification

Important mutations should be followed by application-appropriate checks.

## Secret separation

Credentials should stay out of model prompts, public logs, examples, and repositories.

## Local-first posture

Application execution and project context are designed to remain on the user's machine, while external provider data handling depends on the provider the user chooses.

This document does not describe private production security algorithms.
