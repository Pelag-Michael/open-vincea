# Integration authoring guide

This guide describes how to think about a Vincea-compatible application integration at a public, developer-facing level.

It is not an executable SDK specification.

## Step 1: define the application boundary

Identify:

- the target application;
- supported versions;
- what application state is safe and useful to read;
- what actions are appropriate to expose;
- what actions should remain unavailable.

## Step 2: design capabilities

Each capability should map to a clear application responsibility.

Document:

- purpose;
- inputs;
- expected output;
- side effects;
- known limitations;
- compatibility assumptions.

See [capability-design.md](capability-design.md).

## Step 3: validate inputs

Validate before calling the host application.

Do not assume model-produced parameters are automatically safe or correct.

## Step 4: perform the host operation

Use the application's supported integration mechanisms and follow its own extension or scripting guidance.

## Step 5: return a meaningful result

A result should help both the user and subsequent AI reasoning understand what actually happened.

See [action-result-model.md](action-result-model.md).

## Step 6: test failure behavior

Test malformed inputs, unsupported state, application-version differences, and destructive operations.

## Step 7: document installation and security

Public integrations should clearly explain:

- installation;
- required permissions;
- network behavior if any;
- data handling implications;
- destructive operations;
- recovery recommendations.

## Step 8: complete release audit

Before publication, review provenance, licensing, private data, logs, credentials, local paths, and independence from non-public components.
