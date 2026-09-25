# Sändeman Core Data Model

> Goal: make every signal traceable from output back to raw evidence.

## Canonical objects

```text
Source
SourceSnapshot
RawDocument
Observation
Claim
Entity
Relationship
Event
SignalCluster
SignalScore
Evidence
Hypothesis
Opportunity
Evaluation
ResearchRun
```

## Object roles

### Source
Defines where evidence originates and how it may be accessed.

### SourceSnapshot
Captures a source state at a specific time for reproducibility.

### RawDocument
The immutable fetched artefact or normalized source payload.

Examples: filing, job posting, repository metadata payload, forum post, regulatory notice.

### Observation
An atomic factual observation extracted from a RawDocument.

Example: `Company X posted five new inference-engineering roles.`

### Claim
A statement made by a source that may or may not be independently verified.

Claims must retain provenance and should not be silently converted into facts.

### Entity
A persistent object such as:

- person
- company
- fund
- repository
- technology
- product
- patent
- domain
- regulation
- market

### Relationship
A typed edge between entities.

Examples:

- `PERSON founded COMPANY`
- `COMPANY maintains REPOSITORY`
- `COMPANY raised_from FUND`
- `COMPANY hiring_for CAPABILITY`

### Event
A normalized, time-bound change derived from one or more observations.

Example:

```json
{
  "entity": "Company X",
  "event_type": "HIRING_EXPANSION",
  "topic": "inference infrastructure",
  "value": 5,
  "observed_at": "2026-09-23"
}
```

### SignalCluster
A group of related events that may represent the same emerging market phenomenon.

### SignalScore
Internal quantitative features used to rank and filter clusters.

### Evidence
A link between a hypothesis/signal and supporting or weakening observations, including independence/provenance metadata.

### Hypothesis
A falsifiable interpretation of a signal cluster.

### Opportunity
A commercially framed hypothesis that has passed the required research gates.

### Evaluation
Evidence-backed qualitative or quantitative assessment at a point in time.

### ResearchRun
Records one reproducible execution, including profile, cutoff time, configuration and code/model versions where available.

## Minimum metadata

Every temporal or evidence-bearing object should carry the relevant subset of:

```text
id
created_at
observed_at
published_at
first_seen_at
ingested_at
source_id
source_url
source_type
ingestion_run_id
confidence
provenance_root_id
```

## Core invariants

1. Raw source artefacts are immutable.
2. Every observation can be traced to a RawDocument.
3. Every event can be traced to observations.
4. Every signal can be traced to events.
5. Every hypothesis can show supporting and weakening evidence.
6. Duplicate or syndicated documents do not create artificial evidence independence.
7. Historical queries must respect the `as_of` cutoff.
8. Stable IDs are used so signals and opportunities accumulate evidence over time instead of being recreated each run.

## Initial relational implementation

PostgreSQL is sufficient for v0.1.

Suggested initial tables:

```text
sources
source_snapshots
raw_documents
observations
claims
entities
entity_aliases
relationships
events
signal_clusters
signal_cluster_events
signal_scores
evidence
hypotheses
opportunities
evaluations
research_runs
```

A dedicated graph database is not required for the MVP.
