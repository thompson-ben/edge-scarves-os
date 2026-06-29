# 20 — Customer Intelligence

## Purpose

The strategy and system for understanding **who buys Edge Scarves, why they buy, and what drives repeat purchase** — and for turning that understanding into evidence-backed commercial decisions over time. Customer Intelligence (CI) is the engine that converts scattered signals (orders, surveys, reviews, support, social) into structured data, then into validated insight, then into a prioritised backlog. It is how the business will **validate its Strategic Hypotheses** (e.g. SH-01 "this is a gifting business", SH-03 "the buyer is the gift-giver") instead of guessing.

> **Scope:** documentation and planning only. No Shopify changes, no implementation. This sprint *designs* the intelligence system that future sprints will build.

> **Why this comes before website improvements:** every high-value recommendation in the [Forensic Audit](18-forensic-ecommerce-audit.md) — gifting positioning, AOV, retention, targeting — depends on knowing the gift-vs-self split, occasions and motivations. Build the lens before optimising the picture.

---

## Deliverable 1 — Customer Intelligence Strategy: sources of insight

Every place a customer reveals something about who they are and why they buy. Each source is mapped to: what it tells us, how it's captured, the [evidence tier](19-evidence-standards.md) it produces, and where it lands in [`/evidence`](../evidence).

| # | Source | What it reveals | Capture method | Evidence tier | Lands in |
|---|---|---|---|---|---|
| S1 | **Shopify order attributes** | What/when/how much, gift-wrap, ship-to ≠ bill-to (gift signal), discount used, channel, repeat | Shopify Admin / API export | `[FACT]` | `evidence/analytics` |
| S2 | **Post-purchase survey** | *Purchase reason, recipient, occasion, gift-or-self, discovery source* — the highest-value unknowns | On-site / email survey after purchase | `[FACT]` (self-reported) | `evidence/customer-feedback` |
| S3 | **Email responses & engagement** | Interests, occasion timing, what content resonates, replies | ESP data + reply monitoring | `[FACT]`/`[INFERENCE]` | `evidence/emails` |
| S4 | **Product reviews** | Satisfaction, sentiment, gifting language, objections, product favourites | Reviews app / Trustpilot export | `[FACT]` (text) → `[INFERENCE]` (sentiment) | `evidence/customer-feedback` |
| S5 | **Customer support** | Objections, anxieties, delivery/gift concerns, FAQs | Support inbox / helpdesk tags | `[FACT]`/`[INFERENCE]` | `evidence/customer-feedback` |
| S6 | **Meta comments / DMs** | Sentiment, questions, gift intent, audience language | Meta inbox / social listening | `[FACT]`/`[INFERENCE]` | `evidence/customer-feedback` |
| S7 | **Social engagement** | What resonates (saves, shares, clicks), audience interests | IG/FB/Pinterest insights | `[INFERENCE]` | `evidence/competitors`/feedback |

**Source principles**
- **S2 (post-purchase survey) is the priority build** — it is the only source that directly answers *gift-vs-self, occasion and motivation*, validating SH-01/SH-03. It is also the cheapest to stand up.
- Triangulate: a claim is strongest when ≥2 sources agree (e.g. survey says "gift" + order shows ship-to ≠ bill-to + review uses gifting language).
- Self-reported data (surveys) is a `[FACT]` about *what they said*, an `[INFERENCE]` about *what they do* — label accordingly.

---

## Deliverable 2 — Customer Intelligence Database

The schema design lives in [`schemas/customer-intelligence-schema.md`](../schemas/customer-intelligence-schema.md) (human-readable data dictionary) and [`schemas/customer-profile.schema.json`](../schemas/customer-profile.schema.json) (machine-readable). Summary of the model:

- **`customer`** — one record per person: identity (pseudonymous ID), segment, lifetime spend, order count, repeat flag, first-touch discovery source, favourite products, consent flags, region.
- **`order`** — one per order: value, date, gift-wrapped, gift-or-self, products, channel, discount.
- **`insight_event`** — survey/support/social responses: purchase reason, recipient, occasion, source, timestamp.
- **`review`** — product, rating, sentiment, text.

Derived fields (e.g. repeat customer, lifetime spend, average gifts per customer, segment) are **computed**, not entered, and trace back to source records — preserving evidence traceability. Full field-by-field definitions, allowed values, sources and privacy classes are in the schema file.

---

## Deliverable 3 — The Insight Pipeline

How a raw signal becomes a strategic decision and, ultimately, a backlog item. This **closes the OS loop** and operationalises the [evidence standard](19-evidence-standards.md).

```
   EVIDENCE                STRUCTURED DATA            INSIGHTS                STRATEGIC DECISIONS         SPRINT BACKLOG
   (raw signal)      →     (the CI database)     →    (analysis)        →     (validated direction)  →    (scored work)
   /evidence + S1–S7       schema / profiles          Data Analyst +          Hypotheses validated/       OPP items in
   reviews, orders,        (facts, tagged,            dashboards turn         rejected; North Star        backlog/README,
   surveys, support        traceable)                 data into "so what"     & decisions updated         ranked by Opp. Score
```

| Stage | What happens | Owner | Lives in |
|---|---|---|---|
| **1. Evidence** | Capture raw signals from S1–S7; store with source + date | Data Analyst / Founder | [`/evidence`](../evidence) |
| **2. Structured data** | Normalise into the CI schema; classify & tag; derive fields | Data Analyst | [`schemas/`](../schemas) (model) → CI database (future build) |
| **3. Insights** | Analyse: segments, gift-vs-self, occasion mix, sentiment, LTV; produce "so what" | Data Analyst | [`docs/14-kpis.md`](14-kpis.md) dashboards + analysis notes |
| **4. Strategic decisions** | Validate/reject [Strategic Hypotheses](18-forensic-ecommerce-audit.md#strategic-hypotheses-register); update direction | CEO / Founder | [`00-north-star.md`](00-north-star.md), hypotheses register |
| **5. Sprint backlog** | Turn validated decisions into scored [feature requests](../templates/feature-request.md), ranked | Project Manager | [`backlog/README.md`](../backlog/README.md) |

**Cadence:** insights reviewed monthly (with the [Business Health](../scorecards/business-health-scorecard.md) and Marketing scorecards); hypotheses re-graded as evidence accrues; the audit ([living doc](18-forensic-ecommerce-audit.md)) updated in step.

---

## Deliverable 4 — New KPIs

Seven CI KPIs are defined in full (definition, source, target) in [`docs/14-kpis.md`](14-kpis.md#customer-intelligence-dashboard): **Gift purchase %, Self purchase %, Repeat purchase %, Average gifts per customer, Occasion mix, Review sentiment, Gift-wrap (gift-option) adoption.** These directly measure the gifting thesis and retention — the levers behind the £2k → £10k/month net-profit goal. (See doc 14 for the nuance on "gift-wrap adoption" given wrapping is currently standard.)

---

## Deliverable 5 — Future AI Vision

How AI should *eventually* use this intelligence — once the data exists and is trustworthy. AI is the leverage that lets a lean team act on intelligence at scale; the CI database is its fuel. Each capability maps to the data it needs, its output, the human-approval gate, and a maturity stage.

| AI capability | Data inputs (from schema) | Output | Human gate | Maturity |
|---|---|---|---|---|
| **Product recommendations** | favourite_products, segment, co-purchase, occasion | Personalised PDP/email/cart recs | Auto (monitored) | 🚶 Walk |
| **Email generation** | occasion, recipient, purchase_reason, segment, last_order | Occasion-triggered, personalised emails (e.g. "Mum's birthday is near — gift again") | Approve before send | 🐢 Crawl→Walk |
| **Meta audience suggestions** | high-LTV gifting segments, discovery_source, occasion | Seed/lookalike audience definitions | Approve before spend | 🚶 Walk |
| **Bundle identification** | co-purchase patterns, occasion, gift-or-self | Proposed gift sets/bundles (→ scored OPP) | PM/CEO review | 🚶 Walk |
| **Seasonal demand prediction** | occasion_mix, order time-series, product velocity | Stock & campaign forecasts by occasion | Founder review | 🏃 Run |
| **Merchandising recommendations** | segment × occasion, sentiment, velocity | Collection ordering / homepage rotation suggestions | CRO review | 🏃 Run |

**AI governance (per [`13-ai-strategy.md`](13-ai-strategy.md)):** human-in-the-loop for anything outward-facing (sends, spend, live merchandising); AI proposes, humans dispose; every AI output is measured against KPIs; privacy rules below apply to all training/inference data. **Sequence:** crawl (assist analysis & drafting) → walk (recommend with approval) → run (predict & automate within guardrails). We do not automate what we cannot yet measure.

---

## Data governance & privacy (non-negotiable)

Edge Scarves is a UK business handling personal data — CI must be lawful and trustworthy or it erodes the very customer trust it studies.

- **Lawful basis & consent:** collect survey/marketing data with clear consent; honour opt-outs.
- **Data minimisation:** capture only what informs a decision; avoid storing sensitive data.
- **Pseudonymisation:** use a customer ID; redact names/emails/addresses in evidence files and analysis ([`/evidence`](../evidence) rules).
- **Retention & access:** define retention periods; limit access; secure exports.
- **Right to erasure / portability:** the schema must support deleting a customer's records on request.
- **No dark patterns:** surveys and capture are honest and optional.

> Governance is a `[RECOMMENDATION]` to confirm with the founder (and, if needed, a data-protection check) before any customer data is collected at scale.

---

## Future Vision

A living customer-intelligence system where every order, review and survey response compounds into a sharper picture of the customer. The business knows its gift-vs-self split, its occasion calendar, its best segments and its repeat drivers — and AI turns that knowledge into personalised recommendations, emails, audiences, bundles and forecasts. Strategy stops being opinion and becomes a continuously-updated, evidence-backed model of the customer. This is the foundation of the AI-native company.

## Dependencies

- [`19-evidence-standards.md`](19-evidence-standards.md) (classification) · [`/evidence`](../evidence) (raw) · [`schemas/`](../schemas) (model).
- [`14-kpis.md`](14-kpis.md) (KPIs/dashboards) · [`13-ai-strategy.md`](13-ai-strategy.md) (AI governance).
- [`18-forensic-ecommerce-audit.md`](18-forensic-ecommerce-audit.md) (hypotheses this validates) · [`03-customer-persona.md`](03-customer-persona.md) (persona this evidences).
- Tools (future): post-purchase survey tool, reviews app, ESP, support helpdesk, a data store (Evidence Required — select later).

## Open Questions

- Which survey tool, reviews app, ESP and support system are in use today? (Evidence Required.)
- Is gift wrap always-on (standard) or selectable? (Determines the gift-wrap KPI definition.)
- Where will the CI database physically live (Shopify metafields, a sheet, a lightweight DB, a warehouse)? Start simple, design for scale.
- What is the lawful basis and consent mechanism for survey data?

## Action Items

- [ ] Stand up the **post-purchase survey** (S2) first — it validates SH-01/SH-03 and seeds the highest-value fields.
- [ ] Confirm current tooling (survey/reviews/ESP/support) and pick a starter data store.
- [ ] Finalise the schema with the founder; confirm gift-wrap definition.
- [ ] Confirm privacy/consent approach before collecting at scale.
- [ ] Add CI KPIs to the dashboards and begin baselining as data arrives.

---

**Status:** 🟢 Designed (planning only) — ready to build when tooling is confirmed
**Last Updated:** 2026-06-29
**Owner:** Data Analyst prompt / CEO prompt
