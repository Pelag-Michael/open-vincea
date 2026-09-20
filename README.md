# Vincea

Vincea is an AI interaction layer for professional creative applications. It is designed to help AI understand application context, work with user intent, and perform approved actions inside professional workflows.

## About this repository

This repository contains public technical documentation, selected application integrations, engineering notes, and developer-facing material for Vincea.

It is **not** a full source distribution of Vincea.

Selected integrations and public technical material may be released here after provenance, licensing, security, and privacy review. Vincea uses proprietary runtime, distribution, activation, and production infrastructure that are outside the scope of this repository.

## High-level architecture

```text
User
  ↓
Vincea
  ↓
AI Runtime
  ↓
Tool Authority
  ↓
Application Integration
  ↓
Creative Application
```

The public architecture documentation intentionally stays at a system-concept level. It explains responsibilities and safety boundaries without exposing production implementation details.

## Public material

This repository may include:

- architecture and runtime concepts at a high level;
- tool safety and application-action guidance;
- session, memory, and provider-abstraction concepts;
- integration guidance for application developers;
- selected, independently auditable application integrations.

## Application integrations

Public integrations are reviewed independently before release. Each published integration should document its target application, purpose, installation steps, limitations, security implications, provenance, and licensing.

Third-party notices and copyright history must be preserved. A Vincea attribution does not replace upstream attribution.

## Safety

Application integrations can modify professional projects, documents, scenes, or other user data. Use backups or version control where appropriate, review permissions carefully, and understand the data-handling terms of any external AI provider you configure.

See [SECURITY.md](SECURITY.md) and [docs/security-model.md](docs/security-model.md).

## Documentation

- [Architecture overview](docs/architecture-overview.md)
- [Runtime concepts](docs/runtime-concepts.md)
- [Tool safety model](docs/tool-safety-model.md)
- [Sessions and memory](docs/sessions-and-memory.md)
- [Provider abstraction](docs/provider-abstraction.md)
- [Integration concepts](docs/integration-concepts.md)
- [Security model](docs/security-model.md)

## Project attribution

**Vincea**

Originally created and developed by **Michael Vo — Pelago**

GitHub: https://github.com/Pelag-Michael
