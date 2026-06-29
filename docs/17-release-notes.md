# 17 — Release Notes

## Purpose

The chronological, versioned record of everything shipped — to the repository and to the store. Release notes make change auditable: what shipped, when, why, and what impact it had. Every release (merged PR with a Definition of Done met) appends an entry here.

## Current State

Versioning: `vMAJOR.MINOR` — MAJOR = strategic milestone, MINOR = shipped sprint increment. Newest entries on top. Use [`templates/release-template.md`](../templates/release-template.md) to draft each release.

---

### v0.3 — Forensic Ecommerce Audit (Sprint 1) — 2026-06-29
**Type:** Repository / documentation — evidence & strategy (no store changes, no code)
**Sprint:** [Sprint 1](../backlog/sprint-01-conversion.md)

**Summary:** Delivered a consultancy-grade forensic ecommerce audit of edgescarves.com that becomes the prioritised backlog for all future development. Every recommendation is evidence-based and scored with the Opportunity Scoring Framework.

**Shipped:**
- `docs/18-forensic-ecommerce-audit.md` — 22-section board-grade audit (exec summary → 90-day roadmap → conclusion), 16 scored & ranked recommendations (OPP-01…OPP-16), an Evidence Required Register, and an integrity statement.
- `research/competitors/edge-scarves-evidence-log.md` — cited public-evidence log underpinning the audit.
- `backlog/README.md` — ranked Opportunity Backlog populated from the audit.

**Evidence note:** the live store could not be crawled (session egress policy denied `edgescarves.com:443`); findings rest on search-indexed pages, Trustpilot (4.2/138) and social profiles, with all internal/commercial data marked *Evidence Required*. No facts were invented.
**Business impact:** Produces the commercial blueprint and prioritised backlog; no direct revenue impact (strategy sprint).
**KPIs affected:** None directly; directs the work that will move all KPIs.
**Store changes:** None (by design).

---

### v0.2 — OS Hardening — 2026-06-29
**Type:** Repository / documentation (no store changes)
**Sprint:** [Sprint 0.5 — OS Hardening](../backlog/sprint-00-5-os-hardening.md)

**Summary:** Strengthened the operating system before any website development so future decisions are commercially driven, not technically driven.

**Shipped:**
- `docs/00-north-star.md` — mission, vision, principles, brand promise, definition of success, non-negotiables, decision framework (the repo's highest authority).
- `docs/00-business-principles.md` — ~20 operating principles.
- `scorecards/` — Opportunity Scoring Framework plus Business Health, Website Audit, Marketing and Sprint Review scorecards.
- `research/` — 8 structured, documented folders (competitors, customer psychology, ecommerce best practice, gift market, seasonal campaigns, fashion trends, Meta advertising, CRO research).
- Opportunity Scoring wired into the feature-request template and a ranked `backlog/README.md` — **all backlog items must be scored and ranked before implementation.**
- README updated (structure, working principles, Definition of Done).

**Business impact:** Improves decision quality and commercial discipline; no direct revenue impact (foundation).
**KPIs affected:** None directly; improves the decisions that drive every KPI.
**Store changes:** None (by design).

---

### v0.1 — Foundation (Operating System) — 2026-06-29
**Type:** Repository / documentation (no store changes)
**Sprint:** [Sprint 0 — Foundation](../backlog/sprint-00-foundation.md)

**Summary:** Created the Edge Scarves OS repository — the single source of truth for the business. Established the full documentation structure, the AI specialist team, sprint methodology, development standards, KPI definitions and the roadmap.

**Shipped:**
- `README.md` — vision, principles, sprint method, Definition of Done, branch/release process.
- `docs/01`–`docs/17` — business, brand, persona, commercial, product, website, CRO, Meta, email, SEO, social, Shopify architecture, AI strategy, KPIs, dev standards, roadmap, release notes.
- `prompts/` — 9 AI specialist roles (CEO, PM, Shopify Dev, CRO, Meta, Email, SEO, Content, Data).
- `backlog/` — Sprints 0–3 planned.
- `templates/` — feature request, bug report, release, weekly review, meeting notes.
- `assets/` & `screenshots/` — structured directories for brand and evidence.

**Business impact:** Enables disciplined, measurable, profit-focused development. No direct revenue impact (foundation).
**KPIs affected:** None directly; enables all future KPI movement.
**Store changes:** None (by design).

---

## Future Vision

A complete, searchable history of the business's evolution. Anyone can trace any change — a copy tweak, a flow, an ad structure — to its release, rationale and measured outcome. Release notes become institutional memory that prevents repeated mistakes and proves what works.

## Dependencies

- [`templates/release-template.md`](../templates/release-template.md) — the entry format.
- [`15-development-standards.md`](15-development-standards.md) — the release process.
- [`14-kpis.md`](14-kpis.md) — impact reporting.

## Open Questions

- Should store releases and repo releases share one log or be split? (Currently unified.)
- What is the minimum impact-measurement window before a release is considered validated?

## Action Items

- [ ] Append an entry for every merged release.
- [ ] Revisit each release post-launch to record actual vs. expected impact.

---

**Status:** 🟢 Active
**Last Updated:** 2026-06-29
**Owner:** Project Manager prompt
