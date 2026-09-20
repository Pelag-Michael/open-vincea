# Tool contract concepts

A public tool contract describes the meaning of a capability without exposing Vincea's production schema.

A useful contract answers:

- What does this capability do?
- What inputs are required?
- What application state must exist?
- Does it mutate state?
- What risks or approvals may apply?
- How can success be observed?
- What failure categories are expected?

## Example

```text
Capability
  rename selected item

Precondition
  one supported item is selected

Input
  new name

Side effect
  selected item changes

Verification
  inspect selected item name
```

This is conceptual documentation, not a serialization format.
