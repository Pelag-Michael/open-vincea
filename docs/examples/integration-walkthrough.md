# Example integration walkthrough

This walkthrough illustrates how a developer might reason about a small application integration without publishing an executable Vincea implementation.

## Goal

Suppose an application integration wants to support renaming the currently selected item.

## 1. Define the capability

Name the operation clearly:

```text
rename_selected_item
```

## 2. Define the input

The action needs one input:

```text
name: non-empty string
```

## 3. Define the precondition

Exactly one supported item must be selected.

## 4. Define the side effect

The selected item's name changes in the host application.

## 5. Validate before execution

Reject:

- empty names;
- unsupported selections;
- requests with no active document;
- values the host application cannot accept.

## 6. Execute through the host application

Use the application's supported extension or scripting mechanism.

## 7. Report the result

A successful result might state:

```text
status: success
summary: "Renamed selected item"
affected_items: 1
```

A failure should explain why the operation did not run and whether application state changed.

## What this example demonstrates

Even a small integration benefits from explicit capability scope, preconditions, validation, side-effect documentation, and structured results.
