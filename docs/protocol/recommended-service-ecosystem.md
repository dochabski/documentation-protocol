<!-- SPDX-License-Identifier: CC0-1.0 -->

# Recommended Service Ecosystem

This page explains the Documentation Protocol's **Recommended Service Integration Profile**.

The protocol recommends **service roles**, not mandatory vendors. A package can satisfy a role with any public, institutional, local, or discipline-specific service that provides equivalent evidence. A project remains conformant when a recommended role is deferred, substituted, or omitted with rationale, unless another protocol product independently requires the underlying evidence for the target conformance level.

## Branch policy

Use a Git branch for implementation work and review. Do not maintain a permanent branch for one person's preferred service ecosystem. User- or project-specific choices belong in profile files such as:

```text
examples/service-profiles/david-ochabski-service-profile.yaml
examples/service-profiles/<project-or-user>-service-profile.yaml
```

## Recommended service roles

| Role | Status | Candidate examples |
|---|---:|---|
| Working storage and staging | recommended | Dropbox, OneDrive, Google Drive, institutional storage |
| Source control and change management | highly recommended | GitHub, GitLab, Codeberg, Bitbucket |
| Persistent contributor identity | recommended | ORCID, institutional identifiers |
| DOI archival deposit or equivalent preservation | highly recommended for publication-ready packages | Zenodo, Figshare, Mendeley Data, OSF, Dryad, Dataverse, HAL, institutional repositories |
| Metadata and indexing interoperability | recommended | DataCite, OpenAlex, Crossref, ROR, Google Scholar, ORCID, CITATION.cff, codemeta.json |
| Identifier registration infrastructure | recommended where applicable | DataCite, Crossref, ROR, ORCID |
| Scholarly discovery profile | optional | Google Scholar, ORCID, OpenAlex, ResearchGate, Academia.edu |
| Data or supplement repository | recommended when data/supplements exist | Dryad, Figshare, Mendeley Data, Zenodo, OSF, Dataverse |
| Preprint or paper dissemination | optional | arXiv, bioRxiv, medRxiv, HAL, SSRN, OSF Preprints, Octopus |
| Open peer review and recommendation | optional | Peer Community In, PREreview, OpenReview |
| OER or training dissemination | optional | OER Commons, VIVA Open, MERLOT, Pressbooks |
| Professional and public communication | optional | LinkedIn, Substack, X, YouTube, Instagram, Spotify for Creators |
| Open-science community and sustainability | optional | FORCE11, SCOSS, data.org, Research Data Alliance |
| Long-form publication | optional | Amazon KDP, Pressbooks, Leanpub, university or institutional presses |

## Candidate Service Reference

These service notes explain common candidate examples. They are descriptive, not mandatory.

| Service | Typical role | What it does |
|---|---|---|
| Dropbox | Working storage | Synchronizes private working files, source-material staging folders, exports, and backups before public release. |
| ORCID | Persistent contributor identity | Provides persistent researcher identifiers that connect contributors, works, affiliations, and citation metadata. |
| Mendeley Data | Data or supplement repository | Hosts datasets and supplementary research materials, often with DOI support. |
| Zenodo | DOI archival deposit | Archives research objects and release snapshots with DOI support, including common GitHub release workflows. |
| DataCite | Identifier infrastructure | Provides DOI registration and metadata infrastructure, typically through repositories or member organizations. |
| GitHub | Source control and change management | Hosts Git repositories, issues, pull requests, tags, releases, and automation workflows. GitHub alone is not L5 archival preservation. |
| OSF | Open project wrapper | Provides project pages, components, registrations, files, and related research context. |
| SSRN | Preprint or paper dissemination | Shares preprints, working papers, and reports in relevant scholarly communities. |
| Figshare | Archive or supplement repository | Hosts citable research outputs such as datasets, figures, posters, supplements, and other public artifacts. |
| ResearchGate | Scholarly communication | Supports researcher profiles, publication sharing, project visibility, and scholarly networking. |
| OER Commons | OER dissemination | Shares open educational resources, teaching modules, and learning materials. |
| VIVA Open | OER/open publishing | Shares open educational and open publishing materials in supported communities. |
| MERLOT | OER dissemination | Curates learning objects and teaching resources for discoverability and reuse. |
| Academia.edu | Scholarly communication | Supports academic profiles, publication visibility, and audience building. |
| LinkedIn | Professional communication | Shares release announcements and practitioner-facing summaries with professional audiences. |
| Substack | Long-form communication | Publishes newsletter-style explanations, updates, essays, and practitioner guidance. |
| X | Short-form communication | Supports announcements, brief updates, and public discussion threads. |
| YouTube | Video communication | Hosts demonstrations, tutorials, walkthroughs, teaching videos, and release explanations. |
| Instagram | Visual communication | Supports visual public outreach and release awareness. |
| Spotify for Creators | Audio/video communication | Publishes podcasts or media discussions about releases, methods, or artifacts. |
| OpenAlex | Scholarly index | Indexes scholarly works, authors, institutions, topics, sources, and citations for discovery and context. |
| Amazon KDP | Long-form publication | Publishes book-length guides, manuals, workbooks, or practitioner derivatives. |
| Google Scholar | Scholarly discovery profile | Indexes scholarly works and supports public author profiles and citation discovery. |
| arXiv | Preprint dissemination | Disseminates preprints in fields such as computer science, mathematics, physics, statistics, quantitative biology, quantitative finance, electrical engineering, systems science, and economics. |
| Octopus | Modular open publication | Publishes modular research outputs to support transparent scholarly communication beyond article-only formats. |
| Dryad | Data repository | Hosts publishable datasets and supplementary data packages, commonly linked to publications. |
| Peer Community In | Open peer review and recommendation | Coordinates community review and recommendation of preprints and related research outputs. |
| HAL | Open archive | Provides scholarly deposit and manuscript dissemination, especially in French and European research contexts. |
| bioRxiv | Preprint dissemination | Hosts life-sciences preprints before peer review. |
| medRxiv | Preprint dissemination | Hosts health-sciences preprints; clinical or medical claims need clear non-peer-reviewed cautions. |
| data.org Funding Opportunities | Open-science sustainability | Helps discover funding and program opportunities relevant to data-for-social-impact and open-data initiatives. |
| FORCE11 | Open-science community | Supports community work around scholarly communication, research data, identifiers, and open-science practices. |
| SCOSS | Infrastructure sustainability | Coordinates support for open-science infrastructure sustainability. |
| Crossref | Identifier infrastructure | Registers DOIs and metadata, primarily through publisher, repository, organization, or sponsor workflows. |
| Research Organization Registry | Organization identifiers | Provides persistent identifiers and metadata for research organizations. |

## Evidence rule

For public protocol records, record stable public evidence only: public profile pages, repository URLs, DOIs, deposit pages, public metadata records, preprint identifiers, review URLs, or public documentation pages. Do **not** record private dashboard URLs, submission-console URLs, authentication tokens, account identifiers that are not meant for public release, or credentials.

## Important non-requirements

The protocol does not require any user to have accounts with Google Scholar, arXiv, Octopus, Dryad, Peer Community In, HAL, bioRxiv, medRxiv, Crossref, DataCite, ROR, FORCE11, SCOSS, or any other named service. These are candidate examples for service roles.
