# Tool safety model

AI-generated application actions should not be treated as automatically trustworthy.

Vincea's public safety model is based on a simple principle: a requested action should be checked against the capability surface that the application integration intentionally exposes before execution.

## Developer-facing principles

- Expose only actions that are necessary for the integration's purpose.
- Validate action names and parameters.
- Reject malformed or unsupported requests.
- Make destructive or high-impact behavior explicit in documentation.
- Return clear success and failure information.
- Keep application permissions as narrow as practical.
- Avoid silently broadening capability scope.

## User-facing principles

Users should understand that integrations can change real application state. Important projects should be backed up or version controlled where appropriate, and users should review the permissions and limitations documented by each integration.

This document describes public safety principles only.
