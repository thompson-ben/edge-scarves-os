# 19 — Evidence Standards & Classification

## Purpose

The trust contract of the operating system. Every claim, finding and decision in this repository must be classified by **how much we actually know**, so that no strategic decision is ever mistaken for a proven fact. This document defines the four classification tiers, the labels to use everywhere, the Strategic Hypothesis structure, and how evidence is stored and traced. **Maintaining this distinction is non-negotiable** — it is what makes the OS trustworthy ([North Star](00-north-star.md) non-negotiable: "never invent facts").

> Rule of the house: **every strategic decision must be traceable back to evidence.** If you cannot point to the evidence (or explicitly to its absence), you cannot claim certainty.

## The four classification tiers

Use the label tags in **bold** inline, in tables, and in headings throughout the repo.

| Tier | Tag | Definition | Test to qualify |
|---|---|---|---|
| **Observed Fact** | `[FACT]` | Directly verified from a primary source, with citation. | "I (or the founder) saw this in a named source on a date." |
| **Reasonable Inference** | `[INFERENCE]` | A conclusion logically drawn from facts, but not directly observed. | "This follows from facts X+Y and category norms — but it is not measured." |
| **Strategic Hypothesis** | `[HYPOTHESIS]` | A strategic bet (esp. positioning/direction) that requires validation before it drives irreversible action. | "We believe this is true and it matters strategically — but it is unproven." |
| **Commercial Recommendation** | `[RECOMMENDATION]` | A proposed action with commercial justification, scored via the [Opportunity Framework](../scorecards/opportunity-scoring-framework.md). | "Given the above, do this — and here is the expected £ impact and how we'll measure it." |

**The chain.** Facts and inferences feed hypotheses; validated hypotheses and facts justify recommendations. Each step should be visible:
`[FACT] + [INFERENCE] → [HYPOTHESIS] → (validate) → [RECOMMENDATION]`

**Honesty rules**
- Never upgrade a tier without earning it. An `[INFERENCE]` is not a `[FACT]`; an unvalidated `[HYPOTHESIS]` is not a `[RECOMMENDATION]` to build at scale.
- A `[FACT]` must carry a **source + date**. Store the evidence in [`/evidence`](../evidence) and link it.
- When evidence is missing, say so explicitly (use the Evidence Required register pattern).
- Confidence is stated, not implied.

## Confidence levels

Apply to inferences and hypotheses (and to recommendations whose impact is estimated):

| Level | Meaning | Typical basis |
|---|---|---|
| 🟢 **High** | Strong, multi-source evidence; low chance of being wrong. | Several corroborating facts / measured data. |
| 🟡 **Medium** | Plausible, some evidence, material uncertainty. | One fact + category norms; partial data. |
| 🔴 **Low** | Reasoned guess; little or no direct evidence. | Inference only; no measurement. |

## Strategic Hypothesis structure (required)

Every `[HYPOTHESIS]` — including all strategic *positioning* claims — must be written with these fields:

1. **Statement** — the hypothesis in one sentence.
2. **Supporting Evidence** — facts/inferences that point toward it (cited).
3. **Contradicting Evidence** — facts/inferences that point against it (cited). *(Never leave blank — if none, say "none found yet, which is itself a gap.")*
4. **Validation Required** — exactly what we must learn to confirm/reject it.
5. **Expected Commercial Impact** — the £ prize if true.
6. **Validation Method** — how we will test it (experiment, data pull, customer research).
7. **Confidence Level** — 🟢/🟡/🔴 with one-line rationale.

A hypothesis only becomes a `[RECOMMENDATION]` to implement at scale **after** validation (or via an explicit, bounded, reversible test that is itself the validation method).

## Evidence storage & traceability

- All founder-supplied evidence lives in [`/evidence`](../evidence) (desktop, mobile, checkout, emails, analytics, competitors, customer-feedback).
- Name files so they are citable: `YYYY-MM-DD_<area>_<description>.<ext>`.
- When a claim relies on a piece of evidence, **link to the file**. The [Forensic Audit](18-forensic-ecommerce-audit.md) is a *living document* that must be updated as evidence arrives — upgrading tiers and re-scoring as certainty improves.

## Future Vision

A repository where any reader can see, for every strategic decision, the exact evidence behind it and how confident we are. Decisions improve as evidence accumulates; nothing hides behind confident prose. This is the foundation of an evidence-driven, AI-native company.

## Dependencies

- [`00-north-star.md`](00-north-star.md), [`00-business-principles.md`](00-business-principles.md) (principles 7–10).
- [`/evidence`](../evidence) (storage), [`18-forensic-ecommerce-audit.md`](18-forensic-ecommerce-audit.md) (living application).
- [`scorecards/opportunity-scoring-framework.md`](../scorecards/opportunity-scoring-framework.md) (recommendations).

## Open Questions

- Do we want a lightweight automated check that flags untagged claims in key docs?
- Should confidence levels feed the Opportunity Score (e.g., discount value by confidence)?

## Action Items

- [ ] Apply the four tags across the forensic audit and future analyses.
- [ ] Store all founder evidence in `/evidence` with citable filenames.
- [ ] Keep the audit living — upgrade tiers and re-score as evidence arrives.

---

**Status:** 🟢 Active — core trust standard
**Last Updated:** 2026-06-29
**Owner:** Data Analyst prompt / CEO prompt
