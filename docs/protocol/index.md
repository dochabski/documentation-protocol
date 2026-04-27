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
10. `templates_and_checklists`
11. `automation_and_validation_model`
12. `implementation_roadmap`

## Minimum Use Path

For a new project, fill `templates/artifact-profile-template.yaml`, select a conformance level, create a package inventory, complete metadata, run the package readiness checklist, then enter review. For a DSR project at L2 or above, also complete the DSR transparency crosswalk, contribution-positioning record, and DSR-specific evaluation-plan fields. For a publication-ready project, also complete release, preservation, citation, registry, and practitioner-facing communication records where applicable.

## DSR Transparency Minimum

DSR packages should expose six transparency dimensions: process, problem space, solution space, build, evaluation, and contribution. The protocol asks for enough evidence to support review, reuse, adaptation, and stakeholder confidence while allowing documented limits for privacy, security, intellectual property, proprietary constraints, institutional obligations, maintenance cost, or nonreplicable field interventions.

Evaluation evidence must be separated from demonstration evidence unless acceptance criteria and evidence are defined. Contribution claims should be positioned by artifact type, knowledge scope, knowledge goal, novelty basis, practice contribution, scientific contribution, and transfer conditions.

## Downstream Artifact Licensing Recommendation

Using this protocol does not relicense downstream artifacts. Each artifact package must declare its own license and identify third-party materials and reuse constraints.

For maximum reuse, accessibility, AI indexing/training, adaptation, translation, redistribution, and public benefit, use CC0-1.0 for non-code content and Apache-2.0 or MIT for executable code, with Apache-2.0 preferred when patent clarity is important. Do not make CC0 or Apache-2.0 mandatory for downstream artifacts; document any legal, ethical, institutional, contractual, technical, privacy, funder, export-control, publication, or dependency reason that prevents a highly open license.

## Current Draft Open Questions

- Identify first public maintainers and governance contact.
- Select one software or executable pilot and one non-software DSR pilot.
- Decide whether active GitHub workflow files should be generated before or after the first pilot.
