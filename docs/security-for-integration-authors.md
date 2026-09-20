# Security for integration authors

Application integrations can receive model-produced actions and can modify valuable professional work. Their design should assume that model output may be incorrect, malformed, or overly broad.

## Minimize authority

Expose the smallest practical set of operations.

## Validate all inputs

Validate names, identifiers, paths, numeric ranges, enumerations, and object types before execution.

## Handle file operations carefully

For integrations that read or write files:

- document allowed locations or restrictions;
- avoid accidental overwrite;
- report the final target;
- make destructive behavior explicit;
- prefer user-controlled destinations where appropriate.

## Avoid unnecessary network exposure

If the host integration only needs local communication, do not expose it broadly without a documented reason.

## Protect secrets

Do not store credentials in public repositories, example files, screenshots, logs, or test fixtures.

## Treat logs as data

Logs can contain project names, file paths, user content, and application state. Review them before publication.

## Make failure visible

Silent failure can be dangerous in professional workflows. Return clear failure information and indicate whether state may have changed.

## Backups and version control

For workflows with meaningful side effects, recommend appropriate backup, version-control, or application-native recovery practices.
