# Tool contract concepts

A tool contract is the public concept of describing what an application action accepts and what it returns.

This document does not define production schemas or serialization.

## Conceptual contract

A useful tool description answers:

- What does this action do?
- What inputs are required?
- What inputs are optional?
- What values are valid?
- What application state is required?
- What side effects can occur?
- What does success look like?
- What failure categories are expected?

## Illustrative example

```text
Capability: rename_selected_item

Inputs
  name: non-empty string

Precondition
  one supported item is selected

Side effect
  selected item name changes

Result
  status
  summary
  affected_items
```

The example is intentionally descriptive and does not represent a production schema.

## Why contracts help

Clear contracts make validation, testing, documentation, and safe failure easier.
