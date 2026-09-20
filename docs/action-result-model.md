# Action and result model

Vincea integrations benefit from a predictable separation between an **action request** and an **execution result**.

## Action request

Conceptually, an action request communicates:

- the requested operation;
- the target application scope;
- validated parameters;
- optional user-visible intent context.

Illustrative example:

```text
Action
  operation: "rename_selected_item"
  parameters:
    name: "Hero Camera"
```

This is explanatory notation only, not a production serialization format.

## Execution result

A result should communicate what actually happened.

```text
Result
  status: success
  summary: "Renamed selected item"
  affected_items: 1
```

For failures:

```text
Result
  status: failure
  category: invalid_input
  summary: "No supported item is selected"
```

## Why separate them?

The distinction helps avoid confusing model intent with application reality.

The model can request an action, but only the integration can report whether the host application accepted it and what changed.

## Recommended result qualities

Results should be:

- concise;
- structured enough for follow-up reasoning;
- explicit about partial or failed work;
- careful not to expose sensitive host data unnecessarily.
