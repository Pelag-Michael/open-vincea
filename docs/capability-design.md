# Capability design

A capability is a bounded unit of application functionality that an integration intentionally makes available.

## Good capability characteristics

A capability should be:

- **specific** enough that its purpose is obvious;
- **bounded** so it cannot silently expand into unrelated authority;
- **validatable** before application execution;
- **documented** with expected side effects;
- **observable** through a meaningful result.

## Prefer intent-oriented capabilities

Prefer a capability that reflects a real user action over a generic escape hatch.

Good examples:

- create a supported scene object;
- rename a selected item;
- read the current frame range;
- export a supported document format.

Avoid capabilities that effectively mean "run arbitrary host code" unless the entire purpose of the integration explicitly requires that level of authority and the risk is clearly documented.

## Inputs

Inputs should have explicit meaning, narrow types, and known validation rules.

Useful constraints include:

- required vs optional fields;
- allowed ranges;
- supported enumerations;
- host-application object identifiers;
- expected units;
- file-path restrictions when relevant.

## Side effects

Every capability should make its side effects understandable. If it can overwrite, delete, export, save, or permanently modify application state, say so.

## Results

Return enough information for the user and the next interaction to understand what happened.

A useful result often includes:

- outcome status;
- affected object or document;
- warnings;
- error category when unsuccessful;
- small amounts of relevant output.

The public repository intentionally does not define production capability schemas.
