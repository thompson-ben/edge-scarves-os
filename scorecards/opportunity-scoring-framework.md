# Opportunity Scoring Framework

## Purpose

A single, consistent way to score and **rank every backlog item and feature request by commercial value before any work begins**. It forces decisions to be commercially driven, not technically driven: we build the highest-value, lowest-cost opportunities first. No backlog item is implemented until it has been scored and ranked against the alternatives.

> This is the standard for **features and backlog items**. For rapid triage of small CRO test ideas, lightweight ICE scoring ([`docs/07-conversion-rate-optimisation.md`](../docs/07-conversion-rate-optimisation.md)) is acceptable, but anything entering a sprint is scored here.

## The seven factors

Score each factor **1–10**. Be honest and evidence-based; where you are guessing, say so and lower confidence.

**Value factors** (higher = more attractive):

| Factor | Question | 1 = | 10 = |
|---|---|---|---|
| **Revenue Impact** | How much could this grow top-line revenue? | Negligible | Transformational |
| **Profit Impact** | How much could this grow **net profit**? | Negligible | Transformational |
| **Conversion Impact** | How much could this lift conversion rate / AOV? | None | Major uplift |
| **Customer Experience Impact** | How much better is the customer's experience? | No change | Significantly better |
| **Strategic Value** | How much does this build a lasting asset (brand, data, capability, moat)? | None | Core to the long game |

**Cost factors** (higher = less attractive):

| Factor | Question | 1 = | 10 = |
|---|---|---|---|
| **Effort** | How much work/time/money to deliver? | Trivial | Very large |
| **Risk** | How likely to fail, harm brand, or be hard to reverse? | Safe & reversible | High / irreversible |

## The score

Two intermediate indices, then one ranking number.

**1. Value Index** — a weighted average of the five value factors. Weights are profit-first (per the [North Star](../docs/00-north-star.md) decision framework):

| Factor | Weight |
|---|---|
| Profit Impact | 30% |
| Revenue Impact | 20% |
| Conversion Impact | 20% |
| Strategic Value | 15% |
| Customer Experience Impact | 15% |

```
Value Index = 0.30·Profit + 0.20·Revenue + 0.20·Conversion + 0.15·Strategic + 0.15·CX
```
(Result is on a 1–10 scale.)

**2. Cost Index** — the average of the two cost factors:
```
Cost Index = (Effort + Risk) / 2
```
(Result is on a 1–10 scale.)

**3. Opportunity Score** — value earned per unit of cost, scaled to a readable number:
```
Opportunity Score = (Value Index / Cost Index) × 10
```

- **Higher is better.** Range ≈ **1 to 100**.
- A high-value, low-cost item scores high; a high-value but heavy/risky item is penalised — exactly the commercial bias we want.

### Bands (guideline)
| Score | Band | Action |
|---|---|---|
| **≥ 40** | 🟢 Strong | Prioritise — top of backlog |
| **20–39** | 🟡 Moderate | Schedule when capacity allows |
| **10–19** | 🟠 Weak | Defer / needs reshaping to reduce cost or raise value |
| **< 10** | 🔴 Poor | Reject unless strategically mandated |

> Bands are guidance, not gates. The **rank order** is what governs the backlog. Profit Impact also carries an implicit veto: an item scoring very low on Profit Impact should be challenged by the CEO prompt regardless of total score.

## Worked example

> "Add abandoned-cart email flow." Scores: Revenue 6, **Profit 7**, Conversion 6, CX 6, Strategic 7 · Effort 3, Risk 2.

```
Value Index = 0.30·7 + 0.20·6 + 0.20·6 + 0.15·7 + 0.15·6
            = 2.10 + 1.20 + 1.20 + 1.05 + 0.90 = 6.45
Cost Index  = (3 + 2) / 2 = 2.5
Opportunity Score = (6.45 / 2.5) × 10 = 25.8  → 🟡 Moderate, but high value-for-effort
```

> "Full custom homepage rebuild." Scores: Revenue 7, **Profit 4**, Conversion 5, CX 7, Strategic 6 · Effort 9, Risk 7.
```
Value Index = 0.30·4 + 0.20·7 + 0.20·5 + 0.15·6 + 0.15·7 = 1.20+1.40+1.00+0.90+1.05 = 5.55
Cost Index  = (9 + 7) / 2 = 8
Opportunity Score = (5.55 / 8) × 10 = 6.9 → 🔴 Poor — defer/reshape despite looking exciting
```

The framework correctly favours the cheap, profit-driving email flow over the expensive, risky rebuild — commercially driven, not technically driven.

## How to use it

1. Score every feature request ([`templates/feature-request.md`](../templates/feature-request.md) has the table built in).
2. Record the score on the item and in the ranked backlog ([`backlog/README.md`](../backlog/README.md)).
3. **Rank the whole backlog by Opportunity Score before committing a sprint.** PM owns the ranking; CEO prompt sanity-checks Profit Impact.
4. Re-score if assumptions change (e.g. new data lowers Effort or raises Profit Impact).

## Dependencies

- [`docs/00-north-star.md`](../docs/00-north-star.md) (decision framework), [`docs/00-business-principles.md`](../docs/00-business-principles.md) (principles 2, 3, 11).
- [`templates/feature-request.md`](../templates/feature-request.md) — where scoring is captured.
- [`backlog/README.md`](../backlog/README.md) — the ranked backlog.

## Open Questions

- Should weights be tuned once we have real profit data (e.g. raise Profit weight further)?
- Do we want a minimum Profit-Impact threshold as a hard gate (not just CEO challenge)?

## Action Items

- [ ] Apply the framework to all existing backlog items.
- [ ] Maintain the ranked backlog index in `backlog/README.md`.
- [ ] Revisit weights once real commercial data exists.

---

**Status:** 🟢 Active
**Last Updated:** 2026-06-29
**Owner:** Project Manager prompt / CEO prompt
