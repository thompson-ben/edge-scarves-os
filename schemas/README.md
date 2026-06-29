# Schemas

Data-model designs for Edge Scarves OS — the structured backbone the [Customer Intelligence](../docs/20-customer-intelligence.md) system and future implementation will build on. Schemas here are **designs, not a live database** (this is a planning sprint); they define exactly what we will capture so implementation is unambiguous.

## Contents

| File | Purpose |
|---|---|
| [`customer-intelligence-schema.md`](customer-intelligence-schema.md) | Human-readable data dictionary: every entity, field, type, allowed values, source and privacy class. |
| [`customer-profile.schema.json`](customer-profile.schema.json) | Machine-readable JSON Schema for a unified customer profile record (for future implementation/validation). |

## Principles

- **Traceable:** every stored fact links back to its source ([evidence standard](../docs/19-evidence-standards.md)); derived fields are computed, not invented.
- **Privacy-first:** pseudonymous customer IDs; minimise and redact personal data (see governance in [`docs/20-customer-intelligence.md`](../docs/20-customer-intelligence.md)).
- **Start simple, design for scale:** the model is implementable in Shopify metafields / a sheet today and a proper data store later, without redesign.
- **Source-mapped:** every field names the source(s) (S1–S7) that populate it.

**Status:** 🟢 Designed (planning) · **Last Updated:** 2026-06-29 · **Owner:** Data Analyst prompt
