<div align="center">

# SÄNDEMAN

### Peripheral intelligence · Wide-field intelligence for markets in motion

**A peripheral, wide-angle research system for finding real market friction before it becomes obvious.**

`CORE SCAN → DEEP DIVE → EVALUATE → TRACK`

</div>

---

# 🛰️ Development Status — Team Cockpit

> **This is the operational source of truth for where the project is right now.**  
> Update this section whenever implementation status, architecture, milestone completion, ownership or the immediate next step changes.

| | Current state |
|---|---|
| **Current milestone** | **M1 — Sändeman Core v0.1: executable foundation** |
| **Status** | 🟡 **READY TO IMPLEMENT** |
| **Current objective** | Turn the defined architecture into the first executable Python package and canonical data pipeline |
| **Exact next code task** | Create `pyproject.toml`, `src/sandeman/` and typed canonical models for `Source`, `RawDocument`, `Observation`, `Event` and `SignalCluster` |
| **Next-task owner** | **Codex** |
| **Blocked / waiting on team** | ✅ **Nothing** |
| **Next milestone** | **M2 — First real source adapters + provenance/deduplication pipeline** |
| **Last updated** | **2026-09-25** |

### Active ownership / pending

| Owner | Pending now | State |
|---|---|---|
| **@cjrandersson** | Nothing required before M1 implementation can start | ✅ **CLEAR** |
| **ChatGPT** | Keep architecture, definitions, review findings and this cockpit synchronized whenever the project changes | 🟢 **ACTIVE RULE** |
| **Codex** | Implement the M1 Python scaffold and canonical typed models | 🟡 **NEXT MOVE** |
| **Gonzalo** | Nothing assigned yet | ⚪ **CLEAR** |

> **Ownership rule:** nothing may be marked `pending`, `blocked`, `waiting` or `next` without an explicit owner. If Robin must act, show it explicitly as `🚨 @cjrandersson — <required action>`. Use `ChatGPT`, `Codex` or a named collaborator for other owners. Do not invent GitHub handles.

### Milestone progress

- [x] **M0 — Product & architecture definition**
  - [x] Research policy and Core Scan / Deep Dive model
  - [x] Founder Opportunity Profile selected for V1
  - [x] Initial research domain locked
  - [x] Sändeman Core architecture defined
  - [x] Canonical data model defined
  - [x] Signal Engine contract defined
  - [x] Source Registry rules defined
  - [x] Historical `as_of` / backtest requirement defined
  - [x] Swedish first-class explanation layer added

- [ ] **M1 — Sändeman Core v0.1: executable foundation** ← **CURRENT**
  - [ ] Create Python package scaffold — **Codex**
  - [ ] Implement typed canonical models — **Codex**
  - [ ] Implement Source Registry loader / schema — **Codex**
  - [ ] Implement immutable RawDocument ingestion contract — **Codex**
  - [ ] Implement `Observation → Event` transformation contract — **Codex**
  - [ ] Add basic persistence with historical timestamps — **Codex**
  - [ ] Add `as_of` filtering contract — **Codex**
  - [ ] Add unit tests for model validation and temporal rules — **Codex**

- [ ] **M2 — Ingestion + provenance**
  - [ ] Add first real source adapters
  - [ ] Canonical normalization
  - [ ] Deduplication
  - [ ] Evidence-root / provenance tracking
  - [ ] Entity resolution foundation

- [ ] **M3 — Signal Engine + historical replay**
  - [ ] Signal clustering
  - [ ] Anomaly / velocity / convergence features
  - [ ] Internal signal vector
  - [ ] Historical replay runner
  - [ ] First backtest against a defined historical case

- [ ] **M4 — Founder Opportunity research loop**
  - [ ] Core Scan output from real data
  - [ ] Deep Dive escalation
  - [ ] Opportunity log
  - [ ] Weekly Radar V1
  - [ ] First measurable Precision@K / lead-time benchmark

**Rule:** a meaningful project change is not fully documented until this cockpit reflects the new state **and the correct owner for every pending action**.

---

## Vad är Sändeman? 🇸🇪

**Sändeman letar efter flera små, oberoende förändringar som tillsammans kan avslöja ett viktigt marknadsskifte innan det blivit uppenbart.**

Kortare:

> **Sändeman försöker se vad som håller på att hända, inte bara vad alla redan pratar om.**

➡️ **[Läs den enkla svenska förklaringen](./docs/SANDEMAN_PA_SVENSKA.md)**

---

## What is Sändeman?

Sändeman is a research framework for continuously discovering and validating **evidence-backed startup opportunities**.

Instead of chasing headlines, it looks for the quieter signals underneath markets: repeated complaints, manual work, weak integrations, regulatory pressure, hiring patterns, procurement, incumbent failures and new technical capabilities.

> **The goal is not to generate more ideas.**  
> The goal is to find problems worth investigating.

---

## Research system

| Layer | Purpose | Output |
|---|---|---|
| 🟦 **01 · Scope** | Define where to look and what is feasible | Research boundaries |
| 🟨 **02 · Core Scan** | Detect weak signals, pain and change | Signal radar |
| 🟧 **03 · Deep Dive** | Verify the strongest signals | Opportunity cards |
| 🟩 **04 · Evaluate & Track** | Compare evidence over time | Opportunity log + weekly radar |

```text
DEFINE SCOPE
     ↓
CORE SCAN
     ↓
10–20 SIGNALS
     ↓
FILTER
     ↓
2–5 CANDIDATES
     ↓
DEEP DIVE
     ↓
0–3 OPPORTUNITIES
     ↓
UPDATE LOG
     ↓
WEEKLY RADAR
```

---

## Sändeman Core

The research policy above remains the human-readable operating model. Underneath it, Sändeman is now being defined as a **temporal signal engine** that turns fragmented source material into persistent, traceable and falsifiable signals.

```text
RAW DOCUMENT
     ↓
OBSERVATION
     ↓
EVENT
     ↓
SIGNAL CLUSTER
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

Core architectural principles:

- provenance before source-count inflation
- temporal history and reproducible `as_of` backtesting from day one
- deterministic state, scoring and thresholds outside the LLM
- internal numerical signal features, interpretable external output
- evidence that both strengthens and weakens hypotheses

The Core Engine is designed to remain profile-agnostic so different research profiles can later use the same underlying evidence system.

---

## What the radar looks for

<table>
<tr>
<td width="50%" valign="top">

### 🟦 Friction

- Repeated customer pain
- Manual workflows
- Excel / email / PDF operations
- Integration gaps
- Human middleware
- Reconciliation work

</td>
<td width="50%" valign="top">

### 🟨 Change

- New technology
- Agent / MCP adoption
- New standards and APIs
- Regulation
- Cost shifts
- Market restructuring

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🟧 Commercial evidence

- Existing software spend
- Hiring
- Procurement / RFPs
- Consulting spend
- Switching attempts
- Explicit buying intent

</td>
<td width="50%" valign="top">

### 🟩 Opportunity

- Weak incumbents
- Clear buyer
- Narrow MVP
- Measurable ROI
- Accessible customers
- Expansion path

</td>
</tr>
</table>

---

## Research focus

### 🟪 Legacy infrastructure
**EDI modernization · EDI-to-API · MCP infrastructure · ERP interoperability · integration observability**

### 🟦 B2B software & AI
**Agentic workflows · enterprise AI · developer infrastructure · data orchestration · RevOps automation**

### 🟨 Vertical software
**Industry-specific SaaS · specialized commerce · RegTech · procurement · operational software**

### 🟩 Climate & energy
**Grid software · ESS/BESS · industrial energy · AgriTech · water · circular systems**

### 🟥 Resilience & financial infrastructure
**Cybersecurity · critical infrastructure · geospatial intelligence · embedded B2B finance · fraud prevention**

---

## V1 research domain

Sändeman V1 is intentionally narrower than the long-term research universe.

**Initial domain:** Enterprise infrastructure & emerging B2B software

- AI infrastructure
- developer tooling
- integration / interoperability
- vertical operational software

The first product profile is the **Founder Opportunity Profile**: Sändeman is used as our own venture-discovery system first, while the underlying Core Engine remains reusable for later VC, strategy and market-intelligence profiles.

---

## Geographic lens

**Primary**  
🇸🇪 Sweden · 🇳🇴 Norway · 🇩🇰 Denmark · 🇫🇮 Finland

**Secondary**  
🇪🇺 European Union · 🇬🇧 United Kingdom · 🇺🇸 United States

**Research principle**  
A signal can emerge in one market while the best launch market exists somewhere else.

`SIGNAL MARKET → PROBLEM MARKET → INITIAL TARGET → EXPANSION MARKET`

---

## Founder feasibility filter

Sändeman prioritizes opportunities that can realistically begin with:

| Constraint | Default |
|---|---:|
| Team | **1–2 founders** |
| Initial capital | **$5k–$25k** |
| Available time | **~20 h / week** |
| Strategy | **Bootstrapped first** |
| Preferred model | **B2B / SaaS / API / automation / vertical software** |

> **Small product surface + painful problem + high customer value.**

Capital-intensive hardware, biotech/pharma development, speculative crypto, heavily regulated financial entities and operationally heavy businesses are generally deprioritized.

---

## Weekly output

Each research cycle should produce a compact radar rather than a long trend report.

| Opportunity | Status | Evidence | Commercial | Founder fit | Next proof |
|---|---|---|---|---|---|
| Example A | 🟢 Strengthening | High | High | High | Interview 5 buyers |
| Example B | 🟡 Watch | Medium | Medium | High | Find procurement evidence |
| Example C | 🔴 Weakening | Medium | Low | Medium | Re-test willingness to pay |

### Status language

`NEW` · `STRENGTHENING` · `WATCH` · `UNCHANGED` · `WEAKENING` · `INVALIDATED`

Every serious opportunity receives a stable ID so evidence accumulates over time instead of being rediscovered each week.

---

## Evidence before enthusiasm

A strong signal should ideally combine several independent forms of evidence:

```text
COMPLAINT
   +
WORKAROUND
   +
RECURRENCE
   +
IDENTIFIABLE BUYER
   +
MEASURABLE COST
   +
TECHNOLOGY / REGULATORY CATALYST
   ↓
POTENTIAL OPPORTUNITY
```

Funding, headlines and search growth are **signals**, not proof.

Sändeman actively looks for evidence that both **supports and weakens** an opportunity.

---

## Documentation

| Document | Purpose |
|---|---|
| **[Sändeman på svenska](./docs/SANDEMAN_PA_SVENSKA.md)** | Simple Swedish explanation for collaborators and non-specialist readers |
| **[Weekly Research Handbook](./WEEKLY_RESEARCH_HANDBOOK.md)** | Source of truth for layers, definitions, metrics, visualization and weekly research rules |
| **[How it is built & how we run it](./HUR%20BYGGS%20DET%20%26%20HUR%20K%C3%96R%20VI%20DET.md)** | Simplified operating model and research flow |
| **[Core Architecture](./docs/ARCHITECTURE.md)** | Technical system boundaries, machine pipeline, LLM responsibilities and temporal requirements |
| **[Data Model](./docs/DATA_MODEL.md)** | Canonical objects, traceability rules and initial relational schema |
| **[Signal Engine](./docs/SIGNAL_ENGINE.md)** | Signal features, noise reduction, escalation and benchmark metrics |
| **[Source Registry](./docs/SOURCE_REGISTRY.md)** | Source governance, source families, ingestion phases and provenance rules |
| **[Decision Log](./docs/DECISIONS.md)** | Locked architectural and product choices |
| **README** | Project overview, navigation and live development cockpit |

---

## Design principle

> **Core Scan finds signals.**  
> **Deep Dive verifies signals.**  
> **Evaluation decides what deserves attention.**  
> **The opportunity log remembers what changed.**

<div align="center">

### SÄNDEMAN
**Wide-angle research. Narrow, evidence-backed opportunities.**

</div>
