<!-- SPDX-License-Identifier: CC0-1.0 -->

# Documentation Protocol Index

Use this index as the human-facing entry point. The authoritative source is the YAML in `../../specs/`.

## Product Order

1. `protocol_foundation`
2. `governance_and_stewardship`
3. `dsr_lifecycle_and_contribution_model`
4. `information_item_architecture`
5. `repository_architecture`
6. `metadata_and_identifier_profile`
7. `quality_conformance_and_review_model`
8. `artifact_package_specification`
9. `publication_and_registry_model`
10. `service_integration_profile`
11. `templates_and_checklists`
12. `automation_and_validation_model`
13. `implementation_roadmap`

## Minimum Use Path

For a new project, fill `templates/artifact-profile-template.yaml`, select a conformance level, create a package inventory, complete metadata, run the package readiness checklist, then enter review. For a DSR project at L2 or above, also complete the DSR transparency crosswalk, contribution-positioning record, and DSR-specific evaluation-plan fields. For a reusable or publication-ready project, also review the recommended service integration profile, then complete release, preservation, citation, registry, and practitioner-facing communication records where applicable.

Use `orcid-identity.md` to keep author identity consistent across citation, repository, archival, and public profile metadata.

## DSR Transparency Minimum

DSR packages should expose six transparency dimensions: process, problem space, solution space, build, evaluation, and contribution. The protocol asks for enough evidence to support review, reuse, adaptation, and stakeholder confidence while allowing documented limits for privacy, security, intellectual property, proprietary constraints, institutional obligations, maintenance cost, or nonreplicable field interventions.

Evaluation evidence must be separated from demonstration evidence unless acceptance criteria and evidence are defined. Contribution claims should be positioned by artifact type, knowledge scope, knowledge goal, novelty basis, practice contribution, scientific contribution, and transfer conditions.

## Pilot Validation

The first retained pilot is the DSR Framework repository. It validates the protocol only in a bounded sense: downstream pilot application, self-application, and structural-conceptual validation. The current verdict is pass with public-draft/self-application limitations.

This supports coherence, repository usability, source-of-truth discipline, traceability, reviewability, and overclaiming control. In combination with the v1.0.0 L4 readiness review and release records, it supports the package-level L4 reusable-stable release claim. It does not support claims of external adoption, empirical effectiveness, independent external semantic review, or L5 archival/publication-ready status. Use `conformance-declaration.yaml`, `docs/validation/dsr-framework-pilot-validation.md`, `records/validations/record-validation-0001-dsr-framework-pilot.yaml`, and `records/reviews/record-review-l4-readiness-0001-v1-0-0.yaml` for the retained validation boundary.

## Recommended Service Ecosystem

The service integration profile recommends service roles rather than named platforms. Use `docs/protocol/recommended-service-ecosystem.md`, `vocabularies/service-role-vocabulary.yaml`, and `templates/service-integration-profile-template.yaml` to document storage, source control, persistent identifiers, archival deposit, metadata/indexing, dissemination, and communication services. Missing recommended roles are warnings or checklist findings unless another protocol requirement already makes the underlying evidence mandatory.

## Downstream Artifact Licensing Recommendation

Using this protocol does not relicense downstream artifacts. Each artifact package must declare its own license and identify third-party materials and reuse constraints.

For maximum reuse, accessibility, AI indexing/training, adaptation, translation, redistribution, and public benefit, use CC0-1.0 for non-code content and Apache-2.0 or MIT for executable code, with Apache-2.0 preferred when patent clarity is important. Do not make CC0 or Apache-2.0 mandatory for downstream artifacts; document any legal, ethical, institutional, contractual, technical, privacy, funder, export-control, publication, or dependency reason that prevents a highly open license.

## Post-v1 Validation Work

- Identify first public maintainers and governance contact.
- Complete a second internal pilot beyond the DSR Framework pilot.
- Complete a non-DSR pilot or an independent external reviewer pass before claiming stronger external validation or L5 readiness.
- Decide whether active GitHub workflow files should be generated before or after the first pilot.
