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

### D-008 — V1 is Founder Opportunity first

Sändeman V1 is built first as our own venture-discovery system using a **Founder Opportunity Profile**.

The underlying **Sändeman Core** remains profile-agnostic so VC Scout, Corporate Strategy and other profiles can be added later without rebuilding the evidence engine.

### D-009 — Initial research domain

The first research domain is:

**Enterprise infrastructure & emerging B2B software**

Initial subdomains:

- AI infrastructure
- developer tooling
- integration / interoperability
- vertical operational software

The purpose of the initial scope is to improve signal quality, evaluation quality and backtesting before expanding into broader sectors.

### D-010 — Swedish must be a first-class explanation layer

Sändeman must be documented in clear Swedish as well as in technical English.

The Swedish layer should explain the product, research logic and architecture in the simplest accurate language possible, so new collaborators can understand the idea without first reading technical specifications.

Technical terms may remain in English where that is clearer, but each important concept should have a simple Swedish explanation.

### D-011 — README is the live development cockpit

The repository front page must always show the current development state clearly enough that the team can understand where Sändeman is without reading issues, chat history or commit logs.

The README must always contain, near the top:

- current phase / milestone
- current status
- exact next code task
- milestone checklist with completed items checked off
- what follows immediately after the current milestone
- whether anything is blocked or waiting for a team decision
- last-updated date

**Primary maintenance rule:** any meaningful change to implementation status, architecture, milestone completion or next-step priority is not considered fully documented until the README development-status section has also been updated.

The status block is for the team first. It should optimize for operational clarity rather than presentation to outsiders.

### D-012 — Every pending item must have an explicit owner

Nothing may appear as `pending`, `blocked`, `waiting`, `next`, or otherwise require action in the Development Cockpit without naming who owns the next move.

Use explicit owner labels:

- `@cjrandersson` for Robin / project-owner decisions or actions
- `ChatGPT` for analysis, architecture, specification, documentation or review work to be performed in an active ChatGPT session
- `Codex` for repository implementation work assigned to Codex
- a named collaborator for any other person, e.g. `Gonzalo`

Do not invent GitHub handles. Use a GitHub `@mention` only when the actual handle is known.

If Robin's input is required, make it visually explicit in the cockpit, for example:

`🚨 @cjrandersson — choose source A or B before implementation continues`

The cockpit must contain an **Active ownership / pending** table so everyone can immediately see who has the next move. If an owner has nothing pending, say `Nothing` / `CLEAR` rather than omitting them when they are part of the active team.

This ownership rule is part of the same maintenance contract as D-011: a project-status change is not fully documented until both status and ownership are current in README.

## Pending

No blocking product decisions are currently pending.
