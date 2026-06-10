# Saviynt L100 Hands-On Labs

Hands-on lab work completed in a Saviynt Enterprise Identity Cloud (EIC) training environment, covering the core Identity Governance and Administration (IGA) lifecycle end to end — from first login through application onboarding, the access request system, lifecycle automation, certification, analytics, and environment transport.

This repo mirrors my Saviynt L100 lab series, posted lab-by-lab on [LinkedIn](https://www.linkedin.com/in/darrion-wright-2691402ab/recent-activity/all/). Each lab below has its own write-up with screenshots from the live environment.

**Author:** Darrion Wright
**Environment:** Saviynt EIC (L100 training tenant)
**Focus areas:** IGA, JML lifecycle, access governance, certification, identity analytics

## Labs

| # | Lab | Key topics |
|---|-----|-----------|
| 1 | [Getting Started with Identity Cloud](labs/01-getting-started-identity-cloud.md) | Global config, audit trail, Security System / Endpoint / Connection model |
| 2 | [Identity Cloud Building Blocks](labs/02-identity-cloud-building-blocks.md) | SAV roles, platform permissions, feature access, least privilege |
| 3 | [Identity Management](labs/03-identity-management.md) | Username rules, bulk user import, user records and custom properties |
| 4 | [Intelligent Application Onboarding](labs/04-intelligent-application-onboarding.md) | Connections, import jobs, entitlements, account correlation |
| 5 | [Access Request System](labs/05-access-request-system.md) | Request workflows, fulfillment, recommendations, SoD checks |
| 6 | [Identity Lifecycle Policies](labs/06-identity-lifecycle-policies.md) | Joiner birthright, mover transfer, leaver deprovisioning automation |
| 7 | [Access Certification](labs/07-access-certification.md) | Trust scoring, campaign types, audit evidence and reporting |
| 8 | [Intelligence & Analytics](labs/08-intelligence-analytics.md) | SQL analytics, orphan account remediation, custom analytics |
| 9 | [Administrator Functions (Transport)](labs/09-administrator-functions-transport.md) | Export packages, environment promotion, change management |

## Reference

- [REST Connector & Three-Tier Model Notes](reference/rest-connector-notes.md) — Security System / Endpoint / Connection model, connector types, reconciliation vs. provisioning, REST connector JSON configuration, and common debugging patterns.

## Why this matters

These labs walk the full IGA control surface enterprises rely on: getting identity data right at the source, onboarding applications with proper correlation, putting the right friction on access decisions, automating the joiner-mover-leaver lifecycle so deprovisioning never depends on a human remembering, producing audit-ready certification evidence, using analytics to find the risk nobody requested, and promoting tested configuration between environments with proper change management.
