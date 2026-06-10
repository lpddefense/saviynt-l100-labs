# Lab 5 — Intelligence & Trust Scores

## Objective

Work the intelligence layer of Saviynt EIC — the analytics and risk-scoring capabilities most implementations never touch.

## What I did

- **SQL analytics** — wrote analytics queries to surface **orphan accounts** (accounts with no owner), then deprovisioned them directly from the report. Detection to remediation in one flow.
- **Intelligent recommendations** — configured recommendations so access requests suggest the right entitlements based on peer access patterns, instead of making requesters guess.
- **Trust scoring** — configured trust scores that turn distributed risk signals into a single number you can act on.

## Key concepts

- Identity governance is shifting from *"who approved this?"* to *"what does the data say about this?"* The intelligence layer is where that shift happens.
- Orphan accounts are the canonical invisible risk: live access, no owner, no requester — nothing in the request/approval pipeline will ever catch them. Only analytics will.
- Recommendations reduce both friction (users find the right access faster) and risk (fewer over-scoped "just give me what my coworker has" requests).

## Skills demonstrated

Identity analytics, SQL-based reporting, orphan account detection and remediation, intelligent access recommendations, risk/trust score configuration, CSV report export for audit handoff.

## Lab evidence

Screenshots of this lab (the analytics configuration with the SQL query, analytics history for orphan accounts of Siebel MRM, and the map/delete remediation actions) are in my LinkedIn write-up: [Intelligence and Analytics post](https://www.linkedin.com/feed/update/urn:li:activity:7469740157857005568/)
