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

> Sorted high → low by Opportunity Score. Populate as feature requests are scored. Do not implement an unscored item.

| Rank | Item | Revenue | Profit | Conv | CX | Strategic | Effort | Risk | **Opp. Score** | Status |
|---|---|---|---|---|---|---|---|---|---|---|
| — | _No scored items yet — add via the [feature request template](../templates/feature-request.md)._ | | | | | | | | | |

**Bands:** 🟢 ≥40 Strong · 🟡 20–39 Moderate · 🟠 10–19 Weak · 🔴 <10 Poor.

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
