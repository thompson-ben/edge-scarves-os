# Backlog — Ranked by Opportunity Score

## Purpose

The master, prioritised list of everything we might build. **Rule: no backlog item is implemented until it has been scored with the [Opportunity Scoring Framework](../scorecards/opportunity-scoring-framework.md) and ranked here against the alternatives.** This is what keeps development commercially driven, not technically driven — we always work the highest-value, lowest-cost opportunity next.

## How the backlog works

1. Every idea is written up as a [feature request](../templates/feature-request.md) (which includes the scoring table).
2. It is scored → **Opportunity Score = (Value Index ÷ Cost Index) × 10**.
3. It is added to the ranked table below and **re-sorted by score**.
4. The PM commits the top-ranked items into the next sprint; the CEO prompt sanity-checks Profit Impact.
5. Items are re-scored when assumptions or data change.

## Ranked backlog

> Sorted high → low by Opportunity Score. Populated from the [Sprint 1 Forensic Audit](../docs/18-forensic-ecommerce-audit.md). Do not implement an unscored item. **Scores are provisional pending baseline data (E1–E3 in the audit) — re-score once analytics exist.**
>
> **Sequencing note:** OPP-02 (data foundation) is a hard prerequisite — schedule it first regardless of rank. OPP-01/07/12 rank lower on pure efficiency but carry a strategic mandate (CEO sign-off).

| Rank | ID | Item | Rev | Profit | Conv | CX | Strat | Effort | Risk | **Score** | Status |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | OPP-03 | Merchandise reviews/Trustpilot on-site | 6 | 5 | 8 | 6 | 5 | 2 | 2 | **29.8** | Ranked |
| 2 | OPP-05 | Cart free-shipping progress + threshold | 5 | 7 | 6 | 5 | 4 | 2 | 2 | **28.3** | Ranked |
| 3 | OPP-16 | Homepage value-prop + gifting promise | 6 | 6 | 7 | 6 | 6 | 3 | 2 | **24.8** | Ranked |
| 4 | OPP-02 | Analytics & tracking foundation | 6 | 6 | 6 | 3 | 8 | 3 | 2 | **23.4** | **Do first** |
| — | ~~OPP-01~~ | **→ Strategic Hypothesis SH-01** (gifting reposition) — validation-gated, not build-ranked | — | — | — | — | — | — | — | — | 🔵 Hypothesis |
| 6 | OPP-09 | Confirm/optimise market & currency config | 6 | 5 | 6 | 6 | 5 | 2 | 3 | **22.2** | Ranked |
| 7 | OPP-04 | Gift bundles / sets + multi-buy (AOV) | 7 | 8 | 5 | 6 | 7 | 4 | 3 | **19.3** | Ranked |
| 8 | OPP-08 | PDP conversion essentials | 6 | 6 | 8 | 7 | 5 | 5 | 2 | **18.3** | Ranked |
| 9 | OPP-07 | Email capture + flows + occasion reminders | 7 | 8 | 6 | 6 | 8 | 5 | 3 | **17.8** | Ranked (strategic) |
| 10 | OPP-06 | Gifting UX (message, receipt, send-direct, add-ons) | 7 | 6 | 7 | 8 | 7 | 5 | 3 | **17.1** | Ranked |
| 11 | OPP-10 | SEO: gift-intent, structured data, "Scarfs", guides | 7 | 6 | 5 | 4 | 7 | 5 | 2 | **16.7** | Ranked |
| 12 | OPP-14 | Mobile UX + site-speed optimisation | 6 | 6 | 7 | 7 | 6 | 5 | 3 | **15.9** | Ranked |
| 13 | OPP-12 | AI Gift Finder quiz (AI-native) | 7 | 6 | 7 | 8 | 9 | 6 | 4 | **14.3** | Ranked (strategic) |
| 14 | OPP-11 | Paid-acquisition readiness (Pinterest/Meta/Shopping) | 8 | 7 | 5 | 4 | 7 | 5 | 4 | **14.1** | Ranked |
| 15 | OPP-13 | Loyalty / "gift again" / occasion CRM / referral | 6 | 7 | 4 | 6 | 8 | 6 | 4 | **12.4** | Ranked |
| 16 | OPP-15 | Range focus & category-expansion gating | 5 | 6 | 4 | 5 | 8 | 4 | 5 | **12.3** | Ranked |

**Bands:** 🟢 ≥40 Strong · 🟡 20–39 Moderate · 🟠 10–19 Weak · 🔴 <10 Poor.

### Strategic Hypotheses (validation-gated — NOT in the build ranking)

Strategic **positioning** bets are held as hypotheses in the [Strategic Hypotheses Register](../docs/18-forensic-ecommerce-audit.md#strategic-hypotheses-register) and must be **validated with evidence before implementation** (per [`docs/19-evidence-standards.md`](../docs/19-evidence-standards.md)). They are tracked separately so they are never mistaken for ready-to-build, scored work.

| ID | Strategic Hypothesis | Confidence | Validation method |
|---|---|---|---|
| SH-01 | Edge Scarves is fundamentally a gifting business → reposition to affordable-luxury gifting | 🟡 Medium | Post-purchase survey + gifting-framed conversion test |
| SH-02 | There is unrealised pricing power | 🔴 Low | Controlled price/premium-tier test |
| SH-03 | Primary customer is the gift-giver, not self-purchaser | 🟡 Medium | Survey + GA4 + gift-message/ship-to data |
| SH-04 | AI-native gifting differentiation is a durable moat | 🔴 Low–Med | Lean AI gift-finder MVP vs control |
| SH-05 | A focused scarves-led range beats category expansion | 🟡 Medium | Category profitability + attach-rate analysis |

> A validated hypothesis re-enters the ranked backlog above as one or more scored recommendations at that point.

## Sprints

The sprint files below pull their work from the top of this ranked backlog:

- [Sprint 0 — Foundation](sprint-00-foundation.md) ✅
- [Sprint 0.5 — OS Hardening](sprint-00-5-os-hardening.md) ✅
- [Sprint 1 — Conversion](sprint-01-conversion.md)
- [Sprint 2 — Meta](sprint-02-meta.md)
- [Sprint 3 — Email](sprint-03-email.md)

> Note: the foundation sprints (0, 0.5) build the operating system itself and predate the scoring requirement. From Sprint 1 onward, every implementation item must carry an Opportunity Score.

## Dependencies

- [`scorecards/opportunity-scoring-framework.md`](../scorecards/opportunity-scoring-framework.md) — the scoring method.
- [`templates/feature-request.md`](../templates/feature-request.md) — where items are written and scored.
- [`docs/00-north-star.md`](../docs/00-north-star.md) — the decision framework scoring sits inside.

## Action Items

- [ ] As website audit (Sprint 1) produces findings, write each as a scored feature request and rank here.
- [ ] Keep this table sorted and current; review at every sprint planning.

---

**Status:** 🟢 Active — ranking process live, items to be added
**Last Updated:** 2026-06-29
**Owner:** Project Manager prompt
