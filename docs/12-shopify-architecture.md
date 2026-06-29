# 12 — Shopify Architecture

## Purpose

Document how the Shopify store is technically built and configured, so that any change is made safely, reversibly and consistently. This is the engineering reference for the Shopify Developer. It captures the theme, apps, integrations, data model and the safe workflow for making changes.

> ⚠️ This document **describes and plans**. It does not authorise live changes during foundation work. Store changes happen only through authorised sprints, on a duplicated/dev theme first.

## Current State

> Populate from the real store. Do not invent versions or app lists.

**Theme**
- Theme name & version: TODO
- Theme type: Online Store 2.0? TODO
- Customisations / custom code: TODO
- Version control for theme code: TODO (recommend Git-backed via Shopify CLI / GitHub integration)

**Apps & integrations**
| App / integration | Purpose | Monthly cost | Notes |
|---|---|---|---|
| TODO | TODO | TODO | TODO |

(Watch for: app bloat hurting speed/cost, overlapping apps, unused apps.)

**Data & tracking**
- Analytics: GA4 — TODO verify
- Meta Pixel + Conversions API — TODO verify ([`08-meta-ads.md`](08-meta-ads.md))
- Other pixels/tags: TODO

**Domains / DNS / email auth:** TODO (SPF/DKIM/DMARC for deliverability — links to [`09-email-marketing.md`](09-email-marketing.md)).

**Safe change workflow (standard)**
1. Duplicate the live theme (or use a dev/unpublished theme).
2. Make + review changes off the live theme.
3. Test on mobile + desktop; check speed and key flows.
4. Publish during low-traffic window; keep the previous theme as rollback.
5. Record the change in [`17-release-notes.md`](17-release-notes.md).

## Future Vision

A clean, fast, well-documented Shopify setup: a maintainable Online Store 2.0 theme under version control, a lean app stack justified by ROI, reliable tracking, and a disciplined dev-theme-first change process. Engineering changes are safe, reviewable and reversible — supporting rapid CRO iteration without risking the live store.

## Dependencies

- [`06-website-audit.md`](06-website-audit.md) / [`07-conversion-rate-optimisation.md`](07-conversion-rate-optimisation.md) — what changes are needed.
- [`15-development-standards.md`](15-development-standards.md) — how changes are made and reviewed.
- [`10-seo.md`](10-seo.md), [`08-meta-ads.md`](08-meta-ads.md) — technical/tracking requirements.

## Open Questions

- What theme/version is live, and is it Online Store 2.0?
- Is theme code under version control? Should we set up the Shopify–GitHub integration?
- What is the full app list, cost and overlap?
- Is tracking (GA4, Pixel, CAPI) correctly configured?

## Action Items

- [ ] Document the live theme, version and customisations.
- [ ] Inventory all apps with cost and purpose; flag bloat.
- [ ] Verify analytics and ad tracking.
- [ ] Set up version control for theme code (Shopify CLI / GitHub).
- [ ] Document the safe change workflow and a dev theme.

---

**Status:** 🟡 Draft — awaiting store technical audit
**Last Updated:** 2026-06-29
**Owner:** Shopify Developer prompt
