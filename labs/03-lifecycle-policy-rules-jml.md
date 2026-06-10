# Lab 3 — Lifecycle Policy Rules (JML)

![Technical Rules configured in Saviynt EIC — birthright rules creating accounts and assigning responsibilities based on user city](../images/lab3-technical-rules.jpg)

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

## Lab evidence

Screenshots of this lab (technical rules, pending provisioning tasks, the User_Transfer update rule, and the leaver remove-access task) are in my LinkedIn write-up: [Identity Lifecycle Policies post](https://www.linkedin.com/feed/update/urn:li:activity:7468656996100100096/)
