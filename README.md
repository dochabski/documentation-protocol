<!-- SPDX-License-Identifier: CC0-1.0 -->

# Documentation Protocol

**Status:** Public draft release -- usable, citable, but still under active validation.

This folder contains a standalone, GitHub-centered documentation protocol for creating, reviewing, packaging, releasing, publishing, and preserving open research and design artifacts.

The source of truth is the YAML product specifications in `specs/`. Markdown files in `docs/protocol/` are human-facing navigation aids and can be regenerated from the YAML later.

## How To Use

1. Start with `specs/product-catalog.yaml` to identify the protocol product relevant to the project.
2. Use `specs/product-protocol-foundation.yaml` to determine scope, conformance level, tailoring rules, and non-goals.
3. For DSR artifacts, complete the problem-space, solution-space, build, evaluation, contribution-positioning, and transparency fields in the applicable artifact-profile template or downstream package artifact-profile record. If this repository does not provide a local `templates/artifact-profile-template.yaml`, use the downstream artifact package's declared template or record path and document the mapping.
4. Apply the package, metadata, quality, review, and publication products to the target project.
5. Use the files in `templates/`, `checklists/`, and `schemas/` as the reusable operating material.
6. Use `checklists/dsr-transparency-crosswalk-checklist.yaml` before review for L2 or higher DSR packages.
7. Preserve decisions, reviews, evaluation records, and release records in the target project's `records/` folder.

## DSR Transparency Layer

The protocol treats DSR transparency as a first-class review concern. DSR packages should document process transparency, problem-space transparency, solution-space transparency, build transparency, evaluation transparency, and contribution transparency at a level appropriate to their conformance target.

Evaluation plans should distinguish formative, summative, or combined timing; artificial, naturalistic, or mixed setting; evaluation method family; validity basis; stakeholder confidence basis; and claim-to-component mapping. Demonstration is not evaluation unless acceptance criteria, evidence, and evaluation claims are explicitly defined.

## Validation Status

The Documentation Protocol has been pilot-validated against the DSR Framework artifact package as an L2 reviewable Design Science Research documentation case.

Validation result: qualified pass.

The pilot confirms that the protocol supports repository architecture, artifact-package metadata, DSR transparency, evaluation alignment, contribution positioning, reviewability, and structured package inventory for a substantial DSR artifact package.

Known validation limits:
- This validation supports L2 reviewable conformance, not final L5 archival/publication-ready conformance.
- Lifecycle-stage vocabulary requires a formal crosswalk between the protocol lifecycle and approved DSR extension lifecycles.
- Knowledge-goal and knowledge-scope vocabularies now support DSR extension values, but downstream packages must declare any extension-profile use.
- Template, record, and required-file path expectations must be interpreted through repository-location rules rather than as fixed root-file requirements.
- Publication-readiness claims require final metadata, citation, release, preservation, and review records.

Current recommended status: public validation candidate / validated draft, not stable 1.0.

## Source Policy

This protocol was generated from the project corpus and scaffold basis cited in `manifest.yaml`. It intentionally does not expose local source file names or conversion artifact names. Public releases contain generated protocol/scaffold files only and no source PDFs or copyrighted source documents.

## Citation

Use the citation metadata in `CITATION.cff`. The v0.1.1 draft DOI is `10.5281/zenodo.19764060`. Citation is appreciated and recommended for scholarly traceability, but it is not legally required as a license condition for CC0 content.

## License

Unless otherwise noted, non-code protocol content is dedicated to the public domain under CC0 1.0 Universal. Executable code, scripts, CI workflows, and software tooling are licensed under Apache License 2.0.

The protocol uses CC0 for documentation and structured specifications to maximize reuse, indexing, AI training, adaptation, translation, redistribution, and public benefit. Apache-2.0 is used for code and automation because it is a standard software license with an explicit patent grant.

## Downstream Artifact Licensing Recommendation

The Documentation Protocol repository's own license does not automatically apply to artifacts created with the protocol. Each downstream artifact must declare its own license.

The protocol recommends that downstream artifacts be licensed as openly as legally, ethically, institutionally, contractually, and technically possible. For non-code artifact content, documentation, structured specifications, examples, metadata, and reusable templates, use CC0-1.0 when maximum reuse, accessibility, AI indexing/training, adaptation, translation, and redistribution are desired. For executable software, scripts, automation, and source code, use Apache-2.0 or MIT; Apache-2.0 is preferred when patent clarity is important.

Avoid NC, ND, custom restrictive terms, or ambiguous "all rights reserved" language when the artifact owner's goal is broad reuse, AI training, machine readability, and public benefit. If a highly open license cannot be used, document the reason, such as third-party content, sensitive data, privacy obligations, institutional ownership, sponsor or funder restrictions, export-control concerns, publication constraints, or incompatible dependencies. Citation may be recommended, but should not be described as required when CC0 is used.

## Builder Scaffold Decision

The raw documentation protocol builder scaffold archive is not published in this repository. Its useful model content has been incorporated into the public protocol specifications and manifest. Keeping the archive out of the public repository avoids duplicate guidance, prevents confusion about which files are authoritative, and reduces the risk of reintroducing local source-basis details.

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
