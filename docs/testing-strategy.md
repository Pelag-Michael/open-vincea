# Testing strategy

The private Vincea implementation contains a broad regression surface around runtime behavior, session lifecycle, application interaction, vision, provider formatting, job control, safety, and integration contracts.

The public lesson is more important than any one test count: agentic creative software needs tests at several boundaries.

## Runtime tests

Cover:

- job creation and terminal states;
- pause/resume/cancel behavior;
- approval and user-input checkpoints;
- recovery after interruption;
- session isolation;
- tool outcome normalization.

## Provider-format tests

The same capability description may need different schema or message translation for different model providers.

Changes to the shared capability surface should therefore be checked across provider adapters.

## Application integration tests

Cover:

- input validation;
- application state inspection;
- mutation behavior;
- error handling;
- version differences;
- structured result shape.

## Vision and media tests

Visual workflows need coverage for:

- image references;
- session continuity;
- screenshot or image result handling;
- large/binary output hygiene.

## Safety regression tests

High-risk behavior should have explicit regression coverage around approval, session boundaries, destructive operations, and execution ownership.

## Reality check

The existence of tests does not mean every application integration has identical maturity, nor does it mean every development snapshot is globally green. Public compatibility claims should be based on targeted verified evidence.
