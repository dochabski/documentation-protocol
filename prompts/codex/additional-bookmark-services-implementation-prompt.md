# Codex handoff: add expanded service candidates from the new bookmark set

You are updating `dochabski/documentation-protocol`.

## Goal

Add the second service-candidate set to the Documentation Protocol's Recommended Service Integration Profile. This update adds Google Scholar, arXiv, Octopus, Dryad, Peer Community In, HAL, bioRxiv, medRxiv, data.org Funding Opportunities, FORCE11, SCOSS, Crossref, and ROR as **candidate examples** under vendor-neutral service roles.

Do **not** make any named service, membership, dashboard, or personal account mandatory for protocol conformance.

## Branch

Use:

```bash
git switch main
git pull --ff-only
git switch -c feature/service-integration-profile-bookmarks-v2
```

If a service-integration branch already exists locally, inspect it first. Do not discard work. If the first service-profile package was never committed, use the files in this package as the combined base + v2 implementation.

## Files to add or replace

Copy everything under `files-to-add-or-replace/` into the repository root, preserving paths:

```text
specs/product-service-integration-profile.yaml
vocabularies/service-role-vocabulary.yaml
templates/service-integration-profile-template.yaml
templates/service-integration-record-template.yaml
checklists/service-integration-readiness-checklist.yaml
schemas/service-integration-profile.schema.json
docs/protocol/recommended-service-ecosystem.md
examples/service-profiles/david-ochabski-service-profile.yaml
examples/service-profiles/service-candidate-catalog-v0-2.yaml
```

If these files already exist, merge carefully or replace with the v0.2 files after confirming no unrelated local changes would be lost.

## Existing files to patch

Patch these files if present:

1. `README.md`
   - Add `service_integration_profile` to Product Set.
   - Add one short sentence under How To Use or publication guidance: service profiles are recommended for L4/L5 service-role planning and are advisory unless an underlying evidence record is required elsewhere.

2. `specs/product-catalog.yaml`
   - Add a product entry for `service_integration_profile` using the YAML in `patches/repository-patch-snippets.yaml`.

3. `specs/product-protocol-foundation.yaml`
   - Add `service_integration_profile` to downstream outputs.
   - In assumptions or normative `should`, add: projects should consider recommended service roles while retaining freedom to use equivalent services.

4. `specs/product-metadata-and-identifier-profile.yaml`
   - Mention DataCite, Crossref, ROR, ORCID, OpenAlex, Google Scholar, CITATION.cff, and codemeta.json as examples of identifier/indexing interoperability.
   - Preserve the rule that ORCID is recommended, not universally required.

5. `specs/product-publication-and-registry-model.yaml`
   - Add `service_integration_profile` as an upstream dependency or related output.
   - Add service integration profile/review checklist as publication-readiness evidence for L4/L5 only.

6. `specs/product-automation-and-validation-model.yaml`
   - Add validation checks for service profile syntax and secret-like values.
   - Add warning behavior for missing recommended roles.
   - Add error behavior if a named service is encoded as required.

7. `specs/product-templates-and-checklists.yaml`
   - Add the service integration profile template, record template, and checklist to reusable material.

8. `checklists/release-publication-checklist.yaml`
   - Add the checklist entry from `patches/repository-patch-snippets.yaml`.

9. `templates/artifact-profile-template.yaml`
   - Add a lightweight `service_integration_profile` field pointing to the applicable profile path/status.

## Validation commands

Run:

```bash
python - <<'PY'
from pathlib import Path
import json
import yaml
for path in Path('.').rglob('*.yaml'):
    if '.git' in path.parts:
        continue
    try:
        yaml.safe_load(path.read_text(encoding='utf-8'))
    except Exception as e:
        raise SystemExit(f'YAML parse failed: {path}: {e}')
for path in Path('.').rglob('*.json'):
    if '.git' in path.parts:
        continue
    try:
        json.loads(path.read_text(encoding='utf-8'))
    except Exception as e:
        raise SystemExit(f'JSON parse failed: {path}: {e}')
print('syntax validation passed')
PY
```

Also run any existing repository validation, lint, or tests if present.

## Acceptance criteria

- `service_integration_profile` appears in product catalog and README product set.
- All v0.2 service candidate examples are present in the vocabulary or example catalog.
- `david-ochabski-service-profile.yaml` includes the new bookmarks as non-normative examples.
- No named service is required for conformance.
- No credential, token, or private account URL is added.
- GitHub is not represented as archival preservation by itself.
- Public-facing docs explain branch policy: branches are for implementation; example profiles are for user-specific service choices.

## Pull request

Open a PR titled:

```text
Add expanded recommended service integration candidates
```

Use this PR summary:

```markdown
## Summary
- Adds v0.2 service-role vocabulary and candidate catalog for additional open-science services.
- Adds Google Scholar, arXiv, Octopus, Dryad, PCI, HAL, bioRxiv, medRxiv, data.org, FORCE11, SCOSS, Crossref, and ROR as candidate examples.
- Keeps all named services nonmandatory and records David Ochabski's choices as a non-normative example profile.

## Validation
- [ ] YAML parse passed
- [ ] JSON parse passed
- [ ] Existing repo validation passed, if available
- [ ] No credentials or private dashboard URLs added
```
