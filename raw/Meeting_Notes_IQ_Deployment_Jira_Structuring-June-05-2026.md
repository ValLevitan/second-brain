# Meeting Summary — IQ Deployment Schedule Review
**Date:** June 5, 2026, 2:18 PM ET
**Duration:** ~18 minutes
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko

## Summary

Val set the deployment goal and the team worked out how to structure four new Jira items so the rollout can be tracked.

**The rollout target.** By July 15, put the first 10 IQ stations live with operators on location, with CI/CD ready so updates can be pushed and problems patched. If the first few weeks go well, add 20 more, then another 20 within 60 days — about 50 units running on location by roughly October. Val said this is a lot of first-time work and the team will have to "burn the midnight candles," but there's no choice.

**The Jira problem.** Val created four items (FP-1116 and BIP 33-06, 33-07, 33-08) but they're "hanging in a vacuum" — only due dates, no start dates, not linked into the development tree. The goal of the meeting was to link them to everything else so Val can monitor the release.

**How to structure them.** Irina and Pavel said Jira won't let these sit in the tree as plain tasks — each needs a Feature parent under the right IP. Val agreed: convert the four items to Features and park them under the project they belong to. FP-1116 goes under FlexIQ (IP-744) and covers the Flex IQ production run. 33-08 is cross-cutting (Business Central / server settings, billing integration) and will live under the billing IP, touching Andrei Bosik, Dzima Chudzinau, Nathan, and Igor.

**Testing moves to CI/CD.** Val was firm: the separate test plans are going away. Testing becomes the CD part of the release. Irina pushed back at first but it was settled.

**Credentials.** 33-06 is production credentials / GitHub Actions secrets — Andrei Bosik and Nathan to pair on it. 33-07 is per-location INCOM credentials; Pavel thinks it may not even need to be its own task, since INCOM emails credentials per location and someone (Andrei Bosik or Juan) enters them by hand. Assigned to Andrei Bosik for now.

**Logistics Val flagged.** Components for 50 units must reach Georgia; Genadi will make another trip there; Felipe must prep customers; Laura and INCOM need to know about the 10-unit release. Coordination has to be tight.

The team will take the open points away and reconvene Monday, June 8 at 9 AM.

## Decisions Made

- **Convert FP-1116, BIP 33-06/07/08 from Tasks to Features** and parent them under the correct IPs — Jira won't hold them in the tree otherwise, and Val needs the structure to monitor the release. (Val, endorsed by Pavel and Irina)
- **Testing moves into CI/CD; the separate test plans are retired.** Treat testing as the CD part of the release. (Val)
- **FP-1116 renamed** — "beta" removed because it's not a beta, it's a production run. Done live. (Val)
- **FP-1116 parented under FlexIQ (IP-744).** (Pavel)
- **33-08 to live under the billing IP** as a cross-cutting feature (integration, Dzima Chudzinau's services, Andrei Bosik, Nathan, Igor). (Pavel)
- **33-07 assigned to Andrei Bosik for now**; likely not needed as a standing task long-term. (Val/Pavel)
- **33-06 — Andrei Bosik and Nathan to pair.** (Val)
- **Reconvene Monday, June 8, 9:00 AM.** (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel | Convert the 4 Jira items (FP-1116, BIP 33-06/07/08) to Features and parent them correctly in the tree so the rollout is monitorable | Mon Jun 8 | High | This was the whole point of the meeting |
| 2 | Pavel | Talk to Genadi about the production-run hardware/tooling point | Mon Jun 8 | Normal | Components + plastic for 50 units |
| 3 | Pavel + Irina (+ Dzima Chudzinau) | Work out where 33-08 (Business Central / billing integration) sits in the Jira tree | Mon Jun 8 | Normal | Last unresolved point |
| 4 | Juan | Meet INCOM to confirm whether per-location credential provisioning is now automated (affects 33-07); Andrei Bosik to join | TBD | Normal | INCOM promised automation ~a year ago |
| 5 | Andrei Bosik | Take 33-07 — enter per-location INCOM credentials "for now" | TBD | Normal | Manual until INCOM automates |
| 6 | Andrei Bosik + Nathan | Pair on 33-06 — production credentials into GitHub Actions secrets | TBD | Normal | Secrets must be set up before the 10-unit release |

## Open Questions

- Has INCOM already automated per-location credential provisioning? (Juan + Andrei Bosik to check with INCOM.)
- Exact Jira parent for 33-08 under billing — to be settled Monday.

---
*Processed from Teams transcript on June 5, 2026*
*Source meeting: IQ_deployment_Schedule_review-June-05-2026*
