# 14 — KPIs & Dashboards

## Purpose

The single definition of every metric Edge Scarves tracks, the targets for each, and the dashboards that make performance visible. No work is "Done" without a measurable impact on one of these KPIs. This document is how the business knows whether it is winning.

## Current State

> All baselines and targets are `TODO` until real data is loaded. Definitions are fixed; numbers are pending. Do not invent figures.

**Reporting cadence:** weekly (operational, see [`templates/weekly-review.md`](../templates/weekly-review.md)) and monthly (commercial, P&L vs. model in [`04-commercial-analysis.md`](04-commercial-analysis.md)).

**North-star metric:** **Monthly net profit** (Phase 1 target £2,000; long term £10,000+).

---

### Commercial dashboard
| KPI | Definition | Baseline | Target | Source |
|---|---|---|---|---|
| Revenue | Total sales (net of refunds) | TODO | TODO | Shopify |
| Net profit | Revenue − all costs | TODO | £2,000/mo (P1) | Accounts |
| Orders | Completed orders | TODO | TODO | Shopify |
| Average order value (AOV) | Revenue ÷ orders | TODO | TODO | Shopify |
| Conversion rate | Orders ÷ sessions | TODO | TODO | Shopify/GA4 |
| Returning customer % | Repeat customers ÷ total | TODO | TODO | Shopify |
| Gross margin % | (Revenue − COGS) ÷ revenue | TODO | TODO | Accounts |

### Marketing dashboard
| KPI | Definition | Baseline | Target | Source |
|---|---|---|---|---|
| ROAS | Revenue ÷ ad spend | TODO | ≥ break-even | Meta/GA4 |
| CPA | Ad spend ÷ acquisitions | TODO | TODO | Meta |
| CTR | Clicks ÷ impressions | TODO | TODO | Meta |
| CPC | Spend ÷ clicks | TODO | TODO | Meta |
| CPM | Spend ÷ (impressions/1000) | TODO | TODO | Meta |
| Email revenue | Revenue attributed to email | TODO | TODO | ESP/Shopify |

### Website dashboard
| KPI | Definition | Baseline | Target | Source |
|---|---|---|---|---|
| Sessions | Store visits | TODO | TODO | GA4 |
| Product conversion | Product-page → purchase | TODO | TODO | GA4/Shopify |
| Homepage conversion | Homepage → onward engagement/purchase | TODO | TODO | GA4 |
| Checkout conversion | Checkout-started → completed | TODO | TODO | Shopify |
| Cart abandonment | 1 − (purchases ÷ carts) | TODO | TODO | Shopify |

### Customer Intelligence dashboard

> Introduced in [Sprint 2 — Customer Intelligence](20-customer-intelligence.md). These measure *who buys and why* — the evidence behind the gifting thesis (SH-01/SH-03) and retention. Sourced from the [CI schema](../schemas/customer-intelligence-schema.md); baselines pending the post-purchase survey + order analysis.

| KPI | Definition | Baseline | Target | Source |
|---|---|---|---|---|
| Gift purchase % | Gift orders ÷ total orders | TODO | TODO | Survey + order signals |
| Self purchase % | Self orders ÷ total orders | TODO | TODO | Survey + order signals |
| Repeat purchase % | Customers with ≥2 orders ÷ total customers | TODO | TODO | Shopify/CI |
| Average gifts per customer | Gift orders ÷ customers | TODO | TODO | CI |
| Occasion mix | Distribution of stated occasions | TODO | n/a (monitor) | Survey |
| Review sentiment | % positive reviews (or mean score) | TODO | TODO | Reviews/Trustpilot |
| Gift-wrap (option) adoption | Orders using gift options (message/recipient) ÷ orders | TODO | TODO | Shopify/CI |

> **Note on "gift-wrap adoption":** wrapping is currently *standard*, so the decision-useful metric is **gift-option adoption** (gift message / recipient address). Confirm whether wrap is always-on or selectable before finalising the target.

### Operations dashboard
| KPI | Definition | Baseline | Target | Source |
|---|---|---|---|---|
| Stock | Units / weeks of cover | TODO | TODO | Shopify |
| Refunds | Refund rate & value | TODO | TODO | Shopify |
| Reviews | Volume & average rating | TODO | TODO | Reviews app |
| Support | Tickets, response/resolution time | TODO | TODO | Support tool |

---

## Future Vision

A live, trusted dashboard suite (commercial, marketing, website, operations) reviewed on a fixed cadence. Every metric has a definition, baseline, target and owner. Trends are visible, anomalies are caught early, and every sprint's impact is read directly off these dashboards. The north-star — monthly net profit — is always one glance away.

## Dependencies

- [`04-commercial-analysis.md`](04-commercial-analysis.md) — commercial targets/model.
- Every channel doc (08–11) — channel metrics.
- Data sources: Shopify, GA4, Meta, ESP, reviews/support tools. (TODO confirm access + reliability.)

## Open Questions

- Is tracking accurate enough to trust these numbers? (Verify before reporting.)
- Where will dashboards live (Shopify, GA4, a sheet, a BI tool)?
- What are the realistic Phase 1 targets per metric (derived from the model)?
- Who owns updating each dashboard and when?

## Action Items

- [ ] Verify data accuracy across all sources.
- [ ] Load baselines for every KPI.
- [ ] Derive Phase 1 targets from the commercial model.
- [ ] Choose where dashboards live and build them.
- [ ] Assign an owner and cadence to each dashboard.

---

**Status:** 🟡 Draft — definitions set, baselines/targets pending
**Last Updated:** 2026-06-29
**Owner:** Data Analyst prompt
