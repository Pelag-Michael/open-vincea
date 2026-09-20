# Application integration release checklist

Use this checklist before publishing an integration in `addons/`.

## Scope

- [ ] Target application is clearly identified.
- [ ] Integration can stand on its own as public material.
- [ ] No dependency on non-public Vincea components is required for understanding the published source.

## Documentation

- [ ] Purpose is documented.
- [ ] Installation steps are documented.
- [ ] Supported application versions are documented.
- [ ] Limitations are documented.
- [ ] Side effects are documented.
- [ ] Security implications are documented.

## Source hygiene

- [ ] No credentials or secrets.
- [ ] No private URLs.
- [ ] No machine-specific absolute paths.
- [ ] No unnecessary logs.
- [ ] No caches or generated artifacts.
- [ ] No user project data.
- [ ] No private research notes.

## Provenance and licensing

- [ ] Source provenance is known.
- [ ] Upstream attribution is preserved.
- [ ] License compatibility is verified.
- [ ] Copyright history is not rewritten inaccurately.
- [ ] Vincea attribution is present where appropriate.

## Safety

- [ ] Inputs are validated.
- [ ] Destructive operations are documented.
- [ ] Failure behavior is understandable.
- [ ] File operations are reviewed for overwrite or path risks.
- [ ] Network behavior is documented if present.

## Final review

- [ ] Public repository content does not expose proprietary production implementation details.
- [ ] README links are correct.
- [ ] Integration documentation matches tested behavior.
