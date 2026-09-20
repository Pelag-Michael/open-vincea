# Security for integration authors

Application integrations sit close to valuable user work.

## Treat model output as untrusted input

Validate operation names, identifiers, paths, numeric ranges, and object types.

## Keep authority narrow

Prefer explicit host operations over a broad escape hatch.

## Make destructive behavior obvious

Saving, overwriting, deleting, batch-editing, exporting, and replacing assets should be documented.

## Preserve a recovery story

Where practical, support backups, snapshots, undo, version control, or application-native recovery.

## Keep network exposure deliberate

Do not expose an application integration broadly when a local-only interface is sufficient.

## Review logs and fixtures

Logs can contain project names, paths, user content, screenshots, or application state.

## Fail visibly

If the integration cannot determine whether an operation succeeded, return an ambiguous/failure state rather than reporting success.
