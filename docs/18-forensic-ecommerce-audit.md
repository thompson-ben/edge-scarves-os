# 18 — Forensic Ecommerce Audit (Sprint 1)

**Prepared for:** The board of Edge Scarves · **Prepared by:** Fractional Ecommerce Director (acting as Shopify Plus Ecommerce Director, Senior CRO Consultant, Ecommerce CEO, strategy & UX research perspectives) · **Date:** 2026-06-29 · **Status:** 🟢 Living document — evolves as evidence improves.

> **No store changes were made. No code was written.** This is an evidence-gathering and commercial-strategy sprint. Recommendations are ranked, not implemented.

> 📄 **This is a LIVING consultancy document (v1.1).** It is updated as evidence arrives in [`/evidence`](../evidence): claims are upgraded between tiers and recommendations re-scored. See the **Changelog** at the foot of this document.

### Classification key (every claim is tiered — see [`19-evidence-standards.md`](19-evidence-standards.md))

| Tag | Tier | Meaning |
|---|---|---|
| `[FACT]` | Observed Fact | Directly verified from a cited primary source. |
| `[INFERENCE]` | Reasonable Inference | Logically drawn from facts + category norms; not measured. |
| `[HYPOTHESIS]` | Strategic Hypothesis | A strategic/positioning bet requiring validation before scaled action. |
| `[RECOMMENDATION]` | Commercial Recommendation | A scored, justified action (the OPP backlog). |

**Critical for trust:** strategic *positioning* claims in this audit — including the gifting repositioning — are now classified as **Strategic Hypotheses** (`[HYPOTHESIS]`), held in the **Strategic Hypotheses Register** below, and must be **validated with evidence before they drive irreversible action.**

---

## ⚠️ Evidence basis & integrity statement (read first)

A forensic audit is only as good as its evidence, so I am explicit about mine. **The live store could not be crawled directly from this environment:** the session's egress policy denied `edgescarves.com:443` (`connect_rejected — policy denial`). Per the operating system's own non-negotiable ("never invent facts"), I have **not fabricated** page-level observations to fill that gap.

What this audit *is* built on (all cited, see [evidence log](../research/competitors/edge-scarves-evidence-log.md)):
- Search-indexed pages of edgescarves.com (homepage, collections, products, About, policies)
- Trustpilot (TrustScore 4.2, 138 reviews) and review sentiment
- Public Instagram/Facebook profiles
- Competitor research

What it is **not** built on (and is therefore marked **Evidence Required**): direct rendering of the homepage/PDP/cart/checkout, mobile rendering, Core Web Vitals/PageSpeed, structured-data inspection, and **all internal commercial data** (conversion rate, AOV, traffic, repeat rate, margins, ad performance). These require store/analytics access.

**To upgrade this to a full forensic audit, unblock one of:** (a) allow `edgescarves.com` on the session network policy so I can crawl the storefront; (b) provide screenshots (homepage + mobile + a checkout walk-through); (c) grant read access / exports from GA4 and Shopify Analytics. The **Evidence Required Register** (§after Risks) lists exactly what to collect, why, and how it changes the recommendation.

The strategic and commercial reasoning below (positioning, gifting, AOV, retention, AI) stands on the evidence we *do* have and on the economics of the category — it is where most of the value sits, and it is the part least dependent on a live crawl.

---

## 1. Executive Summary

Edge Scarves is a **2021-founded, Norfolk-based online scarf & accessories boutique** that has already built the hardest thing to fake: **a genuine, well-loved gifting product**. Trustpilot 4.2 across 138 reviews, with customers repeatedly praising *quality, hand gift-wrapping (tissue, ribbon, card) and fast delivery*, tells us the product, fulfilment and packaging are not the problem. That is a strong foundation and should be protected, not "optimised away."

The central finding is **strategic, not cosmetic** — and it is a **Strategic Hypothesis (`[HYPOTHESIS]` SH-01), not a proven fact.** What we *know* (`[FACT]`): the business is positioned as *"Luxury Scarves"* but priced at **~£18–£30** and self-describes its mission as *"high-quality scarves at an affordable price"*; its reviews centre overwhelmingly on *gifting and packaging*. What we *infer* (`[INFERENCE]`): it is, in reality, **an affordable premium gifting brand wearing a luxury label**, and that contradiction is likely capping growth (confusing the customer, weakening pricing power, under-exploiting the gifting asset). The **hypothesis** is that the biggest commercial prize is **becoming the go-to destination for a beautiful, affordable, ready-to-give gift** — *to be validated, not assumed* (see Strategic Hypotheses Register, SH-01).

Would I still recommend these moves at £100k/month revenue? The strategic ones (gifting positioning, AOV system, email/retention, paid-acquisition readiness, AI gift-finder) become *more* valuable with scale, not less — they are the engine, not a patch. I flag explicitly where a recommendation is a near-term fix that scale would supersede.

**The five things that matter most (depth over volume):**
1. **Pick a lane and own "gifting."** Resolve the luxury-vs-affordable contradiction by making *the perfect, beautifully-wrapped gift* the hero proposition. **`[HYPOTHESIS]` SH-01 — validate before acting.**
2. **Instrument the business.** Without trustworthy GA4/Shopify/pixel data, every decision below is a guess. This is the prerequisite. (OPP-02)
3. **Put the social proof to work.** 138 Trustpilot reviews and 4.2 stars barely appear to be merchandised on-site. (OPP-03)
4. **Engineer AOV.** A ~£25 product with a £50 free-ship threshold is begging for gift bundles, sets and multi-buy. (OPP-04, OPP-05)
5. **Build the owned-audience and acquisition engine** (email + occasion reminders; Pinterest/Meta gifting creative) — a gifting brand has the best retention hooks in retail (birthdays, anniversaries, Christmas). (OPP-07, OPP-11)

**Headline commercial logic for the £2k → £10k/month net-profit goal:** profit = traffic × conversion × AOV × margin × repeat. Edge Scarves has product and trust; it is under-monetising each of conversion, AOV and repeat. Fixing those — in that order of cost-efficiency — is the cheapest path to £2k/month, and the same levers, instrumented and scaled with paid + retention, are the path to £10k+.

---

## 2. Overall Business Health

| Dimension | Read (evidence-based) | Health |
|---|---|---|
| **Product & fulfilment** | Loved: quality, packaging, speed (Trustpilot 4.2/138). | 🟢 Strong |
| **Brand affection** | Real, but small reach (IG 281, FB 939). | 🟡 Promising, sub-scale |
| **Positioning clarity** | "Luxury" vs ~£18–30 / "affordable" = contradiction. | 🟠 Needs work |
| **Conversion readiness** | Unknown — no analytics. Likely leaks (typical of the stage). | ⚪ Evidence Required |
| **AOV system** | No visible bundling/sets; £50 threshold vs ~£25 item. | 🟠 Underbuilt |
| **Acquisition** | Tiny organic social; paid readiness unknown. | 🟠 Early |
| **Retention/CRM** | Gifting = ideal for it; maturity unknown. | ⚪ Evidence Required |
| **Data foundation** | Unknown; assume immature. | 🔴 Likely a gap |

**Verdict:** a healthy *product* business with an *undermonetised commercial layer*. The gap between "people love it" and "it prints profit" is conversion, AOV, retention and acquisition discipline — all addressable.

---

## 3. Commercial Positioning

> **Tier:** the observations are `[FACT]`; the conclusion that repositioning will unlock growth is `[HYPOTHESIS]` **SH-01/SH-02** — validate before acting.

**Observation `[FACT]`.** Three different self-descriptions are in market simultaneously: *"Luxury Scarves Beautifully Gift Wrapped"* (site), *"Luxury scarves, accessories & gifts"* (FB), *"high-quality scarves at an affordable price"* (About Us). Price points sit at ~£18–£30.

**Why it matters.** "Luxury" sets an expectation (£80–£300, silk/cashmere, heritage) the price and product deliberately don't meet. Mismatched positioning does two expensive things: it **deters the gift-buyer who fears it's out of budget** and **fails to convert the luxury-seeker who finds it "too cheap to be real luxury."** It also **forfeits pricing power** — the brand is apologising for a low price instead of celebrating an accessible one.

**The opportunity.** The honest, ownable, and *more profitable* position is **"affordable luxury gifting"** — *a genuinely beautiful gift, beautifully wrapped, that feels far more expensive than it costs, ready to give.* That is what the reviews already say. It widens the market (every gift occasion), supports gentle price increases, and is defensible against both cheap marketplaces (we're nicer) and true luxury (we're attainable).

**USP, sharpened:** *"The effortless premium gift — hand-wrapped, ready to give, from £25."* Sustainability (REPREVE recycled) and reversibility are **proof points**, not the headline.

→ Captured as **Strategic Hypothesis SH-01** (reposition around gifting) and **SH-02** (pricing power) in the register below — **validation-gated, not yet a build.** Strategic value at £100k/month: *higher* — positioning is the foundation everything else compounds on.

---

## 4. Website Audit

> Most page-level specifics are **Evidence Required** (no live crawl). Findings below combine the evidence we have with category UX research (Baymard/NN-group patterns) — and each is framed as a *hypothesis to verify*, not an asserted defect.

### 4.1 Homepage
- **Observation/Hypothesis:** the homepage likely leads with product/aesthetic rather than a single, unmissable **value proposition + gifting promise + proof** above the fold. **Evidence Required:** capture above-the-fold (desktop + mobile).
- **Why it matters:** first 5 seconds decide bounce; a gifting visitor needs to instantly grasp *what this is, why it's a great gift, why to trust it, and the price is accessible.*
- → **OPP-16** (homepage value-prop & first-impression clarity).

### 4.2 Merchandising & storytelling
- The packaging/unboxing is a top-3 reason customers love the brand, yet (hypothesis) it is under-told on-page. The wrapping *is* the product differentiator and should be shown, not just stated. **Evidence Required:** does the homepage/PDP show the wrapped product? → feeds OPP-01/OPP-08.

### 4.3 Trust on-page
- 138 Trustpilot reviews and 4.2★ appear under-merchandised on-site. → **OPP-03** (highest-ranked quick win).

*(Navigation, collection and product detail in §5, §4.4 below and §8 CRO.)*

### 4.4 Product Pages (summary; full finding OPP-08)
- **Hypotheses to verify:** styling/"how to wear" content for a 90×180cm scarf (versatility is a selling point); material/care/dimension clarity; benefit-led (not feature-led) copy; reviews on the PDP; gifting options (message, send-direct); genuine low-stock urgency. Each is a known conversion lever for considered/gift purchases.

---

## 5. Customer Journey Audit

Mapping the gifting buyer (the dominant, higher-value journey):

| Stage | Evidence / read | Gap → finding |
|---|---|---|
| **Discovery** | Tiny organic social; SEO partial; paid unknown. | Acquisition engine → OPP-10, OPP-11 |
| **Browsing** | Collections exist but gift-occasion framing unknown. | Gift navigation/merchandising → OPP-01, OPP-16 |
| **Comparison** | Reversibility/eco are differentiators; proof under-surfaced. | Reviews + PDP → OPP-03, OPP-08 |
| **Purchase** | Gift UX (message/receipt/send-direct) unknown. | Gifting UX → OPP-06 |
| **Post-purchase** | Packaging delights; review request maturity unknown. | Post-purchase flow → OPP-07 |
| **Retention/Repeat** | Gifting = recurring occasions; CRM maturity unknown. | Occasion reminders/loyalty → OPP-07, OPP-13 |
| **Referral** | Delight exists; no visible referral mechanic. | Referral (fold into OPP-13). |

**Insight:** the journey is strong at the *middle* (product, fulfilment) and weak at the *edges* (getting found; coming back). For a gifting brand, **the edges are where the money is** — occasions repeat.

---

## 6. Mobile Audit

**Assume mobile-majority traffic** (category norm; **Evidence Required:** confirm device split in GA4). For a gift bought impulsively or on-the-go, mobile is the primary store. **Evidence Required:** mobile above-the-fold, tap-target sizing, sticky add-to-cart, image weight, and mobile checkout length. Until captured, mobile-specific defects can't be asserted — but mobile performance/UX is treated as a first-class concern in OPP-08 and OPP-14, and the roadmap front-loads a mobile capture.

---

## 7. Technical Audit

**Evidence Required across the board** (no crawl): Core Web Vitals/PageSpeed (LCP/CLS/INP), image optimisation, structured data (Product, Breadcrumb, Organization, AggregateRating — the last would put review stars in Google), canonical handling of Shopify collection/variant URLs, indexation/sitemap, and JS/app weight. **One concrete signal:** a collection tag is spelled **"Scarfs"** (`/collections/all/scarfs`) — a misspelling/variant that, if it surfaces in URLs or internal links, is both an SEO and polish issue worth checking. → feeds OPP-10. A technical baseline (PSI + Search Console) is cheap and is scheduled early.

---

## 8. CRO Audit

Without analytics I cannot quantify leaks, so I prioritise the **highest-probability, lowest-cost conversion levers** for this exact business model, each as a verifiable hypothesis:

1. **Social proof is under-merchandised** (OPP-03) — stars on homepage/collection/PDP + Trustpilot widget. Strongest evidence (we *know* 138 reviews/4.2★ exist).
2. **First-impression clarity** (OPP-16) — value prop + gifting promise above the fold.
3. **PDP conversion essentials** (OPP-08) — styling content, benefits, trust, reviews, gifting.
4. **Cart/shipping incentive** (OPP-05) — progress-to-free-shipping messaging.
5. **Gifting UX** (OPP-06) — gift message/receipt/send-direct reduce purchase anxiety for the *non-self* buyer.

**Principle applied:** I am *not* recommending generic "best practice." Each lever is justified by *this* business being a trust-rich, gift-led, ~£25 AOV store where the dominant buyer is purchasing for someone else.

---

## 9. Brand Audit

**Strengths (evidence):** authentic packaging ritual, real warmth in reviews, a coherent "lovingly gift wrapped" thread across site/IG/FB, and credible sustainability (REPREVE). **Tensions:** the "luxury" claim vs accessible price/product; small reach limiting brand-building flywheel. **Consistency/Evidence Required:** typography, colour, photography direction, and whether photography sells *the gift and the wearing* (lifestyle) vs flat product. **Recommendation:** double down on **"affordable luxury gifting"** with consistent lifestyle + unboxing photography. Brand is an asset here — protect the affection, sharpen the claim. *Do not* chase a true-luxury reposition (the price/product can't bank it).

---

## 10. SEO Audit

**Evidence:** the site is indexed with a logical collection taxonomy (Best Sellers, Recycled, Reversible, Wraps, Bags, Loungewear) — good. **Gaps/Evidence Required:** title/meta optimisation, structured data (esp. AggregateRating for review stars in SERPs), the **"Scarfs"** spelling variant, thin-collection risk, and — critically — **no visible capture of gift-intent search demand** ("scarf gifts for her", "gifts under £30", "Mother's Day scarf", "eco-friendly gift"). A gifting brand should own informational + commercial gift queries via collections + buying guides. → **OPP-10**. SEO compounds — at £100k/month it's a major moat, so start the foundations now.

---

## 11. Marketing Readiness

| Channel | Readiness (evidence) | Priority |
|---|---|---|
| **Email/CRM** | Unknown; **the** highest-margin lever for a repeat-occasion gifting brand. | High → OPP-07 |
| **Pinterest** | Not yet leveraged; *ideal* for scarves/gifting/styling (high-intent, visual, long content life). | High → OPP-11 |
| **Meta (FB/IG)** | 939 FB / 281 IG; organic sub-scale; paid readiness (pixel/CAPI/catalogue) **Evidence Required**. | High → OPP-11 |
| **Google Shopping** | Feed/Merchant Center status unknown; strong for product+gift intent. | Med → OPP-11 |
| **SEO/Content** | Foundations only. | Med → OPP-10 |
| **Remarketing** | Depends on pixel + audiences (email, viewers). | Med → OPP-02, OPP-11 |

**Gate:** no paid scaling until **tracking is trustworthy (OPP-02)** and **break-even ROAS is known** (from margin data). Spending before instrumentation is how small brands lose money fast.

---

## 12. Trust & Credibility

**Strong and underused.** Trustpilot 4.2/138 + glowing packaging/delivery sentiment is a conversion asset largely sitting *off-site*. Bring it on-site everywhere (OPP-03), add trust/guarantee/returns clarity at PDP and cart (OPP-05/06/08), and address the two isolated negatives operationally (delivery confirmation comms; protective packaging in transit) — small fixes that protect the 4.2. **Reconcile** the on-site "5★/103" vs Trustpilot "4.2/138" so the brand quotes one credible, consistent number.

---

## 13. Product Strategy

**Evidence:** core = ladies' scarves (~90×180), Eco/REPREVE range, reversible range; **plus** loungewear, wraps, bags. **Tension:** breadth (loungewear, bags) can dilute a small brand's identity and inventory focus, *or* it can raise AOV/LTV if coherent. **Recommendation:** keep **scarves as the hero**, treat wraps/eco/reversible as the natural family, and **gate category expansion (loungewear/bags) behind a margin + attach-rate test** — expand only what raises AOV/repeat without blurring "the gift brand." → **OPP-15** (range focus & category gating). At £100k/month, a coherent range is what makes paid acquisition efficient, so set the discipline now.

---

## 14. Merchandising Strategy

**Recommendations:** (a) **occasion-led merchandising** — "Gifts for Her", "Under £30", "Mother's Day", "Eco Gifts", "Bestselling Gifts" — so browsing maps to *why people buy*; (b) lead collections with **bestsellers + review counts**; (c) show the **wrapped/gift state** in merchandising, not just the flat scarf; (d) seasonal front-page rotation aligned to the gifting calendar. Most of this is configuration, not build — high leverage. Folded into OPP-01/OPP-16 and the seasonal plan.

---

## 15. AOV Opportunities

**The clearest near-term profit lever.** A ~£25 item against a **£50 free-shipping threshold** is an open invitation:
- **Gift bundles / curated gift sets** (e.g. "scarf + matching accessory", "two-gift set") — raises AOV *and* reinforces the gifting identity. (OPP-04)
- **"Buy 2, both beautifully wrapped"** multi-gift framing — gifting buyers often need several gifts. (OPP-04)
- **Free-shipping progress messaging** in cart ("£12 away from free delivery") — nudges toward the £50 threshold. (OPP-05)
- **Thoughtful add-ons** (gift card, premium wrap upgrade, greeting card) — small attach items lift AOV at near-100% margin. (fold into OPP-06)

**Why it compounds:** every £1 of AOV on existing traffic is near-pure contribution — the single most efficient route to the £2k/month net target. Still essential at £100k/month.

---

## 16. Retention Opportunities

A gifting brand has **the best natural retention hooks in ecommerce**: occasions recur.
- **Core email flows** (welcome, abandoned cart, post-purchase, win-back) — table stakes, high ROI. (OPP-07)
- **Occasion reminders** — capture "who/what was this gift for + the date" and prompt next year ("Mum's birthday is coming — gift again?"). This is a *category-defining* retention mechanic few small scarf brands run. (OPP-07/OPP-13)
- **Loyalty / "gift again"** reorder mechanic + referral (delighted gift recipients are warm leads). (OPP-13)
- **Gifting subscription / "gift of the season"** — a curated wrapped scarf delivered each season as a standing gift or self-treat (strategic, test later). (OPP-13)

Retention is how £2k/month becomes durable and £10k/month becomes achievable without buying every sale.

---

## 17. Strategic Opportunities (think bigger — 5-year view)

*"What business should Edge Scarves become?"* — **the UK's go-to affordable luxury gifting brand, starting with scarves**, run as an **AI-native** operation.

- **Own "the effortless gift."** Expand from "scarves" to *adjacent, coherent, giftable accessories* (always hand-wrapped) — the moat is the *gifting experience + brand affection*, not the scarf SKU.
- **AI-native differentiation:**
  - **AI Gift Finder / quiz** — "Find the perfect gift in 30 seconds" (recipient, occasion, budget, taste → curated wrapped gift). Raises conversion + AOV, captures first-party data, and is genuinely on-brand for the gifting use case. (OPP-12)
  - **AI styling assistant** ("3 ways to wear this"), **AI-generated SEO buying guides** at scale, **AI customer service**, and **AI-driven occasion/lifecycle personalisation**. These let a lean team operate like a big one — the company's stated thesis.
- **Subscription/loyalty** (above) for recurring revenue.
- **Partnerships / corporate & event gifting** (weddings, corporate thank-yous) — high-AOV, low-CAC B2B2C extension of the gifting core.
- **Operational efficiency:** AI for merchandising, content, and support to protect net margin as volume grows.

These are where the £10k+/month (and beyond) value compounds. They depend on the foundations (positioning, data, AOV, retention) being in place first — hence the roadmap order.

---

## 18. Risks

| # | Risk | Why it matters | Mitigation |
|---|---|---|---|
| R1 | **Decisions without data** | Every commercial call is a guess; spend can leak. | OPP-02 first; baseline before scaling. |
| R2 | **Positioning drift** | "Luxury" vs price confuses & caps conversion. | OPP-01 — commit to affordable-luxury gifting. |
| R3 | **Premature paid spend** | Scaling ads before tracking/economics → losses. | Gate paid on OPP-02 + known break-even ROAS. |
| R4 | **Single-channel / platform dependence** | Over-reliance on one traffic source or Shopify app sprawl. | Diversify (SEO, email, Pinterest); lean app stack. |
| R5 | **Brand dilution via range sprawl** | Loungewear/bags blur the gift identity. | OPP-15 — gate expansion on margin/attach tests. |
| R6 | **Protecting the 4.2★** | Delivery-comms & transit-damage complaints erode trust. | Ops fixes (confirmations, protective packing). |
| R7 | **Founder/key-person & capacity** | Lean team; over-ambition stalls delivery. | Sequence ruthlessly by Opportunity Score; AI leverage. |
| R8 | **Seasonality concentration** | Gifting peaks (Q4) create revenue lumpiness. | Build year-round occasions + retention (OPP-07/13). |

---

## Evidence Required Register (what to collect, why, how it changes decisions)

> Founder-supplied evidence is stored in [`/evidence`](../evidence) (desktop, mobile, checkout, emails, analytics, competitors, customer-feedback) and **referenced back into this living document** — each item below, once collected, upgrades the relevant claim's tier and re-scores its recommendation.

| # | Evidence needed | Why it matters | How to collect | Influences |
|---|---|---|---|---|
| E1 | Conversion rate, sessions, device split, funnel drop-off | Quantifies every CRO finding; sizes the prize | GA4 + Shopify Analytics export | OPP-02, all CRO |
| E2 | AOV, margin, COGS, contribution/order | Sets break-even ROAS; sizes AOV prize | Shopify + accounts | OPP-04/05, paid gate |
| E3 | Repeat-purchase rate, LTV, email list size & rev share | Sizes retention prize | Shopify + ESP | OPP-07/13 |
| E4 | Homepage/PDP/cart **screenshots** (desktop+mobile) | Confirms UX hypotheses | Manual capture → `/screenshots` | OPP-08/16, §4/§6 |
| E5 | Checkout walk-through (steps, options, friction) | Identifies checkout leaks | Manual test order | §CRO, checkout |
| E6 | PageSpeed/CWV + structured-data + Search Console | Technical baseline & SEO | PSI, Rich Results test, GSC | OPP-10/14, §7 |
| E7 | Default currency / Markets config | UK trust & conversion; USD-to-crawler caveat | Store admin / test as UK visitor | OPP-09 |
| E8 | Pixel/CAPI/catalogue & ad-account status | Paid readiness & remarketing | Meta/Google admin | OPP-02/11 |

> **Top priority to unblock:** E4 + E5 (screenshots/checkout walk-through) and E1/E2 (GA4 + Shopify exports). With those, ~80% of the "Evidence Required" items convert to firm, quantified findings.

---

## Strategic Hypotheses Register

> **These are `[HYPOTHESIS]`, not `[RECOMMENDATION]`.** They are strategic/positioning bets that must be **validated with evidence before they drive irreversible action**. Each follows the structure in [`19-evidence-standards.md`](19-evidence-standards.md). They are *not* in the build-ranked backlog; validating them is the work. The contradicting-evidence column is deliberately populated — a hypothesis with no stated counter-evidence is under-examined.

### SH-01 — Edge Scarves is fundamentally a *gifting* business and should reposition around "affordable luxury gifting"
- **Statement:** Making *the perfect, beautifully-wrapped, ready-to-give gift* the hero proposition (rather than "luxury scarves") will increase conversion, AOV and brand pull.
- **Supporting Evidence:** `[FACT]` reviews centre overwhelmingly on packaging/gifting/delivery; `[FACT]` "gift wrapping as standard" (tissue/ribbon/card); `[FACT]` IG/FB bios already foreground "lovingly gift wrapped"; `[FACT]` ~£18–30 price suits gifting impulse buys.
- **Contradicting Evidence:** `[INFERENCE]` some customers may buy for themselves (self-treat) — unknown split; `[INFERENCE]` "luxury" framing may attract a segment we'd dilute; no `[FACT]` yet on gift-vs-self ratio.
- **Validation Required:** the gift-vs-self purchase split; whether gifting framing lifts conversion/AOV vs current.
- **Expected Commercial Impact:** potentially the largest single lever — conversion + AOV + lower price-sensitivity + wider occasion-driven demand. (Quantify after E1–E2.)
- **Validation Method:** post-purchase survey ("gift or self? who for?"); analytics on gift-message usage; an A/B or before/after test of gifting-framed homepage/landing vs control.
- **Confidence Level:** 🟡 **Medium** — strong qualitative signal (reviews, packaging), no quantitative split yet.

### SH-02 — There is unrealised pricing power
- **Statement:** The brand can hold or raise prices (improving margin) without materially losing volume, because the "luxury/affordable" gap suggests it is under-charging for the perceived value.
- **Supporting Evidence:** `[FACT]` "luxury" positioning at ~£18–30; `[FACT]` reviews say product/packaging feel premium ("beautifully presented", "excellent quality").
- **Contradicting Evidence:** `[FACT]` mission explicitly targets "affordable price"; `[INFERENCE]` price-sensitive gift shoppers may anchor on sub-£30; competitor price points (£20–55) are mixed.
- **Validation Required:** price elasticity; whether a higher price or premium tier holds conversion.
- **Expected Commercial Impact:** direct margin/net-profit uplift — even +£2–3 AOV on existing volume is high-leverage. (Quantify after E2.)
- **Validation Method:** price test on a subset/new line; premium "gift edition" at a higher price; monitor conversion + AOV.
- **Confidence Level:** 🔴 **Low** — plausible but untested; do not act before a controlled test.

### SH-03 — The primary customer is the *gift-giver*, not the self-purchaser
- **Statement:** The dominant, higher-value buyer is purchasing for someone else; the persona and journey should be built for the gift-giver first.
- **Supporting Evidence:** `[FACT]` gifting-led reviews; `[FACT]` gift-wrap-as-standard; `[INFERENCE]` seasonal gifting category.
- **Contradicting Evidence:** no `[FACT]` on the actual split; reversible/eco features appeal to self-purchasers too.
- **Validation Required:** the real gift-vs-self ratio and the gifter's demographics/occasions.
- **Expected Commercial Impact:** sharper targeting → cheaper acquisition, higher conversion; underpins SH-01.
- **Validation Method:** post-purchase survey; GA4 demographics; gift-message/ship-to-different-address data.
- **Confidence Level:** 🟡 **Medium** — consistent qualitative signal; needs the quantitative split.

### SH-04 — AI-native gifting differentiation is a durable competitive moat
- **Statement:** Building AI-native gifting experiences (starting with an AI Gift Finder) creates a defensible advantage small scarf competitors won't match, improving conversion, AOV and first-party data.
- **Supporting Evidence:** `[FACT]` company thesis is to be AI-native; `[INFERENCE]` gift discovery is a genuine customer pain (decision anxiety) that AI suits; `[FACT]` competitors show no such tooling in research.
- **Contradicting Evidence:** `[INFERENCE]` at current traffic the absolute uplift may be small; build/maintenance cost is real; novelty ≠ profit.
- **Validation Required:** that a gift finder measurably lifts conversion/AOV at our traffic; that it's not solving a non-problem.
- **Expected Commercial Impact:** conversion + AOV + data asset; compounds at scale. (Quantify via test.)
- **Validation Method:** a lean MVP gift-finder on a fraction of traffic; measure completion → conversion/AOV vs control.
- **Confidence Level:** 🔴 **Low–Medium** — strategically compelling, commercially unproven at current scale.

### SH-05 — A focused, scarves-led range beats category expansion at this scale
- **Statement:** Concentrating on scarves + coherent accessories (and gating loungewear/bags behind margin/attach tests) yields better profit and brand clarity than broad expansion.
- **Supporting Evidence:** `[FACT]` range already spans loungewear/bags/wraps; `[INFERENCE]` small brands gain from focus (inventory, story, ad efficiency).
- **Contradicting Evidence:** `[INFERENCE]` expansion could raise AOV/LTV if attach rates are high; no `[FACT]` yet on category-level margins/attach.
- **Validation Required:** per-category margin, sell-through and attach rates.
- **Expected Commercial Impact:** protects margin and acquisition efficiency; avoids dead inventory.
- **Validation Method:** category profitability analysis (E2) + attach-rate analysis; review before any expansion spend.
- **Confidence Level:** 🟡 **Medium** — focus is generally right for the stage, but category data could change the call.

> **Gate:** none of SH-01…SH-05 is implemented at scale until validated. Several validation methods are themselves cheap, reversible tests — that is the approved path from `[HYPOTHESIS]` to `[RECOMMENDATION]`.

---

## Opportunity Backlog — every recommendation, scored & ranked

Scored with the [Opportunity Scoring Framework](../scorecards/opportunity-scoring-framework.md): `Value Index = 0.30·Profit + 0.20·Revenue + 0.20·Conversion + 0.15·Strategic + 0.15·CX`; `Cost = (Effort+Risk)/2`; **`Opportunity Score = (Value/Cost)×10`**. KPI-improvement figures are **directional hypotheses pending baseline (E1–E3)**, not measured results.

| Rank | ID | Recommendation | Rev | Profit | Conv | CX | Strat | Effort | Risk | **Score** | Band |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | OPP-03 | Merchandise reviews/Trustpilot on-site (stars on home/collection/PDP) | 6 | 5 | 8 | 6 | 5 | 2 | 2 | **29.8** | 🟡 |
| 2 | OPP-05 | Cart free-shipping progress + threshold optimisation | 5 | 7 | 6 | 5 | 4 | 2 | 2 | **28.3** | 🟡 |
| 3 | OPP-16 | Homepage value-prop + gifting promise above the fold | 6 | 6 | 7 | 6 | 6 | 3 | 2 | **24.8** | 🟡 |
| 4 | OPP-02 | Analytics & tracking foundation (GA4/Pixel/CAPI/consent) | 6 | 6 | 6 | 3 | 8 | 3 | 2 | **23.4** | 🟡 |
| — | ~~OPP-01~~ | **Reclassified → Strategic Hypothesis SH-01** (gifting repositioning). Validation-gated; see register above. | — | — | — | — | — | — | — | — | 🔵 Hypothesis |
| 6 | OPP-09 | Confirm/optimise market & currency config (GBP default) | 6 | 5 | 6 | 6 | 5 | 2 | 3 | **22.2** | 🟡 |
| 7 | OPP-04 | Gift bundles / curated sets + multi-buy (AOV) | 7 | 8 | 5 | 6 | 7 | 4 | 3 | **19.3** | 🟠 |
| 8 | OPP-08 | PDP conversion essentials (styling, benefits, trust, reviews) | 6 | 6 | 8 | 7 | 5 | 5 | 2 | **18.3** | 🟠 |
| 9 | OPP-07 | Email capture + core flows + occasion reminders | 7 | 8 | 6 | 6 | 8 | 5 | 3 | **17.8** | 🟠 |
| 10 | OPP-06 | Gifting UX (gift message, receipt, send-direct, add-ons) | 7 | 6 | 7 | 8 | 7 | 5 | 3 | **17.1** | 🟠 |
| 11 | OPP-10 | SEO: gift-intent keywords, structured data, fix "Scarfs", guides | 7 | 6 | 5 | 4 | 7 | 5 | 2 | **16.7** | 🟠 |
| 12 | OPP-14 | Mobile UX + site-speed optimisation | 6 | 6 | 7 | 7 | 6 | 5 | 3 | **15.9** | 🟠 |
| 13 | OPP-12 | **AI Gift Finder** quiz (AI-native differentiation) | 7 | 6 | 7 | 8 | 9 | 6 | 4 | **14.3** | 🟠 |
| 14 | OPP-11 | Paid-acquisition readiness (Pinterest/Meta/Shopping + creative) | 8 | 7 | 5 | 4 | 7 | 5 | 4 | **14.1** | 🟠 |
| 15 | OPP-13 | Loyalty / "gift again" / occasion CRM / referral | 6 | 7 | 4 | 6 | 8 | 6 | 4 | **12.4** | 🟠 |
| 16 | OPP-15 | Range focus & category-expansion gating | 5 | 6 | 4 | 5 | 8 | 4 | 5 | **12.3** | 🟠 |

> **Reading the ranking:** the framework correctly floats **cheap, high-certainty conversion/AOV wins** to the top and pushes **heavier strategic builds** down on pure efficiency. That does **not** mean "do 1–6 and ignore the rest" — several lower-ranked items (OPP-01, OPP-07, OPP-12) are **strategically essential** and carry a CEO/strategic mandate. OPP-02 (data) is a **hard prerequisite** for honest measurement and should be sequenced first regardless of its rank.

### Selected findings in full (feature-request format)

> Each item below carries the required fields. (The remaining items follow the same structure; full write-ups are produced as they enter a sprint. Each will be copied into a [feature request](../templates/feature-request.md).)

#### OPP-01 — *Reclassified to Strategic Hypothesis SH-01*
> Per Sprint 1 review, the gifting repositioning is now **`[HYPOTHESIS]` SH-01** in the Strategic Hypotheses Register above — it must be **validated with evidence** (gift-vs-self split; a gifting-framed conversion test) **before** it drives an irreversible reposition. The eventual *implementation* of a validated SH-01 will re-enter the backlog as one or more scored recommendations at that point.

#### OPP-03 — Merchandise social proof on-site
- **Observation:** strong off-site reviews (Trustpilot 4.2/138) appear under-surfaced on-site.
- **Evidence:** Trustpilot page; sentiment praising quality/packaging/delivery.
- **Commercial impact:** social proof is among the most reliable conversion levers; this is high-certainty because the reviews demonstrably exist.
- **Recommended solution:** review stars on homepage, collection cards and PDPs; Trustpilot widget; reconcile to one credible number; seed PDP reviews per product.
- **Expected KPI improvement (hypothesis):** conversion + (esp. PDP). Quantify after E1.
- **Opportunity Score:** 29.8 (Value 5.95 / Cost 2.0). **Priority:** High (top quick win).
- **Dependencies:** reviews app / Trustpilot integration (Evidence Required on current tooling).
- **Acceptance criteria:** rating visible on home, collection and PDP; single consistent stat; PDP review module live.
- **Owner:** CRO + Shopify Developer (future sprint).

#### OPP-02 — Analytics & tracking foundation
- **Observation:** commercial data availability unknown; assume immature.
- **Evidence:** none available to this audit — itself the finding.
- **Commercial impact:** without trustworthy data, every other decision (and all paid spend) is unmeasurable and risky. Foundational.
- **Recommended solution:** verify and correctly configure GA4, Meta Pixel + Conversions API, consent, and key events (view→ATC→checkout→purchase); establish dashboards ([`docs/14-kpis.md`](14-kpis.md)).
- **Expected KPI improvement:** indirect — unlocks measurement of all others.
- **Opportunity Score:** 23.4. **Priority:** **Do first** (prerequisite, overrides rank).
- **Dependencies:** store + ad-account access (E1, E8).
- **Acceptance criteria:** events verified accurate; baselines recorded for every KPI; break-even ROAS derivable.
- **Owner:** Data Analyst + Shopify Developer.

#### OPP-04 — Gift bundles / sets + multi-buy (AOV)
- **Observation:** ~£25 item vs £50 free-ship threshold; no visible bundling.
- **Evidence:** indexed prices; £50 threshold; gifting-led reviews.
- **Commercial impact:** AOV uplift is near-pure contribution — the most cost-efficient route to the £2k/month net target.
- **Recommended solution:** curated gift sets, "two-gift" bundles, premium-wrap/greeting-card add-ons; merchandise toward the £50 threshold.
- **Expected KPI improvement (hypothesis):** AOV +; units/order +. Quantify after E2.
- **Opportunity Score:** 19.3. **Priority:** High.
- **Dependencies:** OPP-01 framing; margin data (E2); bundling capability (Evidence Required).
- **Acceptance criteria:** ≥2 gift bundles/sets live; add-on at cart; threshold messaging (OPP-05) in place.
- **Owner:** Merchandising/CRO + Shopify Developer.

*(OPP-05, 06, 07, 08, 09, 10, 11, 12, 13, 14, 15, 16 — same format, written up on entry to a sprint; see ranked table and the relevant section above for observation/evidence/impact.)*

---

## 19. Quick Wins (high score, low cost — do first)

1. **OPP-03** Reviews on-site (29.8)
2. **OPP-05** Cart free-shipping progress (28.3)
3. **OPP-16** Homepage value-prop clarity (24.8)
4. **OPP-09** Confirm GBP/market config (22.2)
5. **OPP-02** Tracking foundation (23.4) — *technically a quick-ish build but treat as the prerequisite.*

These are mostly **configuration/copy/merchandising**, not heavy builds — fast payback on existing traffic.

## 20. High-Impact Projects (lower efficiency score, high strategic value)

1. **SH-01** Gifting repositioning — the foundation everything compounds on — *validate first (Strategic Hypothesis), then implement.*
2. **OPP-07** Email + occasion-reminder CRM — best retention hooks in retail.
3. **OPP-12** AI Gift Finder — on-brand AI-native differentiation; conversion + data + AOV.
4. **OPP-11** Paid-acquisition readiness (Pinterest/Meta/Shopping) — the growth dial, *after* OPP-02.
5. **OPP-13 / OPP-15** Loyalty & range strategy — durability and margin discipline at scale.

## 21. 90-Day Roadmap

> Sequenced for the £2k/month net target while laying £10k/month foundations. Maps to two-week sprints; each item enters as a scored feature request.

**Days 0–15 — Instrument, See & Validate (foundation)**
- OPP-02 tracking foundation; collect E1–E8 into [`/evidence`](../evidence) (esp. screenshots E4, checkout E5, PSI/GSC E6).
- Confirm OPP-09 currency/market config.
- **Begin validating the Strategic Hypotheses** — launch the post-purchase survey (SH-01/SH-03 gift-vs-self) and category profitability pull (SH-05).
- *Exit:* trustworthy baselines for every KPI; "Evidence Required" items resolved; first hypothesis-validation evidence captured.

**Days 16–30 — Quick Wins on existing traffic**
- OPP-03 reviews on-site; OPP-05 cart threshold messaging; OPP-16 homepage value-prop.
- *Exit:* measurable conversion/AOV lift on current traffic (now measurable thanks to OPP-02).

**Days 31–55 — Position & Monetise**
- **Act on SH-01/SH-03 validation results:** if the gift-vs-self evidence supports it, implement the gifting reposition (homepage + occasion-led collections) as scored recommendations; if not, adjust. OPP-04 bundles/sets; OPP-06 gifting UX; OPP-08 PDP essentials.
- *Exit:* positioning decision made *on evidence*; AOV system live.

**Days 56–75 — Own the Audience**
- OPP-07 email capture + core flows + occasion reminders; OPP-10 SEO gift-intent foundations; OPP-14 mobile/speed.
- *Exit:* owned audience growing; recovered-revenue flows live.

**Days 76–90 — Acquire & Differentiate (test, don't scale blindly)**
- OPP-11 paid readiness + first Pinterest/Meta gifting tests (gated on break-even ROAS); scope OPP-12 AI Gift Finder; plan OPP-13 loyalty & OPP-15 range gating.
- *Exit:* a measured, profitable acquisition test + a differentiation roadmap into the next quarter.

**Through-line:** prove the conversion+AOV+retention engine on existing traffic first (cheap path to £2k/month net), *then* pour acquisition into a store that converts and retains (path to £10k+/month).

## 22. Conclusion

Edge Scarves is a better business than its current scale suggests. It has done the hard, unfakeable part — **a product and a packaging experience customers genuinely love** (`[FACT]`) — and it *appears* to sit on an undervalued strategic asset: the hypothesis (`[HYPOTHESIS]` SH-01) that **it is already a gifting brand.** The work ahead is not to fix a broken store; it is to **stop under-selling a good one** — but the central positioning bet is to be *validated, not assumed.* Instrument the business so decisions are evidence-led, **test the gifting hypothesis**, harvest the cheap conversion and AOV wins, build the owned-audience and occasion-retention engine, and only then scale acquisition — adding AI-native differentiation (starting with a gift finder) as a moat to be proven.

Do that, and £2,000/month net profit is a near-term engineering problem, not a hope; and the same engine, instrumented and scaled, is a credible route to £10,000+/month. The single most important next action is the least glamorous: **get the evidence (E1–E8) so this audit's hypotheses become a quantified, fully-costed plan.**

---

## Dependencies
- [`docs/19-evidence-standards.md`](19-evidence-standards.md) (classification) · [`/evidence`](../evidence) (primary evidence) · [`scorecards/opportunity-scoring-framework.md`](../scorecards/opportunity-scoring-framework.md) · [`research/competitors/edge-scarves-evidence-log.md`](../research/competitors/edge-scarves-evidence-log.md) · [`docs/00-north-star.md`](00-north-star.md) · [`backlog/README.md`](../backlog/README.md)

## Open Questions
- Can `edgescarves.com` be allowed on the session network policy for a full crawl, or will evidence come via screenshots/exports into [`/evidence`](../evidence)?
- Founder's view on Strategic Hypothesis **SH-01** (gifting) — and willingness to run the validating post-purchase survey?
- Confirmed primary market/currency and target geographies?

## Action Items
- [ ] Collect Evidence Required Register items E1–E8 into [`/evidence`](../evidence) (founder/analyst).
- [ ] **Validate the Strategic Hypotheses (SH-01…SH-05)** via their stated methods before any is implemented at scale.
- [ ] Convert each OPP into a scored [feature request](../templates/feature-request.md) and keep [`backlog/README.md`](../backlog/README.md) current.
- [ ] Re-score every OPP, and upgrade claim tiers, as evidence arrives — this is a living document.

## Changelog
- **v1.1 — 2026-06-29:** Sprint 1 review response. Added the four-tier classification key ([`19-evidence-standards.md`](19-evidence-standards.md)); reclassified gifting/positioning recommendations into the **Strategic Hypotheses Register (SH-01…SH-05)** with supporting/contradicting evidence, validation method and confidence; linked the new [`/evidence`](../evidence) intake; marked the document as living. OPP-01 retired into SH-01.
- **v1.0 — 2026-06-29:** Initial forensic audit (Sprint 1), 16 scored recommendations, built on cited public evidence (live crawl blocked by egress policy).

---

**Status:** 🟢 Living document (v1.1) — evidence-led, evolves as `/evidence` grows · **Last Updated:** 2026-06-29 · **Owner:** Fractional Ecommerce Director (CEO + CRO + Data Analyst prompts)
