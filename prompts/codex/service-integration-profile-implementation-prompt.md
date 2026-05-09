<!-- SPDX-License-Identifier: CC0-1.0 -->

# Codex Implementation Prompt: Recommended Service Integration Profile

Repository: `dochabski/documentation-protocol`

## Task

Implement a vendor-neutral Recommended Service Integration Profile. The profile should recommend service roles and evidence patterns, not require named platforms. David's services should appear only as a non-normative example profile.

## Branch

Create or use:

```text
feature/service-integration-profile
```

This is an implementation branch only. Do not create a permanent branch for David's service choices.

## Read first

```text
README.md
specs/product-catalog.yaml
specs/product-protocol-foundation.yaml
specs/product-repository-architecture.yaml
specs/product-metadata-and-identifier-profile.yaml
specs/product-publication-and-registry-model.yaml
specs/product-automation-and-validation-model.yaml
specs/product-templates-and-checklists.yaml
checklists/release-publication-checklist.yaml
templates/artifact-profile-template.yaml
```

## Add supplied files

Copy these supplied files into matching repository paths:

```text
specs/product-service-integration-profile.yaml
vocabularies/service-role-vocabulary.yaml
templates/service-integration-profile-template.yaml
templates/service-integration-record-template.yaml
checklists/service-integration-readiness-checklist.yaml
schemas/service-integration-profile.schema.json
docs/protocol/recommended-service-ecosystem.md
examples/service-profiles/david-ochabski-service-profile.yaml
prompts/codex/service-integration-profile-implementation-prompt.md
```

## Patch existing files

### `specs/product-catalog.yaml`

Add after `publication_and_registry_model`:

```yaml
  - id: service_integration_profile
    title: Recommended Service Integration Profile
    purpose: Define nonblocking, vendor-neutral service roles and candidate service examples for storage, source control, persistent identification, archival deposit, metadata indexing, educational dissemination, public communication, and long-form publication.
    depends_on: [protocol_foundation, repository_architecture, metadata_and_identifier_profile, publication_and_registry_model]
    source_basis: [md_guides, data_and_information, protocol_project_decision]
    product_file: specs/product-service-integration-profile.yaml
```

Also add `service_integration_profile` as a dependency of `templates_and_checklists`, `automation_and_validation_model`, and `implementation_roadmap` if their dependency lists enumerate all upstream products.

### `README.md`

Add:

```markdown
## Recommended Service Ecosystem

The protocol includes a nonblocking Recommended Service Integration Profile. It recommends service roles for working storage, source control, persistent identifiers, archival deposit, metadata/indexing, educational dissemination, public communication, and long-form publication. Named platforms are examples, not conformance requirements. User-specific service choices should be captured in service profile YAML files, not long-lived Git branches.
```

Add `service_integration_profile` to the Product Set.

### `specs/product-protocol-foundation.yaml`

Add to assumptions:

```yaml
        - Recommended service integrations are role-based; named third-party platforms are examples rather than conformance requirements.
```

Add to `should`:

```yaml
        - Projects should complete a recommended service integration profile when preparing reusable or publication-ready artifact packages.
```

Add to `must_not`:

```yaml
        - Projects must not require a named third-party service when an equivalent role-satisfying service or documented substitute is available.
```

Add `service_integration_profile` to downstream outputs where product lists are maintained.

### `specs/product-metadata-and-identifier-profile.yaml`

Add a recommended field:

```yaml
        - id: service_integration_profile
          type: uri_or_path
          required: recommended_for_l4_l5
```

Add to `should`:

```yaml
        - Metadata should link to the service integration profile when service roles support citation, preservation, registry submission, dissemination, or public communication.
```

### `specs/product-publication-and-registry-model.yaml`

Add to publication readiness guidance:

```yaml
        - Publication-ready packages should review the service integration profile to confirm repository, archive, citation, registry, project-wrapper, and communication links are consistent with release metadata.
```

Add `service_integration_record` as an optional or recommended record, not a universal blocking requirement.

### `specs/product-automation-and-validation-model.yaml`

Add a validation layer:

```yaml
        - id: service_integration_validation
          checks: [service_role_profile_present_where_expected, no_named_service_required, no_secrets_or_tokens, github_not_sole_archive_for_l5, service_links_match_release_metadata]
```

Add this severity rule:

```yaml
        - Missing recommended service roles should be warnings, not release-blocking failures, unless another protocol product already requires the underlying evidence.
```

### `specs/product-templates-and-checklists.yaml`

Reference:

```text
templates/service-integration-profile-template.yaml
templates/service-integration-record-template.yaml
checklists/service-integration-readiness-checklist.yaml
```

Recommend for L4/L5 or publication/registry/dissemination use; do not require for every level.

### `checklists/release-publication-checklist.yaml`

Add:

```yaml
    - id: service-integration-reviewed
      question: Has the service integration profile been reviewed for repository, archive, citation, registry, project-wrapper, dissemination, and communication links where applicable?
      evidence_required: [service-integration-profile.yaml, service-integration-record.yaml]
```

### `templates/artifact-profile-template.yaml`

Add near metadata/repository fields:

```yaml
  service_integration:
    service_integration_profile_path: ""
    service_integration_record_ids: []
    highly_recommended_roles_reviewed: false
    named_services_required_for_conformance: false
    substitutions_or_omissions_documented: false
```

## Validation

Run existing validation if present. Otherwise run:

```bash
python -m json.tool schemas/service-integration-profile.schema.json > /tmp/service-schema.json
python - <<'PY'
from pathlib import Path
for p in [
    'specs/product-service-integration-profile.yaml',
    'vocabularies/service-role-vocabulary.yaml',
    'templates/service-integration-profile-template.yaml',
    'templates/service-integration-record-template.yaml',
    'checklists/service-integration-readiness-checklist.yaml',
    'examples/service-profiles/david-ochabski-service-profile.yaml',
]:
    text = Path(p).read_text(encoding='utf-8')
    assert '\t' not in text, f'tab found in {p}'
print('basic checks passed')
PY
```

If PyYAML is available, parse all added YAML files.

## Acceptance criteria

- New product appears in product catalog and README Product Set.
- New product spec, vocabulary, template, record template, checklist, schema, docs, and David example profile exist.
- Named services are examples only.
- Missing recommended service roles are warnings or advisory unless the underlying evidence is already required elsewhere.
- No secrets, tokens, private URLs, or credentials are included.
- David's service profile is explicitly `non_normative_example`.
