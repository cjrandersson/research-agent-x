# Sändeman Signal Engine

> Purpose: rank weak signals without turning internal model scores into false public precision.

## Principle

The engine should discard most raw observations before expensive reasoning occurs.

The goal is not to claim that "99% of false positives" are removed. Performance must be measured empirically with historical benchmarks.

Primary benchmark metrics:

- Precision@K
- Recall
- Mean / median useful lead time
- False escalation rate
- Signal stability
- Independent evidence-root count

## Internal signal vector

Each SignalCluster receives an internal feature vector.

```text
A = Anomaly
V = Velocity
X = Cross-source independence / convergence
P = Persistence
N = Novelty
C = Commercial evidence
Q = Source quality
M = Attention saturation
D = Dependency / noise penalty
```

All features should be normalized to comparable ranges where practical.

Example internal representation:

```json
{
  "anomaly": 0.81,
  "velocity": 0.76,
  "cross_source": 0.91,
  "persistence": 0.58,
  "novelty": 0.72,
  "commercial": 0.44,
  "source_quality": 0.83,
  "attention_saturation": 0.19,
  "noise_penalty": 0.08
}
```

## Feature definitions

### A — Anomaly
How unusual is the current observation/event level compared with the entity/topic historical baseline?

Use robust statistics where possible, for example median/MAD rather than relying only on mean/standard deviation.

### V — Velocity
Measures acceleration, not absolute popularity.

`5 → 8 → 17 → 41` may be more interesting than `500 → 510 → 520`.

### X — Cross-source independence
Measures support from genuinely independent evidence roots and source families.

Five derivative articles from one filing do not equal five independent confirmations.

### P — Persistence
Rewards signals that remain present or strengthen across multiple time windows.

### N — Novelty
Measures distance from existing historical clusters. Novelty alone is weak; novelty combined with velocity and independent confirmation is stronger.

### C — Commercial evidence
Measures evidence that attention is becoming expenditure or operational commitment.

Indicative progression:

```text
mention                 very weak
social discussion       weak
open-source experiment  weak-medium
job posting              medium
repeated customer pain   medium
vendor evaluation        medium-high
RFP / procurement        high
contract / budget        very high
```

Exact values must be calibrated with benchmarks rather than treated as universal truth.

### Q — Source quality
Represents source reliability for the specific claim type.

Source quality is contextual. An official filing may be excellent for financing facts; a practitioner forum may be better for discovering workflow pain.

### M — Attention Saturation
Estimates how visible/established the signal already is.

Possible components:

- major-media volume
- search volume
- social mention volume
- analyst/report coverage
- funding-news coverage
- incumbent/vendor density

Peripheral targets are generally stronger when evidence is high and attention saturation remains low.

### D — Dependency / noise penalty
Penalizes:

- duplicates
- syndication
- obvious marketing content
- bot activity
- single-origin evidence
- hype without operational/commercial evidence

## Funnel

Canonical escalation:

```text
RAW DOCUMENT
   ↓
OBSERVATION
   ↓
EVENT
   ↓
SIGNAL CLUSTER
   ↓
CORE SCAN CANDIDATE
   ↓
DEEP DIVE
   ↓
HYPOTHESIS / OPPORTUNITY
```

Thresholds should initially be configurable and benchmark-driven rather than hard-coded as permanent truth.

## User-facing presentation

Do not expose unexplained decimals such as `87.3 / 100` as if they represent objective truth.

Prefer interpretable output:

```text
SIGNAL STRENGTH       HIGH
VELOCITY              ACCELERATING
SOURCE DIVERSITY      HIGH
COMMERCIAL PROOF      MEDIUM
PUBLIC ATTENTION      LOW
CONFIDENCE            EMERGING
```

The numeric vector remains available internally for sorting, testing and calibration.

## Next Proof

Every escalated signal should state the highest-value missing evidence.

Example:

```text
WHAT CHANGED
Hiring velocity increased across three independent companies.

WHAT WE KNOW
Four independent evidence roots support the cluster.

WHAT WE DON'T KNOW
No procurement or enterprise deployment evidence yet.

COUNTERSIGNAL
A major incumbent introduced overlapping functionality.

NEXT PROOF
Find explicit purchasing, deployment or budget evidence.
```

The engine should optimize for falsifiable progress, not excitement.
