# Sprint 1 — Conversion (Baseline & Audit)

**Dates:** TODO (2 weeks) · **Status:** 🟢 Audit delivered (evidence-gathering) · **Phase:** 1 (Conversion)

> **Sprint 1 ran as an evidence-gathering & commercial-strategy sprint — no code, no store changes, nothing implemented.** Primary deliverable: the [Forensic Ecommerce Audit](../docs/18-forensic-ecommerce-audit.md), which produced the ranked [Opportunity Backlog](README.md). The live store could not be crawled (session egress policy denied `edgescarves.com`), so findings rest on cited public evidence + a documented [Evidence Required Register](../docs/18-forensic-ecommerce-audit.md#evidence-required-register-what-to-collect-why-how-it-changes-decisions). Implementation of any OPP item happens in later sprints, once baselines (E1–E3) exist.

## Objective

Establish trustworthy baselines and audit the store, then ship the first high-impact conversion fixes. By the end we should know our true conversion funnel and have improved at least the top conversion leak — moving toward the £2,000/month net-profit target.

## Business Justification

Conversion is the cheapest profit lever: it increases return on traffic we already pay for. Before scaling spend (Phase 2), the store must convert. This sprint also fixes the prerequisite for everything else — accurate tracking — so all later decisions rest on real data.

## Acceptance Criteria

- [ ] Tracking verified (GA4, Meta Pixel + Conversions API) and trustworthy.
- [ ] Baseline funnel + conversion metrics recorded in [`docs/14-kpis.md`](../docs/14-kpis.md).
- [ ] Full website audit completed with findings + screenshots ([`docs/06-website-audit.md`](../docs/06-website-audit.md)).
- [ ] Top 5–10 hypotheses written and ICE-scored ([`docs/07-conversion-rate-optimisation.md`](../docs/07-conversion-rate-optimisation.md)).
- [ ] At least one prioritised fix implemented (dev theme → tested → published) and its impact measured.
- [ ] Release notes + docs updated.

## Tasks

1. [ ] Verify analytics/tracking; fix any gaps. *(Data Analyst, Shopify Dev)*
2. [ ] Pull and record baseline funnel/conversion metrics. *(Data Analyst)*
3. [ ] Run the full website audit; capture screenshots. *(CRO, Shopify Dev)*
4. [ ] Prioritise findings by severity × impact. *(CRO)*
5. [ ] Write + ICE-score the hypothesis backlog. *(CRO)*
6. [ ] Spec and implement the top fix on a dev theme. *(CRO → Shopify Dev)*
7. [ ] Test (mobile, speed, a11y, tracking), publish, measure. *(Shopify Dev, Data Analyst)*
8. [ ] Document results + learnings; update release notes. *(PM)*

## Expected Business Impact

Higher conversion rate / AOV → more profit from existing traffic. Trustworthy data unlocks confident decisions. Quantify per the commercial model once baselines exist.

## KPIs Affected

Conversion rate, product-page conversion, checkout conversion, cart abandonment, AOV → net profit. ([`docs/14-kpis.md`](../docs/14-kpis.md))

## Dependencies

- Access: Shopify admin, GA4, Meta ad account.
- Sprint 0 foundation complete.
- A testing tool / heatmap tool selected (TODO).

## Release Notes

> Complete at sprint end → [`docs/17-release-notes.md`](../docs/17-release-notes.md).

## Retrospective

> Complete at sprint end. What went well / didn't / learned / next.

---
**Owner:** CRO Specialist prompt / Project Manager prompt · **Last Updated:** 2026-06-29
