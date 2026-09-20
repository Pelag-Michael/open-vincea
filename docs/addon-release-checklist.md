# Application integration release checklist

Use this before publishing source under `addons/`.

## Scope

- [ ] Target application is identified.
- [ ] Tested application versions are recorded.
- [ ] Public source can stand independently from proprietary Vincea components.

## Documentation

- [ ] Purpose is documented.
- [ ] Installation is documented.
- [ ] Capability scope is documented.
- [ ] Limitations are documented.
- [ ] Side effects are documented.
- [ ] Security implications are documented.

## Source hygiene

- [ ] No credentials or secrets.
- [ ] No private URLs.
- [ ] No machine-specific absolute paths.
- [ ] No user project data.
- [ ] No unnecessary logs or test artifacts.
- [ ] No proprietary product configuration.

## Provenance

- [ ] Origin of every significant component is known.
- [ ] Upstream attribution is preserved.
- [ ] License compatibility is verified.
- [ ] Copyright history remains accurate.
- [ ] Vincea attribution is present where appropriate.

## Engineering

- [ ] Inputs are validated.
- [ ] Failure behavior is clear.
- [ ] Destructive operations are documented.
- [ ] Compatibility claims match tested evidence.
- [ ] Result reporting is sufficient to understand what changed.
