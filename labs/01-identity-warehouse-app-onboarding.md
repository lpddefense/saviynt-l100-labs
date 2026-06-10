# Lab 1 — Identity Warehouse & Application Onboarding

## Objective

Build out the Identity Warehouse from scratch: establish the HRMS as the authoritative identity source, then onboard applications on top of it and correlate accounts back to identities.

## What I did

- Configured the HRMS feed as the authoritative source for identities, making it the system of record that every downstream application inherits from.
- Onboarded a **connected application** (Active Directory) that reconciles live against the target.
- Onboarded **disconnected applications** via flat-file import, where accounts and entitlements have no live link to the target and must be loaded and validated manually.
- Ran aggregation jobs to pull accounts and entitlements into the warehouse.
- Worked through **account correlation** — tying every imported account back to an identity in the warehouse.

## Key concepts

- **Connected vs. disconnected apps behave very differently.** AD reconciles live; disconnected apps come in as flat imports that require manual validation. Both end up in the same warehouse, but the operational trust model is different.
- **Correlation is the real work.** An account that doesn't tie back to an identity is noise at best — at worst, it's a risk you can't see (an orphan account with live access and no owner).
- **Authoritative source first, applications second.** If the HRMS data is wrong, everything downstream inherits the error. Data quality at the source is the foundation of the entire governance model.

## Skills demonstrated

Identity warehouse design, application onboarding, account/entitlement aggregation, correlation rules, authoritative source configuration.
