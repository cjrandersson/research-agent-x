# Sändeman Core Architecture

> Status: Core definition for the next implementation phase.

## Purpose

Sändeman is evolving from a prompt-driven research framework into a temporal venture-intelligence system.

The existing research policy remains valid:

`Research Scope → Core Scan → Filter → Deep Dive → Evaluation → Opportunity Log → Weekly Radar`

The new Core Engine sits underneath that workflow and converts fragmented source material into persistent, comparable and falsifiable signals.

## Core principle

Sändeman should not reason directly from a pile of URLs.

The canonical machine pipeline is:

```text
SOURCE REGISTRY
      ↓
INGESTION
      ↓
RAW DOCUMENT
      ↓
NORMALIZATION
      ↓
DEDUPLICATION + PROVENANCE
      ↓
OBSERVATION
      ↓
EVENT EXTRACTION
      ↓
ENTITY RESOLUTION
      ↓
TEMPORAL STORE
      ↓
SIGNAL CLUSTERING
      ↓
SIGNAL ENGINE
      ↓
EVIDENCE / CLAIM GRAPH
      ↓
CORE SCAN
      ↓
DEEP DIVE
      ↓
HYPOTHESIS
      ↓
OPPORTUNITY
      ↓
TRACK / TEST / INVALIDATE
```

## Separation of concerns

### Deterministic code owns

- ingestion state
- source identity
- timestamps
- historical cutoffs
- deduplication
- provenance
- arithmetic/scoring
- threshold logic
- persistence
- reproducibility

### LLMs may assist with bounded tasks

- event extraction
- claim extraction
- classification
- entity-link fallback
- cluster description
- counter-evidence synthesis
- hypothesis synthesis

The LLM must not be the system of record.

## Sändeman Core vs research profiles

The Core Engine should be profile-agnostic.

Profiles may change:

- sectors
- geographies
- source weights
- signal weights
- escalation thresholds
- feasibility constraints
- output format

Potential profiles:

- Founder Opportunity
- VC Scout
- Corporate Strategy
- PE / Diligence

The first product profile remains an open product decision.

## Temporal architecture

Historical replay is a first-class requirement, not a later analytics feature.

Every research run must support an `as_of` cutoff so that no document published after the historical cutoff can influence a backtest.

Required temporal fields should include at minimum:

- `published_at`
- `first_seen_at`
- `ingested_at`
- `valid_from` where applicable

Conceptual execution:

```bash
sandeman research --profile founder-opportunity --as-of 2024-03-01
```

## Evidence independence

Five URLs are not automatically five independent pieces of evidence.

Sändeman must track source ancestry and shared origins so that syndicated or derivative documents do not inflate convergence.

Example:

```text
Company filing
   ↓
Reuters
 ↙     ↘
Blog A  Newsletter B
   ↓
Reddit
```

This is primarily one evidence root unless separate observations independently corroborate the claim.

## Implementation priority

Before a visual dashboard, implement:

1. Source Registry
2. Canonical data models
3. Observation → Event pipeline
4. Provenance + deduplication
5. Entity resolution
6. Signal clustering
7. Internal signal vector
8. Historical replay
9. Benchmark/evaluation harness

The UI should expose the intelligence produced by the engine, not substitute for it.
