# Sändeman Decision Log

This file tracks architectural and product decisions that materially affect the system.

## Locked

### D-001 — Preserve the existing research policy

The current research flow remains valid:

`Research Scope → Core Scan → Filter → Deep Dive → Evaluation → Opportunity Log → Weekly Radar`

The new technical Core Engine is built underneath it rather than replacing it.

### D-002 — Introduce a canonical machine pipeline

Use:

`RawDocument → Observation → Event → SignalCluster → Core Scan → Deep Dive → Hypothesis → Opportunity → Track/Test/Invalidate`

### D-003 — Provenance is a core capability

Evidence independence is based on independent evidence roots, not URL count.

### D-004 — Historical replay is a first-class requirement

The architecture must support `as_of` research cutoffs from the beginning to prevent future-data contamination in backtests.

### D-005 — Internal scores, interpretable external output

Numerical signal features may be used internally for ranking and benchmarking. User-facing outputs should avoid unexplained false precision.

### D-006 — Deterministic state outside the LLM

Timestamps, provenance, deduplication, scoring arithmetic, thresholds and persistent state are controlled by code. LLMs are used only for bounded extraction, classification and synthesis tasks.

### D-007 — Source count is not a product metric

New sources are added only when they improve anomaly detection, velocity, independent validation, commercial evidence, counter-evidence or historical replay.

## Pending

### P-001 — Primary V1 user

Choose one:

**A. Founder Opportunity first**  
Use Sändeman primarily as our own venture-discovery system first, while keeping Sändeman Core profile-agnostic.

**B. Commercial VC Intelligence first**  
Design the first product experience directly for external VC/strategy users.

Current recommendation: **A**.

### P-002 — Initial research domain

Proposed initial domain:

**Enterprise infrastructure & emerging B2B software**

Initial subdomains:

- AI infrastructure
- developer tooling
- integration / interoperability
- vertical operational software

Decision needed: approve as-is or edit.
