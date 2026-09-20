# Security model

Vincea's public security model focuses on minimizing unnecessary authority and making application side effects understandable.

## Core principles

### Narrow capability exposure

An integration should expose only the application operations needed for its intended use.

### Input validation

Application actions should validate supported operations and parameters before execution.

### Clear side effects

Documentation should identify operations that can change projects, documents, scenes, files, or other persistent application state.

### Local-first interfaces where appropriate

When a target application supports a local interface and remote exposure is unnecessary, keeping that interface local can reduce avoidable network exposure.

### Provider awareness

External AI provider data handling depends on the provider and user configuration. Users and organizations should review those terms for their own requirements.

### Recovery

Important professional work should use backups, version control, or application-native recovery features where appropriate.

This repository documents public principles rather than private production security implementation.
