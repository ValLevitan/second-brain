# Meeting Summary — Flex-POS Convergence Review: Session 3 Final Schedule Alignment

**Date:** April 10, 2026, 11:25 AM – 11:37 AM Eastern
**Duration:** ~12 minutes (across 2 recording segments)
**Attendees:** Val Levitan, Irina Shishko, Pavel Frolov (Dmitri addressed briefly at end)

## Summary

This was the third session in the Flex-POS Convergence Review series, focused on planning the alpha sample build for the Flex-POS product. The core issue is assembling alpha units at a location in the state of Georgia (USA), which requires aligning hardware component delivery with software readiness.

**Alpha Station Timeline and Software Delivery.** Val established that the alpha stations will be ready no earlier than April 27, 2026. This sets the deadline for delivering the alpha software version — by April 27, the software team (Irina, Pavel) must hand off an alpha build for installation on the alpha stations. Irina noted that April 20–21 are holidays (Monday–Tuesday), but April 25 (Friday) is a working day, giving them a compressed window leading up to the 27th.

**Hardware Component Hierarchy and Gennady's Role.** Val outlined the hardware dependency chain: HM 505 sits under HM 508, which sits under IP 955. Gennady (not present) needs to order 3D-printed plastic components for delivery to Georgia so that remaining parts can be shipped there for on-site alpha assembly. Val committed to speaking with Gennady separately to create a task in Jira linked to HM 505.

**Jira Task Structure Discussion.** The team debated how to represent the alpha build milestone in Jira. Val noted this isn't a feature — it's a release, but he hasn't yet figured out how to create a release in GitHub and reflect it in Jira. Pavel suggested using a milestone bar across the timeline for visibility, but Val pointed out nothing can be linked to a milestone bar. Irina referenced the Maple project as precedent: for Maple, they created a task assigned to Elizabeth for installing and verifying the build. Pavel proposed creating the task structure under the existing "Flex-POS Transition to Production" feature, with a story for Elizabeth. Val agreed.

**Elizabeth's Alpha Assembly Task.** Val assigned Elizabeth (referred to also as "Alisa") to manufacture 2 alpha samples from temporary (3D-printed) plastic between April 27–30. Pavel began creating this in Jira during the meeting as a story under "Flex-POS Transition to Production," titled something like "Assemble Alpha from 3D Plastic Casings." A follow-up task for software installation on the assembled alpha stations was noted as the next item to create.

**3D Printing Vendor Search.** Dmitri ("Dima") has been searching for 3D printing vendors and contacted approximately 20+ companies in Minsk. One vendor quoted approximately $3,500 for 3 sets (using a specific technology). A second vendor offered two options: a higher-quality variant at 8,000 Belarusian rubles (~$2,500) and a simpler variant at 2,000 rubles (~$700) for 3 sets — roughly $230 per set. Val suggested exploring vendors in China (cheapest, ship by air), Turkey, or Poland, noting that JVL has direct relationships with Chinese suppliers. Pavel cautioned that material quality must be verified before committing — the plastic must not disintegrate during the first assembly. The team agreed to evaluate the vendor proposals and material specifications before deciding.

**Meeting Close.** Val dismissed Dmitri from the meeting as his input was no longer needed. The remaining items were left for follow-up.

## Decisions Made

- **Alpha software delivery target: April 27, 2026** — aligned to alpha station hardware readiness. (Decided by Val)
- **Elizabeth to assemble 2 alpha samples from 3D plastic, April 27–30** — task created in Jira under "Flex-POS Transition to Production." (Decided by Val, implemented by Pavel)
- **Jira structure: use story under existing feature, not a release or milestone** — following Maple project precedent. (Decided collectively, Val and Pavel)
- **Evaluate 3D printing vendor proposals before committing** — must verify material durability. (Decided collectively)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val Levitan | Talk to Gennady about ordering 3D-printed plastic components (linked to HM 505) for shipment to Georgia | TBD | High | Blocks alpha assembly in Georgia — hardware components must arrive before build can start |
| 2 | Pavel Frolov | Create Jira story under "Flex-POS Transition to Production" for Elizabeth: assemble 2 alpha samples from 3D plastic, April 27–30 | April 10, 2026 | High | Being created during the meeting; needs to be finalized and assigned |
| 3 | Pavel Frolov | Create follow-up Jira task for software installation on alpha stations (after assembly) | TBD | Normal | Sequential dependency — follows alpha assembly task |
| 4 | Irina Shishko / Pavel Frolov | Evaluate 3D printing vendor proposals — verify material specs and durability before selecting vendor | Before April 27 | High | Must ensure plastic doesn't break on first assembly; multiple quotes pending |
| 5 | Irina Shishko | Deliver alpha software version to Elizabeth for installation on alpha stations | April 27, 2026 | High | Hard deadline aligned to hardware readiness |

## Engineering Signals

### Confirmed Signals
- **Possible REQ:** Val stated the need to build 2 alpha samples from 3D-printed (temporary) plastic at the Georgia location — this is a concrete product milestone for Flex-POS transition to production.

### Suspected Signals
- **Possible ADR:** Discussion about how to represent releases in Jira when the release is actually managed in GitHub — Val noted "release is done in GitHub" but unclear how to reflect it in Jira. This may warrant an ADR on release tracking tooling integration.
- **Possible REQ:** The 3D printing material must survive assembly without breaking — this implies a material durability requirement for alpha casings that isn't formally tracked.

## Open Questions

- How to create a GitHub release and reflect it in Jira — Val mentioned he hasn't learned this yet. No resolution reached.
- Final 3D printing vendor selection — pending evaluation of material proposals.

---
*Processed from Teams transcript on April 10, 2026*
*Source meeting: Flex-POS Convergence Review — Session 3: Final Schedule Alignment*