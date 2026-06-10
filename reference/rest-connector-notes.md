# Saviynt EIC — REST Connector & Three-Tier Model Notes

Working notes from connector study alongside the L100 labs.

## The three-tier model

| Object | Role | Example |
|--------|------|---------|
| **Security System** | Top-level container for the application: metadata, entitlement types, password policy, which Connection to use | "Workday" |
| **Endpoint** | A specific instance of the app: account naming, requestable status, owner, config overrides | "Workday-Prod", "Workday-UAT" |
| **Connection** | How to technically reach the target: URLs, credentials, REST/SOAP JSON blocks, JDBC strings | OAuth2 connection to the Workday API |

**Why split?** Separation of concerns — swap Endpoints without rebuilding the Security System; rotate credentials in the Connection without touching either.

## Connector types

- **REST** — modern SaaS targets with JSON APIs; config-driven via JSON blocks. Most common today.
- **SCIM 2.0** — standardized provisioning; cleanest when the target supports it.
- **JDBC** — direct database read/write for legacy apps with no API. Risk: bypasses app business logic.
- **AD / LDAP** — directory targets over LDAP protocol.
- **Flat file** — CSV import; common for HR feeds.
- **SOAP** — older XML APIs (SAP, legacy).
- **Custom** — Java extension; last resort.

## Reconciliation vs. provisioning

**Reconciliation (target → EIC):**

- *Full recon* — pulls everything; slow but definitive. Initial load, post-schema-change, periodic backstop.
- *Incremental recon* — watermark-based (e.g., `lastModified > timestamp`); fast, run daily. Risk: misses deletions if the target doesn't track them — which is why you keep a periodic full recon.

**Provisioning (EIC → target)** is triggered by: approved access requests, role assignment, birthright rules on joiner, leaver workflows, SoD auto-revokes, and attribute-change rules.

## Key REST connector JSON blocks

| Block | Purpose |
|-------|---------|
| `ConnectionJSON` | Auth + base URL (e.g., OAuth2 client credentials with token refresh via `tokenResponsePath`, `maxRefreshTryCount`) |
| `ImportAccountEntJSON` | Pull accounts/entitlements — `listField` (where the array lives), `keyField` (dedup key; null = record silently dropped), `colsToPropsMap` (target field → EIC field mapping), `pagination` |
| `CreateAccountJSON` / `UpdateAccountJSON` / `DeleteAccountJSON` | Provisioning calls |
| `AddAccessJSON` / `RemoveAccessJSON` | Entitlement assignment/revocation |
| `StatusAndThresholdConfig` | HTTP success/failure codes and recon abort thresholds |

## Debugging patterns worth memorizing

**"Recon imported 0 records"** — check Job History stack trace. Usual suspects in order: target field renamed (breaks `colsToPropsMap`), `keyField` null in response (records silently dropped), expired/rotated credentials, pagination misconfigured, wrong `listField` path.

**"Recon imported half the users"** — almost always pagination. The target returned one page and the connector never asked for the next. The #1 cause of "only first 100 users imported" tickets.

**"Provisioning task failed"** — read the HTTP code: 400 = payload schema mismatch, 401 = auth, 403 = service account lacks target permissions, 409 = duplicate (recon out of sync), 500 = target-side issue.
