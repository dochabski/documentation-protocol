<!-- SPDX-License-Identifier: CC0-1.0 -->

# DSR Framework Pilot Validation

**Status:** Public draft/self-application validation evidence.

The DSR Framework repository is the first retained downstream pilot for the Documentation Protocol. The validation target is the Documentation Protocol. The validation vehicle is the DSR Framework repository. The validation type is downstream pilot application, self-application, and structural-conceptual validation.

## Validation Claim

The DSR Framework repository functions as the first substantive pilot artifact for validating the Documentation Protocol's ability to guide, structure, review, and release a complex DSR artifact package. This validation supports protocol coherence, structural adequacy, repository usability, source-of-truth discipline, traceability, and reviewability.

This validation does not prove external adoption, empirical effectiveness, independent semantic adequacy, or publication-ready/L5 status. It also does not validate downstream artifacts automatically merely because they use the Documentation Protocol.

## Evidence Inspected

The pilot review inspected the DSR Framework repository at commit `080b634acd256d5be87baf7bb9533d89d1a1c1c7`, release `v1.2.0`, and the Documentation Protocol repository at commit `80aec1aab1f1317e258fbce12e02419bbe9b6ca1`, release `v0.1.1`.

The pilot evidence includes the DSR Framework root control files, `manifest.yaml`, `metadata.yaml`, `artifact-profile.yaml`, `package-inventory.yaml`, `conformance-declaration.yaml`, product specifications, models, vocabularies, templates, checklists, schemas, protocol documentation, records, crosswalks, examples, and validation automation.

## Results

| Validation question | Result | Evidence basis |
|---|---|---|
| Can the protocol generate a coherent repository architecture? | Pass | DSR Framework root files, manifest, package inventory, conformance declaration, and canonical directories |
| Can the protocol distinguish source-of-truth YAML from explanatory Markdown? | Pass | Structured YAML control files plus human-facing `README.md` and `docs/protocol/` |
| Can the protocol support DSR transparency dimensions? | Pass with limitations | DSR transparency records, templates, checklists, and documentation |
| Can it preserve decision, review, evaluation, and release evidence? | Pass | Retained records for design decisions, contribution positioning, evaluation, reviews, releases, and preservation |
| Can it prevent overclaiming? | Pass | L4-not-L5 conformance boundary, limitations, release records, and preservation status |
| Can another user follow it without local context? | Pass with limitations | README, templates, checklists, schemas, examples, and validation automation; external user review not yet completed |

## Limitations

- The pilot is a self-application case, not independent external validation.
- The pilot is a single repository case.
- The DSR Framework is DSR-specific and contains richer DSR operationalization than the general Documentation Protocol should contain.
- The pilot does not provide empirical evidence that the protocol improves downstream outcomes.
- The pilot does not prove adoption, maintainability under independent users, or L5 archival/publication-ready closure.

## Disposition

The pilot is retained as public draft validation evidence. The current verdict is `pass_with_public_draft_self_application_limitations`.

The Documentation Protocol should remain a public draft release: usable, citable, but still under active validation. This pilot can support movement toward a future `v0.2.0` validated draft after additional pilot evidence and independent review are retained.

## Next Validation Tier

The next validation work should move beyond self-application. Preferred next steps are a second internal pilot outside the DSR Framework, a non-DSR artifact pilot, an independent external reviewer pass, a time-bounded re-instantiation test, and only later an L5 readiness review after preservation, registry, and external review closure.

## Related Records

- `records/validations/record-validation-0001-dsr-framework-pilot.yaml`
- `crosswalks/documentation-protocol-to-dsr-framework-pilot.yaml`
- `checklists/pilot-learning-checklist.yaml`
- `records/roadmap/record-next-validation-tier-0001.yaml`
