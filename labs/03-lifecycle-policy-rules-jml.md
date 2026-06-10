# Lab 3 — Lifecycle Policy Rules (JML)

## Objective

Configure the policy rules that automate the joiner-mover-leaver (JML) lifecycle so access is granted, adjusted, and revoked without a human clicking anything.

## What I did

- **Joiner / birthright rules** — grant day-one access automatically the moment a new identity lands from the HR feed.
- **Mover / transfer rules** — re-evaluate access when someone changes roles or departments, adding what the new role needs and removing what the old role had. Yesterday's access is tomorrow's audit finding.
- **Leaver / termination rules** — end-date and termination rules that pull access the moment employment ends. This is the gap where ghost accounts live.

## Key concepts

- **Manual deprovisioning does not scale and does not hold up in an audit.** Rules do.
- The leaver flow is the highest-risk part of the lifecycle: a terminated employee with live access is a breach waiting for a headline.
- Mover logic is the subtle one — access accumulation from role changes ("permission creep") is invisible without automated re-evaluation.

## Skills demonstrated

Lifecycle policy configuration, birthright provisioning, transfer-based access re-evaluation, automated deprovisioning, JML automation design.
