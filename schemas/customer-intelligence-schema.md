# Customer Intelligence — Data Dictionary

Design for the Customer Intelligence database ([strategy](../docs/20-customer-intelligence.md)). Four entities: **customer**, **order**, **insight_event**, **review**. Source codes (S1–S7) reference the [insight sources](../docs/20-customer-intelligence.md#deliverable-1--customer-intelligence-strategy-sources-of-insight). Privacy class: 🟢 non-personal · 🟡 pseudonymous/derived · 🔴 personal (minimise, redact, consent).

> **Derived** = computed from other records, never hand-entered (preserves traceability). All `[FACT]`s trace to a source + date.

## Entity: `customer` (one per person)

| Field | Type | Allowed / example | Source | Derived? | Privacy |
|---|---|---|---|---|---|
| `customer_id` | string (UUID/pseudonym) | `cus_8f3a…` | S1 | no | 🟡 |
| `region` | string | `UK`, `EU`, `US`, `ROW` | S1 | no | 🟢 |
| `first_seen` | date | `2026-03-04` | S1 | no | 🟢 |
| `discovery_source` | enum | `meta_ad`,`google`,`pinterest`,`organic_search`,`direct`,`referral`,`email`,`unknown` | S1, S2 | first-touch | 🟡 |
| `order_count` | integer | `3` | S1 | yes | 🟢 |
| `repeat_customer` | boolean | `true` if `order_count ≥ 2` | S1 | yes | 🟢 |
| `lifetime_spend` | decimal (GBP) | `74.50` | S1 | yes | 🟡 |
| `avg_order_value` | decimal (GBP) | `24.83` | S1 | yes | 🟢 |
| `gift_order_count` | integer | `2` | S1, S2 | yes | 🟢 |
| `avg_gifts_per_customer` | decimal | `0.67` (gift orders ÷ orders) | S1, S2 | yes | 🟢 |
| `favourite_products` | array[product_id] | top by purchase/engagement | S1, S3, S4 | yes | 🟢 |
| `customer_segment` | enum | see **Segments** below | derived | yes | 🟡 |
| `predominant_buyer_type` | enum | `gifter`,`self`,`mixed`,`unknown` | S2 + S1 signals | yes | 🟡 |
| `email_engagement` | enum | `engaged`,`passive`,`lapsed`,`none` | S3 | yes | 🟡 |
| `review_sentiment_avg` | enum/score | `positive`,`neutral`,`negative` / −1…+1 | S4 | yes | 🟢 |
| `consent_marketing` | boolean | `true`/`false` | S2, S3 | no | 🔴 |
| `consent_timestamp` | datetime | ISO 8601 | S2, S3 | no | 🔴 |
| `last_order_date` | date | `2026-05-21` | S1 | yes | 🟢 |

## Entity: `order` (one per order)

| Field | Type | Allowed / example | Source | Derived? | Privacy |
|---|---|---|---|---|---|
| `order_id` | string | `ord_…` | S1 | no | 🟡 |
| `customer_id` | string (FK) | → customer | S1 | no | 🟡 |
| `order_date` | date | `2026-05-21` | S1 | no | 🟢 |
| `order_value` | decimal (GBP) | `28.00` | S1 | no | 🟢 |
| `items` | array[product_id] | `[eco-style-hearts, …]` | S1 | no | 🟢 |
| `item_count` | integer | `2` | S1 | yes | 🟢 |
| `gift_wrapped` | boolean | `true` (standard — see note) | S1 | no | 🟢 |
| `gift_options_used` | boolean | gift message / recipient address used | S1 | no | 🟢 |
| `gift_or_self` | enum | `gift`,`self`,`unknown` | S2 + ship-to≠bill-to signal | partly | 🟢 |
| `ship_to_differs` | boolean | shipping ≠ billing name/address | S1 | yes | 🟡 |
| `discovery_source` | enum | (per order, attribution) | S1 | no | 🟡 |
| `discount_used` | boolean / code | `false` / `WELCOME10` | S1 | no | 🟢 |
| `channel` | enum | `online_store`,`other` | S1 | no | 🟢 |

> **Gift-wrap note:** wrapping is currently "standard," so `gift_wrapped` may be ~always true. The decision-useful signals are `gift_options_used` (message/recipient) and `gift_or_self`. Confirm whether wrap is always-on or selectable (Open Question, doc 20).

## Entity: `insight_event` (survey/support/social responses)

| Field | Type | Allowed / example | Source | Privacy |
|---|---|---|---|---|
| `event_id` | string | `ie_…` | — | 🟡 |
| `customer_id` | string (FK) | → customer (nullable if anonymous) | — | 🟡 |
| `order_id` | string (FK, nullable) | → order | S2 | 🟡 |
| `source` | enum | `survey`,`support`,`email_reply`,`meta_comment`,`social_dm` | S2,S5,S6,S3 | 🟢 |
| `purchase_reason` | enum/text | `gift`,`self_treat`,`replacement`,`occasion`,`other` (+ free text) | S2 | 🟡 |
| `recipient` | enum | `self`,`mother`,`partner`,`friend`,`colleague`,`other` | S2 | 🟡 |
| `occasion` | enum | `birthday`,`christmas`,`mothers_day`,`valentines`,`anniversary`,`thank_you`,`none`,`other` | S2 | 🟢 |
| `discovery_source_stated` | enum | as `discovery_source` | S2 | 🟢 |
| `free_text` | text | verbatim (redact PII) | S2,S5,S6 | 🔴 |
| `sentiment` | enum/score | `positive`,`neutral`,`negative` | derived (S4-style) | 🟢 |
| `timestamp` | datetime | ISO 8601 | — | 🟢 |

## Entity: `review`

| Field | Type | Allowed / example | Source | Privacy |
|---|---|---|---|---|
| `review_id` | string | `rev_…` | S4 | 🟡 |
| `customer_id` | string (FK, nullable) | → customer | S4 | 🟡 |
| `product_id` | string | → product | S4 | 🟢 |
| `rating` | integer | `1`–`5` | S4 | 🟢 |
| `sentiment` | enum/score | `positive`,`neutral`,`negative` / −1…+1 | derived | 🟢 |
| `themes` | array[enum] | `quality`,`packaging`,`delivery`,`value`,`gifting`,`issue` | derived | 🟢 |
| `text` | text | verbatim (redact PII) | S4 | 🔴 |
| `review_date` | date | `2026-05-30` | S4 | 🟢 |

## Customer segments (derived `customer_segment`)

Illustrative starter segmentation — refine with real data:

| Segment | Rule of thumb |
|---|---|
| `vip_gifter` | repeat + high LTV + predominantly `gift` |
| `repeat_self` | repeat + predominantly `self` |
| `one_time_gifter` | single order, `gift` |
| `one_time_self` | single order, `self` |
| `lapsed` | no order in N months |
| `prospect` | engaged (email/social) but no purchase |

## KPI derivations (link to [`docs/14-kpis.md`](../docs/14-kpis.md))

| KPI | Formula (from this schema) |
|---|---|
| Gift purchase % | `count(order where gift_or_self='gift') / count(order)` |
| Self purchase % | `count(order where gift_or_self='self') / count(order)` |
| Repeat purchase % | `count(customer where repeat_customer) / count(customer)` |
| Avg gifts per customer | `sum(gift_order_count) / count(customer)` |
| Occasion mix | distribution of `insight_event.occasion` |
| Review sentiment | share `positive` of `review.sentiment` (or mean score) |
| Gift-wrap (option) adoption | `count(order where gift_options_used) / count(order)` |

---
**Status:** 🟢 Designed (planning) · **Last Updated:** 2026-06-29 · **Owner:** Data Analyst prompt
