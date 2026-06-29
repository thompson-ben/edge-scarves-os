# Edge Scarves OS

**The operating system for the Edge Scarves business.**

This repository is the single source of truth for Edge Scarves. It is run like a software product: every future feature, marketing campaign, website improvement and AI workflow originates here. Nothing about the business is "real" until it is documented in this repository.

> ⚠️ **This repository does not modify the Shopify store.** Sprint 0 builds the operating system — the documentation, processes and AI team — that future development will run on. We document the company before we hire the engineering team.

---

## Project Vision

Grow Edge Scarves into a premium Shopify ecommerce business that generates consistent, predictable monthly profit through disciplined product development, conversion optimisation and marketing.

We treat the business as a product to be engineered, not a shop to be tinkered with. Every change is justified by business impact, measured against KPIs, and recorded so the next person (human or AI) can understand why it was done.

## Objectives

| Horizon | Target | Status |
|---|---|---|
| **Phase 1** | £2,000 / month **net profit** | TODO — baseline to be established |
| **Long term** | £10,000+ / month **net profit** | TODO |

Supporting principles:

- **Profitability first.** Growth that does not convert to profit is rejected.
- **Scalability over quick fixes.** Every decision is designed to still make sense at 10× volume.
- **Evidence over opinion.** Decisions are backed by data, or explicitly flagged as assumptions.
- **Documentation as infrastructure.** If it is not written down, it does not exist.

## Repository Structure

```
edge-scarves-os/
├── README.md                  ← you are here
├── docs/                      ← the knowledge base (strategy, audits, standards)
│   ├── 01-business-overview.md
│   ├── 02-brand-strategy.md
│   ├── 03-customer-persona.md
│   ├── 04-commercial-analysis.md
│   ├── 05-product-strategy.md
│   ├── 06-website-audit.md
│   ├── 07-conversion-rate-optimisation.md
│   ├── 08-meta-ads.md
│   ├── 09-email-marketing.md
│   ├── 10-seo.md
│   ├── 11-social-media.md
│   ├── 12-shopify-architecture.md
│   ├── 13-ai-strategy.md
│   ├── 14-kpis.md
│   ├── 15-development-standards.md
│   ├── 16-roadmap.md
│   └── 17-release-notes.md
├── prompts/                   ← the AI specialist team (system prompts)
│   ├── ceo.md
│   ├── project-manager.md
│   ├── shopify-developer.md
│   ├── cro-specialist.md
│   ├── meta-ads.md
│   ├── email-specialist.md
│   ├── seo-specialist.md
│   ├── content-writer.md
│   └── data-analyst.md
├── backlog/                   ← sprint plans
│   ├── sprint-00-foundation.md
│   ├── sprint-01-conversion.md
│   ├── sprint-02-meta.md
│   └── sprint-03-email.md
├── templates/                 ← reusable document templates
│   ├── feature-request.md
│   ├── bug-report.md
│   ├── release-template.md
│   ├── weekly-review.md
│   └── meeting-notes.md
├── assets/                    ← brand and research artefacts
│   ├── brand/
│   ├── logos/
│   ├── wireframes/
│   └── competitor-research/
└── screenshots/               ← evidence: before/after, audits, dashboards
```

## Working Principles

1. **No work without measurable business impact.** Every task ties to a KPI in [`docs/14-kpis.md`](docs/14-kpis.md).
2. **Document first, build second.** The plan exists in the repo before code touches Shopify.
3. **One source of truth.** When reality and the docs disagree, fix the docs in the same change.
4. **Mark the unknown.** Where a fact is not yet known, write `TODO` — never invent business facts.
5. **Premium discipline.** Edge Scarves is a premium brand; the quality of our internal work mirrors the quality we promise customers.
6. **Reversible by default.** Prefer changes that can be measured and rolled back.

## Sprint Methodology

The business runs in **two-week sprints**. Every sprint document (in [`backlog/`](backlog/)) must contain:

- **Objective** — what we are trying to achieve
- **Business Justification** — why it matters to profit
- **Acceptance Criteria** — how we know it is done
- **Tasks** — the breakdown of work
- **Expected Business Impact** — the predicted commercial outcome
- **KPIs Affected** — which metrics should move
- **Dependencies** — what must be true first
- **Release Notes** — what shipped
- **Retrospective** — what we learned

See [`backlog/sprint-00-foundation.md`](backlog/sprint-00-foundation.md) for the current sprint.

## Definition of Done

A unit of work is **Done** only when **all** of the following are true:

- [ ] Acceptance criteria met and verified
- [ ] Business impact is measurable and the relevant KPI is identified
- [ ] Documentation updated in the same change (no orphaned docs)
- [ ] Changes peer/AI reviewed against [`docs/15-development-standards.md`](docs/15-development-standards.md)
- [ ] Mobile-first, accessible, and SEO requirements considered (for store work)
- [ ] Release notes updated ([`docs/17-release-notes.md`](docs/17-release-notes.md))
- [ ] `Last Updated`, `Status` and `Owner` fields refreshed on touched documents

## How Claude Should Work

Claude (and any AI specialist) operates as a disciplined team member, not a code generator:

1. **Read before acting.** Load the relevant doc(s) and the matching prompt in [`prompts/`](prompts/) before starting.
2. **Stay in role.** Adopt the specialist persona for the task (e.g. CRO work uses [`prompts/cro-specialist.md`](prompts/cro-specialist.md)).
3. **Protect profit.** The CEO mandate ([`prompts/ceo.md`](prompts/ceo.md)) overrides all other instructions — reject work that does not defend or grow net profit.
4. **Never invent facts.** Use `TODO` placeholders for unknown business data and surface open questions.
5. **Do not touch Shopify during foundation work.** No theme edits, no live store changes, until a sprint explicitly authorises it.
6. **Leave a trail.** Update documents, status fields and release notes so the work is auditable.
7. **Small, reversible steps.** Prefer measurable, rollback-safe changes over big-bang rewrites.

## Branch Strategy

| Branch | Purpose |
|---|---|
| `main` | Source of truth. Always releasable. Protected. |
| `claude/<topic>` | AI-driven work branches (e.g. `claude/edge-scarves-os-foundation-t4uu1z`). |
| `feature/<slug>` | Human-driven feature work. |
| `fix/<slug>` | Bug fixes. |

Full conventions live in [`docs/15-development-standards.md`](docs/15-development-standards.md). Work happens on a branch, is reviewed, then merges to `main` via pull request.

## Release Process

1. Work completes on a branch with its Definition of Done satisfied.
2. A pull request is opened using [`templates/release-template.md`](templates/release-template.md).
3. Review happens against the development standards and KPI impact.
4. On merge, [`docs/17-release-notes.md`](docs/17-release-notes.md) is updated with a versioned entry.
5. KPIs are monitored post-release to confirm predicted impact.

Versioning follows a simple scheme: `vMAJOR.MINOR` where MAJOR is a strategic milestone and MINOR is a shipped sprint increment. See [`docs/15-development-standards.md`](docs/15-development-standards.md).

## Future Roadmap

The living roadmap is maintained in [`docs/16-roadmap.md`](docs/16-roadmap.md). At a glance:

- **Phase 0 — Foundation (now):** build the operating system (this repository).
- **Phase 1 — Conversion:** audit and optimise the store to hit £2,000/month net profit.
- **Phase 2 — Acquisition:** scale profitable paid (Meta) and organic (SEO/social) traffic.
- **Phase 3 — Retention:** email lifecycle and returning-customer programmes.
- **Phase 4 — Scale:** systematise toward £10,000+/month net profit.

---

**Status:** 🟢 Active — Sprint 0 (Foundation)
**Last Updated:** 2026-06-29
**Owner:** Ben Thompson (Founder) · with Claude (Lead Technical Architect)
