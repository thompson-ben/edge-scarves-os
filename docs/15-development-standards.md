# 15 — Development Standards

## Purpose

The engineering and documentation standards for everyone working in this repository and on the Shopify store — human or AI. Standards make work consistent, reviewable, safe and reversible. They are the contract that lets us move fast without breaking the store or the brand.

## Current State — Standards (active)

### Git workflow
- `main` is always releasable and protected; no direct commits.
- Branch from `main`, work on a branch, open a PR, review, merge.
- Keep branches focused and short-lived. Rebase/merge `main` in regularly.

### Branch naming
| Prefix | Use | Example |
|---|---|---|
| `claude/` | AI-driven work | `claude/edge-scarves-os-foundation-t4uu1z` |
| `feature/` | New feature | `feature/product-page-trust-badges` |
| `fix/` | Bug fix | `fix/cart-shipping-estimate` |
| `docs/` | Docs-only change | `docs/update-kpi-baselines` |
| `chore/` | Tooling/config | `chore/add-pr-template` |

### Commit standards
- Conventional-style prefixes: `feat:`, `fix:`, `docs:`, `chore:`, `refactor:`, `test:`.
- Imperative, present tense; explain **why**, not just what.
- Small, logical commits. One concern per commit.

### Pull requests
- Use [`templates/release-template.md`](../templates/release-template.md).
- State: what changed, why, KPI impact, how tested, rollback plan.
- Link the sprint/feature-request/bug it resolves.
- PRs are created **only when the user explicitly asks**.

### Code review expectations
- Review against these standards and the relevant doc(s).
- Check: correctness, performance, accessibility, mobile, SEO, brand consistency, reversibility.
- Prefer the smallest change that achieves the goal. Be specific and kind.

### Release process
- See [`README.md`](../README.md#release-process). Versioning: `vMAJOR.MINOR`.
- Every release updates [`17-release-notes.md`](17-release-notes.md).

### Documentation requirements
- Docs are updated **in the same change** as the work (no orphaned docs).
- Every doc carries: Purpose, Current State, Future Vision, Dependencies, Open Questions, Action Items, **Status, Last Updated, Owner**.
- Unknown facts are marked `TODO` — never invented.

### Testing checklist (store work)
- [ ] Works on mobile and desktop
- [ ] Key flows tested (PDP → cart → checkout)
- [ ] No console errors; tracking/events still fire
- [ ] Speed not regressed (Core Web Vitals)
- [ ] Accessibility checks pass (contrast, alt, keyboard)
- [ ] Tested on a dev/duplicate theme before publishing
- [ ] Rollback plan confirmed (previous theme retained)

### Performance expectations
- Mobile-first performance. Target good Core Web Vitals (LCP, CLS, INP).
- Justify every added app/script by its weight vs. value.

### Accessibility
- WCAG-minded: sufficient contrast, alt text, semantic structure, keyboard navigability, focus states.

### Mobile-first design
- Design and test for mobile first (the majority of traffic). Desktop enhances, not defines.

### SEO requirements
- Unique titles/meta, correct headings, structured data, clean canonical URLs, fast pages, descriptive alt text. See [`10-seo.md`](10-seo.md).

## Future Vision

Standards are second nature and partly automated (linting, PR templates, checklists, CI where applicable). Every change to the store and the repository is consistent, reviewed, measured and reversible. New contributors (human or AI) become productive immediately because the rules are explicit.

## Dependencies

- [`12-shopify-architecture.md`](12-shopify-architecture.md) — technical context.
- [`templates/`](../templates) — PR, feature-request and bug templates.
- [`14-kpis.md`](14-kpis.md) — the impact every change is measured against.

## Open Questions

- Should we add CI checks (link checking, markdown lint) to the repo?
- What theme-code workflow (Shopify CLI vs. GitHub integration) will we standardise on?
- Do we need a formal review SLA?

## Action Items

- [ ] Add a PR template to `.github/` (mirrors the release template).
- [ ] Decide on the theme-code version-control workflow.
- [ ] Consider lightweight CI (markdown/link lint).
- [ ] Socialise these standards with all specialist prompts.

---

**Status:** 🟢 Active
**Last Updated:** 2026-06-29
**Owner:** Shopify Developer prompt / Claude (Lead Technical Architect)
