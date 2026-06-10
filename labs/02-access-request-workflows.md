# Lab 2 — Access Request Workflows

## Objective

Build three access request workflows in Saviynt, each calibrated to a different risk tier, and follow a request through to fulfillment.

## What I did

Built and tested three approval models:

1. **Auto-approval** — for low-risk, birthright-style access. No human sits in the path of a request that should always be granted.
2. **Single-level manager approval** — for standard access. The manager owns the decision.
3. **Two-level risk-based approval** — for access that can actually hurt the organization. More eyes and more friction, deliberately.

Then configured **fulfillment**, where an approved request becomes a real provisioning task — for both connected apps (automated push to target) and disconnected apps (manual fulfillment task with verification).

## Key concepts

- **The workflow is a control.** Approval friction should match the risk of the access, not the org chart.
- Over-approving low-risk access creates rubber-stamp fatigue; under-approving high-risk access creates audit findings. Tiering solves both.
- A request isn't done at approval — fulfillment is where governance meets the actual target system.

## Skills demonstrated

Workflow design, approval policy configuration, risk-tiered access models, provisioning fulfillment for connected and disconnected applications.
