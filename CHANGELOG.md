<!-- SPDX-License-Identifier: CC0-1.0 -->

# Changelog

## [Unreleased]

## [1.0.1] - 2026-05-09

### Added

- Added a bookmark example consistency review record for the v1.0.1 patch release.
- Added v1.0.1 release and release approval records.

### Changed

- Normalized the David Ochabski bookmark-derived service profile with a stable profile ID, current version metadata, service IDs, public identifiers, and evidence-note fields.
- Renamed the service candidate catalog to `examples/service-profiles/service-candidate-catalog.yaml` and normalized its root key, metadata, service names, service types, and public-safe fields.
- Updated package metadata, citation metadata, specs, and package-control files for the v1.0.1 patch release.

## [1.0.0] - 2026-05-08

### Added

- Added `conformance-declaration.yaml` for the package-level L4 reusable-stable claim.
- Added package-control files: `artifact-profile.yaml`, `package-inventory.yaml`, `traceability-matrix.yaml`, `evaluation-report.yaml`, and `LIMITATIONS.md`.
- Added L4 readiness review and v1.0.0 release approval records.

### Changed

- Stabilized the Documentation Protocol as `v1.0.0` with package conformance `L4 reusable-stable`.
- Clarified that L5 archival/publication-ready status is not claimed.
- Reinterpreted the DSR Framework pilot as L4-supporting evidence when paired with the v1.0.0 readiness and release records.
- Updated repository metadata, citation metadata, and human-facing documentation for the v1.0.0 release.

## [0.1.2] - 2026-05-08

### Added

- Added DSR transparency as a first-class protocol layer covering process, problem space, solution space, build, evaluation, and contribution transparency.
- Added `checklists/dsr-transparency-crosswalk-checklist.yaml`.
- Added `templates/contribution-positioning-record-template.yaml`.
- Added retained DSR Framework pilot validation evidence in `records/validations/record-validation-0001-dsr-framework-pilot.yaml`.
- Added `crosswalks/documentation-protocol-to-dsr-framework-pilot.yaml`.
- Added `docs/validation/dsr-framework-pilot-validation.md`.
- Added `checklists/pilot-learning-checklist.yaml`.
- Added `records/roadmap/record-next-validation-tier-0001.yaml`.
- Added a vendor-neutral Recommended Service Integration Profile product with service-role vocabulary, profile and record templates, readiness checklist, schema, human-facing documentation, candidate catalog, Codex handoff prompt, and a non-normative David Ochabski example profile.
- Added expanded v0.2 service candidates covering Google Scholar, arXiv, Octopus, Dryad, Peer Community In, HAL, bioRxiv, medRxiv, data.org, FORCE11, SCOSS, Crossref, and ROR.
- Added `records/releases/record-release-0001-v0-1-2.yaml`.
- Added DSR-specific artifact profile fields for stakeholders, problem space, solution space, context constraints, kernel theories, existing artifacts, build process, alternatives, design decisions, contribution positioning, transfer conditions, and transparency evidence.
- Added DSR-specific evaluation-plan fields for formative/summative timing, artificial/naturalistic setting, method family, validity basis, stakeholder confidence basis, and claim-to-component mapping.

### Changed

- Strengthened package readiness and review checks to catch the common DSR failure mode of treating demonstration as evaluation.
- Updated the implementation roadmap to treat the DSR Framework as a bounded self-application pilot and to require additional non-self-application evidence before stronger validation claims.
- Integrated service integration profile guidance as nonblocking, vendor-neutral recommendations rather than named-service conformance requirements.
- Expanded manifest citations for DSR transparency, evaluation strategy, and contribution positioning.

## [0.1.1] - 2026-04-25

### Changed

- Changed repository licensing model from the superseded CC-BY-4.0 v0.1.0 model to CC0-1.0 for non-code protocol content.
- Added Apache-2.0 for executable code, scripts, CI workflows, and software tooling.
- Clarified that citation is appreciated and recommended but not required.
- Added `LICENSES/` directory with full CC0-1.0 and Apache-2.0 license texts.
- Added downstream artifact licensing recommendations that encourage maximally open licensing without relicensing downstream artifacts.

## [0.1.0] - 2026-04-24

### Added

- Draft standalone documentation protocol package.
- Twelve protocol product specifications in `specs/`.
- Reusable templates, checklists, JSON schemas, and protocol index.
- Manifest documenting citation-based source basis and scaffold rationale.

### Pending

- Initial maintainer and governance contact assignment.
- First pilot artifact selection.
- Optional generated Markdown renders from YAML source.
