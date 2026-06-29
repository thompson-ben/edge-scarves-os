# Sprint 0.5 — OS Hardening

**Dates:** 2026-06-29 (1 day) · **Status:** 🟢 Complete · **Phase:** 0 (Foundation)

## Objective

Strengthen the operating system **before** any website development, so future decisions are commercially driven rather than technically driven. Add the highest-level guidance (North Star, principles), an external research library, standardised scorecards, and a commercial Opportunity Scoring Framework that ranks all backlog work.

## Business Justification

The repository foundation was strong, but it lacked (a) a single highest authority to resolve conflicts (North Star), (b) explicit operating principles, (c) a place for external evidence, (d) repeatable measurement (scorecards), and (e) a commercial filter that forces every build decision to be ranked by value-for-cost. Adding these now prevents expensive, technically-led mistakes once development begins — the cheapest possible insurance.

## Acceptance Criteria

- [x] `docs/00-north-star.md` (mission, vision, principles, brand promise, definition of success, non-negotiables, decision framework).
- [x] `docs/00-business-principles.md` (~20 operating principles).
- [x] `/research/` with 8 structured, documented folders (competitors, customer psychology, ecommerce best practice, gift market, seasonal campaigns, fashion trends, Meta advertising, CRO research).
- [x] `/scorecards/` with Business Health, Website Audit, Marketing and Sprint Review scorecards.
- [x] Opportunity Scoring Framework (7 factors → Opportunity Score) created.
- [x] Feature-request template updated to use the Opportunity Score.
- [x] Ranked backlog index requiring all items be scored before implementation.
- [x] No Shopify store changes.

## Tasks

1. [x] Write North Star and Business Principles.
2. [x] Build the Opportunity Scoring Framework with formula + worked examples.
3. [x] Scaffold `/research` (8 folders) with guidance READMEs.
4. [x] Build the 4 scorecards + scorecards index.
5. [x] Wire scoring into the feature-request template and a ranked `backlog/README.md`.
6. [x] Update the top-level README to reflect the strengthened OS.
7. [x] Commit and push.

## Expected Business Impact

No direct revenue impact (foundation). Improves the **quality and commercial discipline** of every future decision: work is ranked by Opportunity Score, measured by scorecards, and grounded in research — reducing wasted effort and technically-led risk.

## KPIs Affected

None directly. Improves decision quality that drives every KPI in [`docs/14-kpis.md`](../docs/14-kpis.md).

## Dependencies

- Sprint 0 foundation complete.

## Release Notes

See [`docs/17-release-notes.md`](../docs/17-release-notes.md) → **v0.2 — OS Hardening**.

## Retrospective

- **What went well:** Added a clear top-of-stack authority (North Star) and a commercial ranking mechanism; all new folders documented (no blank files).
- **What didn't:** TODO (founder review pending).
- **What we learned:** TODO.
- **Actions for next sprint:** Apply Opportunity Scoring to all Sprint 1 audit findings before building.

---
**Owner:** Project Manager prompt / Claude (Lead Technical Architect) · **Last Updated:** 2026-06-29
