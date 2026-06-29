# 07 — Conversion Rate Optimisation (CRO)

## Purpose

Turn website-audit findings into a disciplined programme of prioritised, measurable improvements to the store's conversion rate and AOV. CRO is the cheapest growth lever we have: improving conversion lifts profit from traffic we already pay for. This document owns the hypothesis backlog, the testing method, and the results log.

## Current State

> No tests run yet. Framework ready.

**Prioritisation model:** ICE (Impact × Confidence × Ease), each 1–10. Backlog is ranked by ICE score.

**Hypothesis backlog**
| ID | Hypothesis ("If we… then… because…") | Page | Impact | Confidence | Ease | ICE | Status |
|---|---|---|---|---|---|---|---|
| CRO-001 | TODO | TODO | — | — | — | — | Backlog |

**Testing method**
- Prefer A/B tests where traffic allows statistical significance.
- Where traffic is too low for A/B, use before/after with guardrails + qualitative evidence, and accept lower certainty.
- Define success metric and minimum sample/duration **before** launching.
- One change per test where possible; document confounders.

**Results log**
| ID | Change | Metric | Before | After | Result | Decision |
|---|---|---|---|---|---|---|
| — | — | — | — | — | — | — |

**Key conversion metrics (baseline TODO):** sitewide CR, product-page CR, add-to-cart rate, cart→checkout, checkout completion, AOV, cart abandonment. See [`14-kpis.md`](14-kpis.md).

## Future Vision

A continuous CRO loop: audit → hypothesise → prioritise (ICE) → test → measure → ship or kill → document. Conversion rate and AOV climb steadily and measurably, increasing profit per session. Every winning change is recorded so learnings compound and are not re-discovered.

## Dependencies

- [`06-website-audit.md`](06-website-audit.md) — source of hypotheses.
- [`03-customer-persona.md`](03-customer-persona.md) — objections to address.
- [`12-shopify-architecture.md`](12-shopify-architecture.md) — how changes are implemented safely.
- [`14-kpis.md`](14-kpis.md) — metrics moved.
- Tooling: A/B testing app, heatmaps/recordings, GA4 (TODO confirm).

## Open Questions

- Is traffic high enough for statistically valid A/B tests? If not, what is our evidence standard?
- What are the current baseline conversion metrics?
- What are the top 3 conversion leaks from the audit?
- Which testing tool fits a premium Shopify store on our budget?

## Action Items

- [ ] Establish baseline conversion metrics (depends on audit + analytics).
- [ ] Select and document a testing tool and evidence standard.
- [ ] Write the first 5–10 hypotheses from audit findings, ICE-scored.
- [ ] Define the standard test template (metric, sample, duration, guardrails).
- [ ] Run the first test in [`backlog/sprint-01-conversion.md`](../backlog/sprint-01-conversion.md).

---

**Status:** 🟡 Draft — framework ready, no tests yet
**Last Updated:** 2026-06-29
**Owner:** CRO Specialist prompt
