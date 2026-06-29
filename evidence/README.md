# Evidence

The canonical store of **primary evidence** about Edge Scarves — the raw material that turns audit hypotheses into proven facts. Everything the founder supplies (screenshots, exports, recordings, feedback) lives here, is citable, and is referenced directly by the [Forensic Audit](../docs/18-forensic-ecommerce-audit.md) and any strategic decision.

> This folder is what makes the operating system **traceable**: every `[FACT]` should point to a file here. See the classification rules in [`docs/19-evidence-standards.md`](../docs/19-evidence-standards.md).

## Structure

| Folder | What goes here |
|---|---|
| [`desktop/`](desktop) | Desktop storefront screenshots (homepage, nav, collections, PDPs, cart). |
| [`mobile/`](mobile) | Mobile storefront screenshots (same pages — mobile is the priority surface). |
| [`checkout/`](checkout) | Checkout walk-through: each step, payment options, friction points. |
| [`emails/`](emails) | Existing emails & flows (welcome, abandoned cart, post-purchase), ESP screenshots/stats. |
| [`analytics/`](analytics) | GA4 / Shopify / ad-platform exports & screenshots (conversion, AOV, funnel, traffic). |
| [`competitors/`](competitors) | Competitor screenshots and teardowns (complements [`research/competitors`](../research/competitors)). |
| [`customer-feedback/`](customer-feedback) | Reviews, survey responses, support tickets, voice-of-customer. |

## How to add evidence

1. **Name it citably:** `YYYY-MM-DD_<area>_<short-description>.<ext>`
   e.g. `2026-07-02_pdp_mobile_eco-style-hearts.png`, `2026-07-02_ga4_conversion-funnel-30d.csv`.
2. **Drop it in the right folder.** Capture **desktop + mobile** where relevant.
3. **Note the source & date** (the filename date = when captured).
4. **Reference it** from the audit/finding it supports, and **upgrade the claim's tier** (e.g. `[INFERENCE]` → `[FACT]`) per [`docs/19-evidence-standards.md`](../docs/19-evidence-standards.md).
5. Re-score the affected recommendation if the new evidence changes effort/impact.

## Priority evidence to collect first (from the audit's Evidence Required Register)

- **E4** desktop + **mobile** screenshots (homepage, PDP, cart) → `desktop/`, `mobile/`
- **E5** checkout walk-through → `checkout/`
- **E1/E2** GA4 + Shopify exports (conversion, AOV, funnel, margin) → `analytics/`
- **E3** repeat rate / email list / flow stats → `analytics/`, `emails/`
- **E6** PageSpeed / Core Web Vitals / Search Console → `analytics/`
- **E7** currency/market config (screenshot as a UK visitor) → `desktop/`

> Privacy: redact customer personal data (names, emails, addresses) from screenshots and exports before adding.

**Status:** 🟡 Awaiting founder evidence · **Last Updated:** 2026-06-29 · **Owner:** Data Analyst prompt / Ben Thompson (Founder)
