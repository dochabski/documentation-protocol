# Documentation Protocol

**Status:** Public draft release -- usable, citable, but still under active validation.

This folder contains a standalone, GitHub-centered documentation protocol for creating, reviewing, packaging, releasing, publishing, and preserving open research and design artifacts.

The source of truth is the YAML product specifications in `specs/`. Markdown files in `docs/protocol/` are human-facing navigation aids and can be regenerated from the YAML later.

## How To Use

1. Start with `specs/product-catalog.yaml` to identify the protocol product relevant to the project.
2. Use `specs/product-protocol-foundation.yaml` to determine scope, conformance level, tailoring rules, and non-goals.
3. Apply the package, metadata, quality, review, and publication products to the target project.
4. Use the files in `templates/`, `checklists/`, and `schemas/` as the reusable operating material.
5. Preserve decisions, reviews, evaluation records, and release records in the target project's `records/` folder.

## Source Policy

This protocol was generated from the project corpus and scaffold basis cited in `manifest.yaml`. It intentionally does not expose local source file names or conversion artifact names. The v0.1.0 release contains generated protocol/scaffold files only and no source PDFs or copyrighted source documents.

## Citation

Use the citation metadata in `CITATION.cff`. The v0.1.0 draft DOI is `10.5281/zenodo.19748824`.

## License

This protocol is licensed under Creative Commons Attribution 4.0 International (`CC-BY-4.0`).

## Product Set

- `protocol_foundation`
- `governance_and_stewardship`
- `dsr_lifecycle_and_contribution_model`
- `information_item_architecture`
- `repository_architecture`
- `metadata_and_identifier_profile`
- `quality_conformance_and_review_model`
- `artifact_package_specification`
- `publication_and_registry_model`
- `templates_and_checklists`
- `automation_and_validation_model`
- `implementation_roadmap`
