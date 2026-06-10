# Saviynt L100 Hands-On Labs

Hands-on lab work completed in a Saviynt Enterprise Identity Cloud (EIC) training environment, covering the core Identity Governance and Administration (IGA) lifecycle end to end — from onboarding applications into the Identity Warehouse through access requests, lifecycle automation, certifications, and the intelligence layer.

**Author:** Darrion Wright
**Environment:** Saviynt EIC (L100 training tenant)
**Focus areas:** IGA, JML lifecycle, access governance, certification campaigns, identity analytics

## Labs

| # | Lab | Key topics |
|---|-----|-----------|
| 1 | [Identity Warehouse & Application Onboarding](labs/01-identity-warehouse-app-onboarding.md) | Authoritative sources, connected vs. disconnected apps, aggregation, account correlation |
| 2 | [Access Request Workflows](labs/02-access-request-workflows.md) | Auto-approval, manager approval, risk-based multi-level approval, fulfillment |
| 3 | [Lifecycle Policy Rules (JML)](labs/03-lifecycle-policy-rules-jml.md) | Birthright access, transfer rules, termination/deprovisioning automation |
| 4 | [Certification Campaigns](labs/04-certification-campaigns.md) | Manager, entitlement-owner, and application-owner campaigns; audit evidence |
| 5 | [Intelligence & Trust Scores](labs/05-intelligence-trust-scores.md) | SQL analytics, orphan account remediation, intelligent recommendations, trust scoring |
| 6 | [Administrator Functions (Transport)](labs/06-administrator-functions-transport.md) | Export packages, import preview, environment promotion, change management |

## Reference

- [REST Connector & Three-Tier Model Notes](reference/rest-connector-notes.md) — Security System / Endpoint / Connection model, connector types, reconciliation vs. provisioning, REST connector JSON configuration, and common debugging patterns.

## Why this matters

These labs walk the full IGA control surface that enterprises rely on: getting identity data right at the source, putting the right friction on access decisions, automating the joiner-mover-leaver lifecycle so deprovisioning never depends on a human remembering, producing audit-ready certification evidence, using analytics to find the risk nobody requested, and promoting tested configuration between environments with proper change management.

Lab screenshots from the live environment are linked in each write-up via my [LinkedIn lab series](https://www.linkedin.com/in/darrion-wright-2691402ab/recent-activity/all/).
