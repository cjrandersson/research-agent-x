# Weekly Research Handbook

> **Purpose:** Operational handbook for the recurring venture-intelligence research process.
>
> This document explains **how the system thinks, what each layer does, how signals become opportunities, what we measure, and how results should be visualized and interpreted**.

---

## 0. The Core Idea

The research system is intentionally split into layers so that every weekly run does **not** perform a full market investigation on every weak signal.

The operating chain is:

**Research Scope → Core Scan → Filter → Deep Dive → Evaluation → Opportunity Log → Weekly Radar → Next Cycle**

Or, conceptually:

**Signal → Evidence → Interpretation → Opportunity → Missing Proof → Validation → Updated Status**

The system should behave like a radar, not like an idea generator.

- **Core Scan finds radar blips.**
- **Deep Dive investigates promising targets.**
- **Evaluation determines whether the target is commercially and practically interesting.**
- **Opportunity Log preserves memory between runs.**
- **Weekly Radar makes change visible over time.**

The goal is not to manufacture a fixed number of startup ideas each week.

If evidence is weak, the correct output may be **zero new opportunities**.

---

# Layer 1 — Research Scope

## Definition

Research Scope defines the stable boundaries of the system before a weekly scan begins.

It answers:

> **What are we interested in, where do we look, and what is realistically buildable by us?**

This layer changes relatively slowly and should therefore live primarily in the **Master Research Specification**, with only a compressed version included in the production prompt.

## Includes

- Sectors & Topics
- Cross-sector opportunity patterns
- Geographic scope
- Research languages
- Founder capabilities
- Team size
- Initial budget
- Available time
- Preferred startup profiles
- Exclusions / deprioritized opportunity types
- Source universe

## Current founder feasibility assumptions

- **Team:** solo founder or 2-person technical team
- **Initial budget:** approximately **$5,000–$25,000 USD**
- **Available time:** approximately **20 hours/week**
- **Default strategy:** bootstrapped first, external capital optional later

These are not merely descriptive facts. They are a **hard feasibility filter**.

An attractive market that requires a large hardware team, years of regulatory approval, or millions in capital may still contain a relevant opportunity, but the research should search for a smaller **software, data, API, workflow, compliance, integration, or automation wedge**.

## Output of Layer 1

Layer 1 does not produce opportunities.

It produces the constraints used by all later layers.

---

# Layer 2 — Core Scan

## Definition

Core Scan is the recurring broad research layer.

Its job is not to prove that an opportunity is good.

Its job is to detect:

> **Problems, behavioral changes, market shifts, workarounds, technology changes, buying signals, or incumbent weaknesses that deserve further investigation.**

A Core Scan should remain relatively fast and wide.

## Seven Primary Signal Groups

### A. Pain

Look for:

- recurring complaints
- negative reviews
- missing features
- user frustration
- broken workflows
- expensive software
- poor integrations
- difficult onboarding
- recurring reliability problems

Primary question:

> **What do users repeatedly struggle with?**

---

### B. Manual Work / Human Middleware

Look for:

- Excel-heavy workflows
- email-driven processes
- copy/paste work
- manual reconciliation
- manual validation
- repetitive support investigation
- manual data transfer
- humans coordinating between systems
- staff repeatedly translating formats or information

Primary question:

> **Where are people still acting as middleware between systems, organizations, or datasets?**

This is a particularly important signal for the research system.

---

### C. Demand

Look for:

- increasing search interest
- “alternative to …” searches
- “how to automate …” discussions
- “API for …” requests
- explicit requests for tools
- hiring activity
- public procurement
- purchasing intent
- design-partner requests

Primary question:

> **Is there evidence that someone actively wants a solution?**

---

### D. Technology Shift

Look for changes that make previously difficult products possible:

- MCP
- AI agents
- cheaper inference
- small/local models
- new APIs
- new open-source infrastructure
- interoperability standards
- new data availability
- better agent tooling
- event-driven integration

Primary question:

> **What has recently become possible, cheaper, easier, or standardized?**

---

### E. Market / Regulatory Catalyst

Look for:

- new EU regulation
- compliance deadlines
- cybersecurity requirements
- labor shortages
- increasing labor costs
- energy-price changes
- ERP migration cycles
- new reporting requirements
- new industry standards
- supply-chain restructuring

Primary question:

> **What is forcing organizations to change behavior or spend money now?**

---

### F. Competitor / Incumbent Weakness

Look for:

- poor customer reviews
- outdated UX
- high prices
- difficult implementations
- poor APIs
- weak interoperability
- slow product development
- excessive consulting dependence
- customer dissatisfaction after acquisitions
- feature stagnation

Primary question:

> **Is an important problem poorly solved despite existing vendors?**

---

### G. Startup / Market Activity

Look for:

- new startups
- funding rounds
- accelerator cohorts
- acquisitions
- new categories
- founder migration
- product launches
- pivots
- shutdowns

Primary question:

> **Are multiple actors independently moving toward the same problem?**

Important:

Funding and startup activity are **signals of attention**, not proof of a good opportunity.

---

## Core Scan Funnel

A typical weekly scan may identify approximately:

- **10–20 raw signals**
- **2–5 candidates worth additional investigation**
- **0–3 opportunities worth adding or materially updating in the Opportunity Log**

These are guidelines, not quotas.

The system should return fewer findings when evidence is weak.

---

# Layer 2A — Core Scan Data Model

The Core Scan should be visualized primarily as a sortable **Signal Radar Table**.

The table should stay compact. Definitions should be available through expandable / collapsible help text in the UI or report.

## Recommended Core Scan Columns

### Signal ID

<details>
<summary><strong>Svensk förklaring</strong></summary>

Ett stabilt ID för samma signal över tid. Det förhindrar att samma problem skapas som ett nytt fynd varje vecka under olika namn.

Exempel: `SIG-EDI-007`.

</details>

### Problem / Signal

<details>
<summary><strong>Svensk förklaring</strong></summary>

En kort och neutral beskrivning av det faktiska problemet eller förändringen vi observerat.

Det ska beskriva observationen, inte redan formulera en startup-idé.

Bra: **“EDI teams manually investigate failed transactions across multiple systems.”**

Sämre: **“Build an AI EDI platform.”**

</details>

### Customer / User

<details>
<summary><strong>Svensk förklaring</strong></summary>

Personen, rollen eller gruppen som faktiskt upplever problemet i sitt dagliga arbete.

Exempel: EDI Specialist, Grid Operator, Compliance Manager.

</details>

### Likely Buyer

<details>
<summary><strong>Svensk förklaring</strong></summary>

Den roll, chef, avdelning eller budgetägare som sannolikt skulle kunna köpa en lösning.

Användaren och köparen behöver inte vara samma person.

</details>

### Sector / Vertical

<details>
<summary><strong>Svensk förklaring</strong></summary>

Vilken bransch eller specialiserad marknad signalen tillhör.

Exempel: Supply Chain, Energy, RegTech, Maritime, Retail EDI.

</details>

### Geography

<details>
<summary><strong>Svensk förklaring</strong></summary>

Var evidensen kommer ifrån och var problemet verkar vara relevant.

Skilj vid behov på signal market, problem market, initial target market och expansion market.

</details>

### Evidence Count

<details>
<summary><strong>Svensk förklaring</strong></summary>

Antalet **oberoende** belägg som stöder signalen.

Fem artiklar som alla återger samma ursprungskälla räknas inte som fem oberoende belägg.

Exempel: 8 separata klagomål från 6 företag.

</details>

### Source Diversity

<details>
<summary><strong>Svensk förklaring</strong></summary>

Hur många olika typer av källor som stödjer signalen.

Exempelvis är Reddit + G2 + jobbannonser + upphandling + produktdokumentation starkare än fem Reddit-trådar med samma typ av observation.

</details>

### Recurrence

<details>
<summary><strong>Svensk förklaring</strong></summary>

Hur återkommande problemet verkar vara.

Bedöm både frekvens och spridning: händer det ofta för samma användare, eller hos många olika organisationer?

Suggested interpretation: **Low / Medium / High**.

</details>

### Commercial Signal

<details>
<summary><strong>Svensk förklaring</strong></summary>

Hur mycket konkret evidens det finns för att problemet har ekonomisk betydelse.

Exempel på starka signaler:

- befintlig software spend
- konsulter
- anställda som hanterar problemet
- RFP / upphandling
- explicit köpintresse
- betald pilot
- kostsamma fel eller driftstopp

Suggested interpretation: **Low / Medium / High**.

</details>

### Catalyst / Why Now

<details>
<summary><strong>Svensk förklaring</strong></summary>

Vad som gör problemet eller möjligheten särskilt relevant **nu**.

Det kan vara AI, MCP, ny EU-reglering, lägre teknikkostnad, högre arbetskostnad, nya API:er eller förändrad marknadsstruktur.

En gammal smärta är inte automatiskt en bra startup idag. Vi vill förstå varför timingen kan ha förändrats.

</details>

### Status

<details>
<summary><strong>Svensk förklaring</strong></summary>

Visar hur signalen utvecklas mellan research-körningar.

Allowed states:

- **NEW** — ny signal
- **STRENGTHENING** — ny evidens stärker hypotesen
- **UNCHANGED** — inget väsentligt har förändrats
- **WATCH** — intressant men otillräckligt stöd
- **WEAKENING** — ny evidens gör hypotesen svagare
- **INVALIDATED** — centrala antaganden har motbevisats

</details>

### Action

<details>
<summary><strong>Svensk förklaring</strong></summary>

Vad research-systemet bör göra härnäst.

Typical actions:

- Ignore / archive
- Monitor
- Gather specific missing evidence
- Deep Dive

Action ska alltid vara kopplad till det som saknas, inte bara till hur spännande signalen känns.

</details>

### Next Proof

<details>
<summary><strong>Svensk förklaring</strong></summary>

Det mest värdefulla konkreta bevis vi behöver härnäst för att stärka eller försvaga hypotesen.

Exempel:

- hitta tre upphandlingar
- verifiera aktuell produktfunktion hos incumbent
- intervjua fem EDI managers
- hitta faktisk prisdata
- bekräfta att workflowet fortfarande är manuellt

`Next Proof` är en research-instruktion, inte bara en kommentar.

</details>

---

# Layer 3 — Deep Dive

## Definition

Deep Dive körs bara när en Core Scan-signal har tillräckligt stöd eller ovanligt stark kommersiell evidens.

Frågan förändras från:

> **“Finns det något här?”**

Till:

> **“Kan detta faktiskt bli en relevant och genomförbar business?”**

Deep Dive ska aktivt försöka både **stärka och motbevisa** hypotesen.

---

## Deep Dive Step 1 — Verify the Problem

Confirm that the problem is real.

Seek:

- multiple independent users
- multiple organizations
- multiple dates
- different source types
- concrete workflow examples

Also search for counterevidence.

Questions:

- Is the complaint still current?
- Has the incumbent already fixed it?
- Is it an edge case rather than a recurring problem?
- Is it implementation failure rather than a product gap?

---

## Deep Dive Step 2 — Map the Current Workflow

Understand exactly how the problem is solved today.

Example:

```text
Order fails
   ↓
EDI specialist checks VAN
   ↓
Downloads XML
   ↓
Compares transaction with ERP
   ↓
Emails trading partner
   ↓
Mapping team investigates
   ↓
Transaction is corrected and resent
```

This is important because products often hide inside the workflow itself.

The research should identify:

- systems involved
- human handoffs
- data formats
- delays
- duplicate work
- error points
- approvals
- external organizations

---

## Deep Dive Step 3 — Commercial Evidence

Determine whether organizations spend money or meaningful resources on the problem.

Investigate:

- existing software spend
- consulting spend
- staffing
- job postings
- procurement
- RFP/RFI activity
- outsourcing
- downtime
- error costs
- lost revenue
- compliance costs
- switching attempts
- explicit buying intent

We do not need a fabricated TAM calculation.

We need evidence supporting statements such as:

> **Organizations demonstrably spend money and staff time on this problem.**

---

## Deep Dive Step 4 — Existing Solutions & Competitive Gap

Map:

- incumbents
- startups
- internal tools
- consultants
- spreadsheets
- scripts
- open-source tools
- adjacent substitutes

Then determine:

> **What remains unsolved?**

A competitor is not automatically negative evidence.

A market with no competitors may indicate either an opportunity or lack of demand.

---

## Deep Dive Step 5 — Startup Wedge

Translate the verified problem into the **smallest commercially meaningful entry point**.

Avoid broad concepts such as:

> “AI platform for supply chains.”

Prefer narrow wedges such as:

> “AI diagnostic layer for failed EDI transactions that reads mapping logs, ERP state, and partner-specific rules and proposes a resolution.”

The wedge should answer:

- Who uses V1?
- What exact problem does V1 solve?
- What data does it require?
- What can remain manual initially?
- What makes the user willing to try it?

---

## Deep Dive Step 6 — Founder Fit

Evaluate against current constraints:

- 1–2 people
- $5k–$25k initial budget
- approximately 20 hours/week
- bootstrapped first

Questions:

- Can the first useful version be built by 1–2 people?
- Can the hypothesis be tested for less than $25k?
- Can meaningful progress happen part-time?
- Can 5–10 relevant customers realistically be reached?
- Can a concierge or service-assisted MVP test the concept?
- Can revenue begin before building the full platform?
- Is 24/7 manual operation avoidable?
- Can complexity be added gradually?

If not, search for a narrower wedge rather than immediately rejecting the entire market.

---

# Layer 3A — Deep Dive Evaluation Dimensions

The following dimensions should be shown in an **Opportunity Card**.

Use qualitative assessments such as **Low / Medium / High**, backed by evidence.

Do not invent false precision such as an unexplained `87/100` score.

## Problem Severity

<details>
<summary><strong>Svensk förklaring</strong></summary>

Hur allvarligt problemet är för kunden.

Consider:

- kostnad
- tidsförlust
- driftstopp
- risk
- fel
- compliance exposure
- förlorad försäljning
- kundpåverkan

High betyder att problemet har tydlig operativ eller ekonomisk konsekvens.

</details>

## Recurrence

<details>
<summary><strong>Svensk förklaring</strong></summary>

Hur ofta problemet uppstår och hur brett det verkar förekomma.

Ett problem kan vara allvarligt men mycket sällsynt. Ett annat kan vara mindre dramatiskt men inträffa hundratals gånger per vecka.

Båda dimensionerna behövs.

</details>

## Commercial Evidence

<details>
<summary><strong>Svensk förklaring</strong></summary>

Hur stark evidensen är för att företag redan lägger pengar, personal eller andra resurser på problemet.

High kräver mer än att användare säger att problemet är irriterande.

Stark evidens kan exempelvis vara:

- faktisk budget
- upphandling
- konsulter
- dedikerad personal
- kontrakt
- betald pilot

</details>

## Buyer Clarity

<details>
<summary><strong>Svensk förklaring</strong></summary>

Hur tydligt vi kan identifiera vem som äger problemet och vem som har mandat/budget att köpa lösningen.

High betyder att vi kan peka ut en konkret roll eller avdelning.

</details>

## Competitive Gap

<details>
<summary><strong>Svensk förklaring</strong></summary>

Hur mycket relevant problem som återstår trots befintliga produkter och leverantörer.

High betyder **inte** att marknaden saknar konkurrenter.

Det betyder att viktig friktion fortfarande verkar olöst eller dåligt löst.

</details>

## Why Now / Timing

<details>
<summary><strong>Svensk förklaring</strong></summary>

Hur starkt det finns en förändring som gör möjligheten mer relevant idag än tidigare.

Possible catalysts:

- AI/agent capabilities
- MCP
- regulation
- falling costs
- labor shortages
- new standards
- changing buyer behavior
- infrastructure migration

</details>

## MVP Feasibility

<details>
<summary><strong>Svensk förklaring</strong></summary>

Hur realistiskt det är att bygga och testa en liten men faktiskt värdefull första version.

High betyder att kärnhypotesen kan testas utan att bygga hela framtidsvisionen.

</details>

## Founder Fit

<details>
<summary><strong>Svensk förklaring</strong></summary>

Hur väl möjligheten passar våra faktiska resurser och kompetenser.

Bedömningen måste ta hänsyn till:

- teamstorlek
- budget
- tillgänglig tid
- teknisk komplexitet
- regulatorisk komplexitet
- operativ belastning

</details>

## Customer Accessibility

<details>
<summary><strong>Svensk förklaring</strong></summary>

Hur realistiskt det är att hitta, kontakta och få feedback från relevanta kunder.

En bra idé i en marknad där vi inte kan nå någon att intervjua eller sälja till är betydligt svårare att validera.

</details>

## Evidence Confidence

<details>
<summary><strong>Svensk förklaring</strong></summary>

Hur stark själva kunskapsgrunden är.

Detta är **inte** ett mått på hur attraktiv idén känns.

High betyder att flera oberoende, aktuella och relevanta källor stödjer våra centrala slutsatser.

Low betyder att mycket fortfarande bygger på antaganden.

</details>

---

# Non-Scored Opportunity Fields

Some of the most important information should **not** be converted into a score.

Each Opportunity Card should contain:

## Current Workflow

How the customer solves the problem today, preferably as a short process map.

## Startup Wedge

The narrowest meaningful product entry point.

## Biggest Risk

The single most important factor that could make the opportunity substantially worse than it currently appears.

## Next Proof

The next concrete piece of evidence or experiment that would most increase or decrease confidence.

These fields help prevent the dashboard from becoming a decorative scoring machine.

---

# Layer 4 — Evaluation & Opportunity Log

## Definition

Layer 4 turns Deep Dive findings into persistent research memory.

The objective is to track **change over time**, not rediscover the same opportunity every week.

Every qualified opportunity receives a stable ID.

Example:

`OPP-EDI-004 — AI-assisted EDI exception investigation`

If the next weekly run finds new supporting evidence, do not create a new opportunity.

Update the existing one.

---

## Opportunity Status System

### NEW

A newly qualified opportunity with enough evidence to enter the Opportunity Log.

### STRENGTHENING

New evidence materially improves the case.

Examples:

- independent complaints increase
- procurement appears
- buyer becomes clearer
- pricing evidence emerges
- technological feasibility improves

### UNCHANGED

The opportunity remains valid but no material evidence changed.

### WATCH

Interesting signal but currently insufficient evidence for full conviction or action.

### WEAKENING

New evidence reduces attractiveness or confidence.

Examples:

- incumbent ships missing feature
- demand declines
- customer interviews show low willingness to pay

### INVALIDATED

A critical assumption has been disproven.

Invalidated opportunities should remain in history rather than disappear, preventing the same failed hypothesis from being rediscovered later.

---

# Measured Facts vs Interpretation

The system should keep **measured facts separate from model interpretation**.

Examples of measured facts:

- Independent evidence: `11`
- Companies represented: `7`
- Evidence window: `180 days`
- Relevant job postings: `23`
- Relevant tenders: `4`
- Competitors identified: `9`
- Explicit workaround examples: `6`
- Observed pricing: `€8k–€30k/year`

Examples of interpretation:

- Recurrence: `High`
- Commercial Evidence: `High`
- Founder Fit: `Medium`
- Evidence Confidence: `High`

The interpretation must be explainable using the underlying facts.

Do not manufacture numbers when the data is unavailable.

---

# Data Visualization Strategy

The research output should use different visualizations for different zoom levels.

Do not put everything into one giant table.

---

## View 1 — Weekly Radar

### Purpose

Fast overview of the active research landscape.

This is the default weekly dashboard.

### Recommended columns

| Opportunity | Status | Evidence | Commercial | Founder Fit | Next Proof |
|---|---|---|---|---|---|
| EDI Exception Agent | STRENGTHENING | High | High | High | Interview 5 EDI managers |
| NIS2 Supplier Compliance | WATCH | Medium | Medium | High | Find 3 comparable tenders |
| Agent Checkout Infrastructure | WATCH | Low | Medium | Medium | Verify real merchant demand |

### Design principle

The table should answer within seconds:

1. What changed?
2. What is strongest?
3. What requires action next?

---

## View 2 — Core Scan Signal Radar

### Purpose

Show raw and semi-qualified signals before full opportunity analysis.

### Recommended fields

- Signal ID
- Problem / Signal
- Customer
- Likely Buyer
- Sector
- Geography
- Evidence Count
- Source Diversity
- Recurrence
- Commercial Signal
- Catalyst
- Status
- Action
- Next Proof

The interface should support sorting/filtering by:

- sector
- geography
- status
- evidence
- commercial signal
- founder relevance
- source type

---

## View 3 — Opportunity Card

### Purpose

Provide a one-minute understanding of one qualified opportunity.

Recommended structure:

```text
OPP-EDI-004
AI-assisted EDI exception investigation

Problem
EDI specialists manually investigate failed transactions across multiple systems.

Customer
EDI / Integration teams

Likely Buyer
Integration Manager / EDI Manager

Current Workflow
VAN → logs → ERP → XML → email → mapping specialist

Evidence
8 independent examples across 5 source types

Problem Severity       HIGH
Commercial Evidence    MEDIUM
Competitive Gap        HIGH
Founder Fit            HIGH
Evidence Confidence    HIGH

Why Now
LLM context handling + MCP + better enterprise agent tooling

Startup Wedge
Diagnostic assistant before automatic remediation

Biggest Risk
Enterprise system access and security

Next Proof
Interview 5 EDI specialists and obtain 2 real anonymized exception workflows
```

---

## View 4 — Deep Dive Report

### Purpose

Used only for the strongest opportunities.

A Deep Dive Report may include:

- problem definition
- workflow map
- evidence table
- customer and buyer
- competitor landscape
- pricing evidence
- commercial signals
- regulation
- technology catalyst
- startup wedge
- MVP
- business model
- founder feasibility
- risks
- counterevidence
- validation plan
- source coverage

Normally only **1–2 opportunities** should receive a full Deep Dive in one research cycle unless there is unusually strong evidence.

---

## View 5 — Evidence Timeline

### Purpose

Show how an opportunity evolves through time.

Example:

```text
JAN   User complaints appear
 ↓
FEB   Multiple job postings reveal manual workflow
 ↓
MAR   Public tender seeks similar functionality
 ↓
APR   New startup enters category
 ↓
MAY   Incumbent announces partial solution
```

This makes `STRENGTHENING` or `WEAKENING` explainable rather than arbitrary.

---

## View 6 — Opportunity Map

### Purpose

Visual comparison of the active opportunity portfolio.

Recommended scatter plot:

- **X-axis:** Founder Feasibility
- **Y-axis:** Commercial Evidence
- Optional bubble size: Problem Severity or Evidence Count
- Optional category: Sector

The most immediately actionable opportunities tend to move toward the upper-right region.

Important:

The chart is a navigation and comparison tool, not a substitute for the underlying evidence.

---

# Expandable / Collapsible Definitions in the UI

The dashboard should remain visually compact.

Column and dimension explanations should therefore be available through:

- `ⓘ` information controls
- expandable sections
- collapsible `<details>` blocks
- tooltips for very short definitions

Recommended pattern:

```text
Commercial Evidence ⓘ

[expanded]
Vad betyder detta?
Hur mycket konkret evidens finns för att företag redan spenderar pengar,
personal eller resurser på problemet?

HIGH
Recurring spend, procurement or clearly identified budget.

MEDIUM
Indirect spend or measurable operational cost exists.

LOW
Problem exists, but payment evidence is weak or absent.
```

This allows the dashboard to function as both a research interface and a built-in handbook.

---

# Weekly Research Execution Flow

The default weekly cycle is:

```text
1. LOAD RESEARCH SCOPE
          ↓
2. CORE SCAN
          ↓
3. DETECT RAW SIGNALS
          ↓
4. DEDUPLICATE AGAINST OPPORTUNITY LOG
          ↓
5. FILTER / TRIAGE
          ↓
6. SELECT STRONGEST CANDIDATES
          ↓
7. DEEP DIVE
          ↓
8. EVALUATE FOUNDER + COMMERCIAL FIT
          ↓
9. UPDATE OPPORTUNITY LOG
          ↓
10. GENERATE WEEKLY RADAR
          ↓
11. DEFINE NEXT PROOF / NEXT RESEARCH ACTION
```

The next weekly run begins from the existing Opportunity Log rather than from zero.

---

# Deep Dive Trigger

Do **not** Deep Dive every signal.

Escalate when one or more of the following is true:

- multiple independent sources confirm the same problem
- unusually strong commercial evidence exists
- clear procurement or buying intent appears
- a strong regulatory catalyst creates mandatory work
- multiple companies expose the same manual workflow
- the problem appears severe and founder-feasible
- a technology change creates a genuinely new solution path

Do not escalate based solely on:

- media attention
- one viral post
- one funding announcement
- generic analyst predictions
- one unhappy review

---

# Research Quality Rules

## Prefer evidence over narrative

Primary and practitioner evidence is usually more valuable than generic trend commentary.

## Deduplicate

Multiple articles repeating one press release are one underlying signal, not independent confirmation.

## Check recency

A complaint from 2023 may have been resolved in 2026.

Always verify current product documentation when a feature gap is central to the opportunity.

## Search for counterevidence

Each Deep Dive should contain evidence that could weaken the hypothesis.

## Separate facts from interpretation

Observed data and model judgments must remain visibly distinct.

## No forced quota

Return fewer opportunities, or none, when evidence does not justify them.

## Do not invent TAM

Market-size numbers, customer counts, growth rates, or revenue projections must come from evidence or be clearly labeled assumptions.

## Funding is not demand

Investment activity is evidence of market attention, not proof of customer willingness to pay.

---

# Production Prompt Architecture

The long-form research specification should **not** be executed verbatim every week.

Use three artifacts:

## 1. Master Research Specification

Long reference document containing:

- full sector definitions
- full source universe
- geographic definitions
- founder constraints
- exclusions
- evidence rules
- evaluation framework
- edge cases

Purpose:

**Reference manual / source of truth.**

---

## 2. Production Prompt

Compressed prompt used for the actual recurring run.

Recommended sections:

### ROLE

Define the venture-intelligence role and objective.

### SCOPE

Compact version of sectors, geography, founder constraints, and exclusions.

### CORE SCAN

The seven signal groups:

- Pain
- Manual Work
- Demand
- Technology Shift
- Catalyst
- Incumbent Weakness
- Startup / Market Activity

### DEEP DIVE TRIGGER

Explicit instruction not to investigate every signal fully.

### DEEP DIVE METHOD

Six questions:

1. Is the problem real and recurring?
2. Who experiences and buys against it?
3. How is it solved today?
4. Is there commercial evidence?
5. What remains unsolved?
6. What is the smallest feasible startup wedge?

### OUTPUT

- Research Summary
- Weekly Radar
- Qualified opportunities
- Watchlist
- Next Proof
- Research Coverage
- Sources

The Production Prompt should ideally be approximately **20–30% of the length of the Master Specification**.

---

## 3. Deep Dive Template

Separate template activated only for qualified candidates.

This keeps the routine weekly research lightweight while preserving the ability to perform serious investigation when needed.

---

# Interpretation Model

Use the following mental model when reading results:

## Core Scan = Radar Blips

Interesting observations.

They are **not startup ideas yet**.

## Deep Dive = Targets

Signals with enough evidence to justify investigation.

They are **not automatically good businesses**.

## Opportunity Log = Working Hypotheses

Structured hypotheses whose evidence changes over time.

## Customer Validation = Reality Check

Actual interviews, pilots, spending, design partners, or buying behavior are substantially stronger evidence than desk research.

The research system should ultimately help answer:

> **What should we investigate next?**

before attempting to answer:

> **What should we build?**

---

# Default Weekly Output

A production weekly report should generally contain:

## 1. Research Summary

3–7 concise bullets describing the most important changes.

## 2. Weekly Radar

Compact table of active opportunities and status changes.

## 3. New / Materially Changed Opportunities

Only opportunities where evidence changed meaningfully.

## 4. Watchlist

Interesting signals that do not yet justify a Deep Dive.

## 5. Next Proof Queue

The specific questions or evidence requests that should guide the next research cycle.

## 6. Research Coverage

- source types searched
- geographic coverage
- time period
- inaccessible sources
- material evidence gaps

---

# Guiding Principle

The system should optimize for:

**useful evidence, cumulative learning, and falsifiable opportunity hypotheses**

rather than:

**maximum number of trends, ideas, links, or artificial scores.**

The strongest pattern to search for is:

**Painful specialized problem**

**+ recurring manual work**

**+ identifiable buyer**

**+ observable spending**

**+ weak or incomplete existing solution**

**+ credible Why Now catalyst**

**+ small feasible wedge**

**+ accessible first customers**

**= opportunity worth validating**
