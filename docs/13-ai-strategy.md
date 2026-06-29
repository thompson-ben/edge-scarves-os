# 13 — AI Strategy

## Purpose

Define how Edge Scarves uses AI (Claude and the specialist prompt team) as an operating capability — not a gimmick. AI is the leverage that lets a lean business run like a full team: research, drafting, analysis, code, and review at speed. This document sets how AI is used, governed and measured.

## Current State

**The AI team.** Specialist roles are defined as system prompts in [`/prompts`](../prompts):
- CEO (profit guardian), Project Manager, Shopify Developer, CRO Specialist, Meta Specialist, Email Specialist, SEO Specialist, Content Writer, Data Analyst.

**Operating model**
- Claude works as a disciplined team member following the active specialist prompt and the relevant doc(s).
- All AI work follows the repository's Working Principles and Definition of Done ([`README.md`](../README.md)).
- The **CEO mandate overrides** all other prompts: reject work that does not defend or grow net profit.

**Governance (rules)**
1. **Never invent business facts.** Use `TODO`; surface assumptions and open questions.
2. **Human-in-the-loop for irreversible/outward-facing actions** (live store changes, ad spend, sending to customers).
3. **No live Shopify changes during foundation work.**
4. **Cite evidence.** Recommendations reference data or are labelled as assumptions.
5. **Brand-safe.** All customer-facing output matches [`02-brand-strategy.md`](02-brand-strategy.md).

**Current AI use-cases (in scope now):** documentation, research, analysis frameworks, copy drafting, code drafting + review, sprint planning.

**Tooling:** Claude Code (this repository). Other AI tools (e.g. on-platform Shopify Magic, content tools): TODO evaluate.

## Future Vision

AI is embedded in every workflow: drafting and reviewing store code, generating and ranking CRO hypotheses, producing ad/email/content variants, analysing performance data into recommendations, and maintaining this knowledge base. The specialist prompts evolve with the business. AI multiplies the founder's output while the CEO mandate and human-in-the-loop controls keep it profit-focused and brand-safe.

## Dependencies

- [`/prompts`](../prompts) — the specialist definitions.
- [`15-development-standards.md`](15-development-standards.md) — code/review standards AI must follow.
- All strategy docs — the context AI operates within.

## Open Questions

- Which workflows give the highest leverage from AI first?
- What human-approval gates are required for each outward-facing action?
- Which additional AI tools (if any) are worth adopting?
- How do we measure AI's contribution to output/quality?

## Action Items

- [ ] Keep the specialist prompts current as the business learns.
- [ ] Define explicit human-approval gates per outward-facing action.
- [ ] Identify the top 3 highest-leverage AI workflows to formalise.
- [ ] Evaluate complementary AI tooling.

---

**Status:** 🟢 Active — AI team defined in `/prompts`
**Last Updated:** 2026-06-29
**Owner:** Claude (Lead Technical Architect) / Ben Thompson (Founder)
