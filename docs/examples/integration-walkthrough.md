# Example integration walkthrough

This example illustrates the public integration model without publishing executable Vincea integration code.

## Goal

Support renaming the currently selected item in a creative application.

## 1. Define the capability

```text
rename selected item
```

## 2. Define the precondition

Exactly one supported item must be selected.

## 3. Define the input

```text
new name: non-empty text
```

## 4. Validate

Reject the request when:

- no document is active;
- the selection is missing;
- the selected item cannot be renamed;
- the requested name violates host constraints.

## 5. Execute

Use the application's supported extension or scripting mechanism.

## 6. Observe

Read the item back from the application after the operation.

## 7. Report

Return whether the operation succeeded, what changed, and any warning.

The important pattern is **intent → validation → host action → observed result**, not a particular wire format.
