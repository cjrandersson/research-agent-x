# Sändeman Source Registry

> Purpose: define sources as governed inputs with explicit access, provenance and historical properties.

## Why this exists

A source is not just a URL pattern. Sändeman needs to know how a source is accessed, what it is reliable for, whether it can be replayed historically, how often it may be queried, and whether its content can be retained or redistributed.

## Registry fields

Suggested schema:

```yaml
source_id: github
name: GitHub
family: code_ecosystem
access_method: api
historical_access: true
update_frequency: hourly
reliability_profile:
  repository_activity: high
  commercial_adoption: low
rate_limit_policy: required
license_review: required
robots_policy: not_applicable
retention_policy: metadata_first
redistribution_rights: review
status: active
```

Core fields:

```text
source_id
name
family
access_method
endpoint / adapter
historical_access
update_frequency
rate_limit_policy
license / terms review
robots policy where applicable
retention policy
redistribution rights
reliability profile
geographic scope
status
```

## Source families

Use source families to avoid treating multiple similar sources as fully independent evidence.

Initial families:

```text
company_filings
company_registry
code_ecosystem
package_ecosystem
academic_research
patents
regulation
procurement
jobs
company_web
mainstream_media
industry_media
community_forum
social
standards
hardware_approval
```

## Proposed source phases

### Phase 1 — reproducible, structured and high-value

- GitHub
- Hacker News
- Reddit
- SEC EDGAR
- Companies House
- Bolagsverket open data / APIs
- public ATS job postings (for example Greenhouse / Lever where publicly exposed)
- arXiv / Semantic Scholar
- package ecosystems such as PyPI / npm
- Hugging Face Hub for AI/ML research profiles
- RDAP for domain-registration signals

### Phase 2 — specialist commercial and regulatory evidence

- public procurement
- patents
- standards bodies
- regulatory feeds
- specialist forums
- FCC / relevant technical approval datasets

### Phase 3 — difficult / permission-sensitive sources

- Discord
- Telegram
- closed communities
- licensed commercial datasets

These should not be part of the initial ingestion surface because access, privacy, provenance and historical reproducibility are substantially harder.

## Source-specific cautions

### Financing filings

Do not label all filing-derived financing activity as "stealth raises". Treat it as early or newly disclosed financing evidence, with the exact filing type preserved.

### Job postings

Public ATS postings can reveal hiring patterns, capability expansion and geographic expansion. Do not describe public postings as hidden/internal roles unless the source explicitly supports that claim.

### Package downloads

Download volume is not equivalent to adoption or quality. Combine velocity with other evidence such as dependent projects, contributor activity, integrations and job requirements.

### Domain registration

A new domain is weak evidence in isolation. It becomes more useful when combined with independent company, hiring, filing or product signals.

### Community sources

Forums and social channels may be strong for discovering pain but weaker for verifying commercial facts. Reliability is claim-type specific.

## Source independence

Convergence should be calculated using independent evidence roots and source families, not raw URL count.

Example:

```text
SEC filing
  ↓
news article
  ↓
newsletter
  ↓
Reddit discussion
```

This chain should not receive the same independence score as four unrelated observations from separate source families.

## MVP rule

Add sources only when they improve one of these capabilities:

1. anomaly detection
2. velocity detection
3. independent validation
4. commercial evidence
5. counter-evidence
6. historical replay

A large connector count is not a product metric.
