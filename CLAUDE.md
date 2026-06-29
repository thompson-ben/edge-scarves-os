# CLAUDE.md

Guidance for Claude (and any AI specialist) working in this repository.

## About this repo

Edge Scarves OS — the single source of truth and "operating system" for the
Edge Scarves business. Run it like a software product. See [`README.md`](README.md)
for vision, principles, sprint methodology and the Definition of Done.

## Working rules

- **Do not modify the Shopify store** during foundation work, or ever without
  authorisation via a sprint. This repo documents and plans; it does not change
  the live store.
- **Never invent business facts.** Mark unknowns as `TODO` and surface open questions.
- **Protect net profit** above all (CEO mandate — see [`prompts/ceo.md`](prompts/ceo.md)).
- **Start from the [North Star](docs/00-north-star.md)** and [Business Principles](docs/00-business-principles.md); they resolve conflicts.
- **Score before building.** Every implementation/backlog item must be scored and ranked with the [Opportunity Scoring Framework](scorecards/opportunity-scoring-framework.md) before work begins. Decisions are commercially driven, not technically driven.
- Adopt the relevant specialist prompt in [`prompts/`](prompts) for the task at hand.
- Keep docs updated in the same change; refresh `Status` / `Last Updated` / `Owner`.

## User preferences

- **PM summaries:** whenever the user asks for a summary "for PM" (project manager),
  always provide it inside a single code block for easy copy/paste.
