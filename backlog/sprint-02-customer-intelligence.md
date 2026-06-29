# Sprint 2 — Revenue Readiness: Customer Intelligence

**Dates:** 2026-06-29 (planning) · **Status:** 🟢 Designed (documentation & planning only) · **Phase:** 1→2 (Revenue Readiness)

> **Documentation and planning only. No Shopify changes, no implementation.** This sprint *designs* the customer-intelligence system that future sprints will build.

## Objective

Create the **Customer Intelligence** strategic workstream: understand **who buys, why they buy, and what drives repeat purchase** — and design the system that captures, structures and acts on that understanding over time.

## Business Justification

Every high-value opportunity in the [Forensic Audit](../docs/18-forensic-ecommerce-audit.md) — gifting positioning (SH-01), the gift-giver persona (SH-03), AOV, retention, targeting — depends on customer insight we do not yet have. Building the intelligence lens *before* optimising the store ensures decisions are evidence-led, not guessed. CI is the mechanism that turns the [evidence standard](../docs/19-evidence-standards.md) into validated strategy and a prioritised backlog. It is the prerequisite for profitable revenue growth toward £2k → £10k/month net.

## Acceptance Criteria

- [x] **Customer Intelligence Strategy** documenting every insight source (Shopify orders, post-purchase surveys, email, reviews, support, Meta comments, social). → [`docs/20`](../docs/20-customer-intelligence.md#deliverable-1--customer-intelligence-strategy-sources-of-insight)
- [x] **Customer Intelligence Database** schema (incl. purchase reason, recipient, occasion, gift wrapped, repeat customer, discovery source, favourite products, review sentiment, lifetime spend, customer segment). → [`schemas/`](../schemas)
- [x] **Insight Pipeline** defined: Evidence → Structured data → Insights → Strategic decisions → Sprint backlog. → [`docs/20`](../docs/20-customer-intelligence.md#deliverable-3--the-insight-pipeline)
- [x] **New KPIs** defined (gift %, self %, repeat %, avg gifts/customer, occasion mix, review sentiment, gift-wrap adoption). → [`docs/14`](../docs/14-kpis.md#customer-intelligence-dashboard)
- [x] **Future AI Vision** designed (recommendations, emails, audiences, bundles, demand forecasting, merchandising). → [`docs/20`](../docs/20-customer-intelligence.md#deliverable-5--future-ai-vision)
- [x] Data governance/privacy approach documented.
- [x] No Shopify store changes.

## Tasks

1. [x] Write the CI strategy + insight sources (S1–S7).
2. [x] Design the database schema (data dictionary + JSON Schema).
3. [x] Define the insight pipeline and its OS ownership/cadence.
4. [x] Define and add the 7 new KPIs to the dashboards.
5. [x] Design the future AI vision (inputs → output → gate → maturity).
6. [x] Document privacy/governance.
7. [x] Cross-link AI strategy, KPIs, audit hypotheses; commit & push.
8. [ ] (Next) Founder confirms tooling + privacy approach; stand up the post-purchase survey.

## Expected Business Impact

No direct revenue impact (design sprint). Unlocks evidence-led validation of the gifting thesis and retention strategy — the foundation for profitable revenue growth. Reduces risk of optimising the store around an unvalidated persona.

## KPIs Affected

Introduces the Customer Intelligence dashboard ([`docs/14`](../docs/14-kpis.md#customer-intelligence-dashboard)); indirectly enables movement of conversion, AOV, repeat % and net profit once acted upon.

## Dependencies

- [`docs/19-evidence-standards.md`](../docs/19-evidence-standards.md), [`/evidence`](../evidence), [`docs/18`](../docs/18-forensic-ecommerce-audit.md) (hypotheses).
- To build: survey tool, reviews app, ESP, support system, a starter data store (Evidence Required — confirm current tooling).
- Founder decision on privacy/consent approach.

## Release Notes

See [`docs/17-release-notes.md`](../docs/17-release-notes.md) → **v0.5 — Customer Intelligence**.

## Retrospective

- **What went well:** CI system designed end-to-end and wired into the evidence loop; directly validates SH-01/SH-03; schema is implementation-ready and privacy-aware.
- **What didn't:** TODO (pending founder review of tooling/privacy).
- **What we learned:** TODO.
- **Actions for next sprint:** stand up the post-purchase survey first; begin baselining CI KPIs as data arrives.

---
**Owner:** Data Analyst prompt / Project Manager prompt · **Last Updated:** 2026-06-29
