# 06 — Website Audit

## Purpose

A structured, repeatable assessment of the Shopify storefront — what works, what leaks conversion, and what to fix in priority order. The audit is the evidence base for the CRO backlog. It is a living checklist, not a one-off report.

> ⚠️ This document **records observations and recommendations only**. It does not authorise changes to the live store. Fixes are scheduled through sprints (see [`backlog/`](../backlog)).

## Current State

> No audit performed yet. The framework below is ready to be filled with findings + screenshots (store evidence belongs in [`/screenshots`](../screenshots)).

**Audit framework**

| Area | What to check | Finding | Severity | Screenshot |
|---|---|---|---|---|
| Homepage | Clear value prop, hero, navigation, trust | TODO | — | — |
| Collection pages | Filtering, merchandising, load speed | TODO | — | — |
| Product pages | Imagery, copy, price clarity, reviews, CTA, delivery/returns info | TODO | — | — |
| Cart | Friction, upsells, trust, shipping clarity | TODO | — | — |
| Checkout | Steps, payment options, abandonment causes | TODO | — | — |
| Mobile experience | Mobile-first quality (majority of traffic) | TODO | — | — |
| Speed / Core Web Vitals | LCP, CLS, INP | TODO | — | — |
| Trust signals | Reviews, guarantees, returns, security, social proof | TODO | — | — |
| Navigation & IA | Findability, menu structure, search | TODO | — | — |
| Accessibility | Contrast, alt text, keyboard, semantics | TODO | — | — |
| SEO basics | Titles, meta, headings, structured data | TODO | — | — |
| Analytics/tracking | GA4, pixels, events firing correctly | TODO | — | — |

**Severity scale:** 🔴 Critical (blocks/heavily leaks conversion) · 🟠 Major · 🟡 Minor · 🟢 Polish.

**Current theme:** TODO (name/version) — see [`12-shopify-architecture.md`](12-shopify-architecture.md).

## Future Vision

A high-converting, fast, accessible, mobile-first store with no critical conversion leaks. The audit is re-run each quarter and after major changes, with findings tracked to closure through CRO sprints. Every fix is measured against the conversion KPIs.

## Dependencies

- [`07-conversion-rate-optimisation.md`](07-conversion-rate-optimisation.md) — turns findings into tested fixes.
- [`12-shopify-architecture.md`](12-shopify-architecture.md) — the technical context for fixes.
- [`14-kpis.md`](14-kpis.md) — conversion metrics the audit aims to move.
- Tools: GA4, Shopify analytics, PageSpeed/Lighthouse, heatmaps/session recordings (TODO confirm tooling).

## Open Questions

- What is the current sitewide and product-page conversion rate?
- Where do customers actually drop off (funnel data)?
- What is mobile vs. desktop traffic and conversion split?
- Are analytics/events firing correctly (can we trust the data)?

## Action Items

- [ ] Verify analytics/tracking before drawing conclusions.
- [ ] Capture baseline funnel and conversion data.
- [ ] Run the full audit and record findings + screenshots.
- [ ] Prioritise findings by severity × conversion impact.
- [ ] Feed top issues into [`backlog/sprint-01-conversion.md`](../backlog/sprint-01-conversion.md).

---

**Status:** 🔴 Not started — audit pending (do not change store yet)
**Last Updated:** 2026-06-29
**Owner:** CRO Specialist prompt / Shopify Developer prompt
