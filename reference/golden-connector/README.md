# Golden Connector Package - Reference Template

Every connector package in this repository follows the layout shown here. Copy
this folder when starting a new connector and adapt the contents.

## Documentation files

`overview.md`
: Required. Must be non-empty and written in English only. Describe the source
  system, the object model and the data volume that the connector handles.

`usage.md`
: Required. Must be non-empty and written in English only. Explain setup,
  required credentials and a minimal end-to-end example.

`notes.md`
: Optional. Free-form engineering notes, known limitations, rollout caveats.

## Configuration and tooling

`manifest.json`
: Optional. Machine-readable package metadata (id, display_name, tier,
  schedule). Packages without it fall back to platform defaults at build time.

`contract_check.py`
: Optional helper. Some teams use it to exercise the connector contract on a
  developer workstation. It is not required by the build pipeline; include it
  only if the maintainer finds it useful.

`fixtures/`
: Optional folder with sample payloads used during local testing.

## Checklist

- [ ] overview.md is non-empty and English only
- [ ] usage.md is non-empty and English only
- [ ] every statement above that is not marked Optional is satisfied
