# Design principles

Vincea is designed for AI-assisted work inside professional creative applications, where context, user intent, and real application state all matter.

## 1. Application-aware, not chat-only

A useful assistant should understand that a creative application has its own objects, documents, scenes, timelines, selections, and constraints. Vincea treats application context as part of the working environment rather than as incidental text.

## 2. Explicit capability boundaries

An integration should expose a bounded set of actions. The model should not receive arbitrary authority over the host application.

## 3. Validate before acting

Model output is a proposal for an application action, not an automatic command. Parameters and supported operations should be checked before execution.

## 4. Preserve user agency

Users should be able to understand what the system is doing, what changed, and where failures occurred.

## 5. Provider independence

Application integrations should remain focused on application behavior rather than on one model vendor.

## 6. Continuity without opacity

Long-running creative work benefits from session continuity and memory, but integrations should still return clear, inspectable results.

## 7. Safe failure

Unsupported or malformed operations should fail clearly rather than produce ambiguous or partially applied behavior.

## 8. Public/private separation

Public integration material should be useful on its own without exposing proprietary production implementation details.
