# Meeting Summary — Daily Standup meeting
**Date:** November 24, 2026, 3:47 AM Eastern
**Duration:** about 46 minutes of talk (the recording ran until 5:33 AM Eastern)
**Attendees:** Pavel Frolov, Irina Shishko, Dzmitry Chudzinau, Andrei Bosik, Sergey Tsimanov, Alexander Biratko, Anton Seregin, Vladimir Samusenko, Dmitri Kovalchuk, Alexey Khamin, Ivan Shpak, Emma (AI-PM bot)
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Requirements_Sprawl_and_Claude_Review_Merge_Gate-November-24-2026]]

## Summary

**Requirements are getting out of hand (Dzmitry).** Dzmitry raised the main topic. Requirements in Jira are not in any system. Nobody knows how many are duplicates. Dmitri: there are about 1,100 requirements. Dzmitry built a list for the transactional product and about half were empty. Claude told him about 45% were edited after release. He gave an example of two capabilities that contradict each other (the port must block when the location is blocked, but the port must also work with the machine when there is no network). His idea: keep a product spec in GitHub (for example Flex IQ Port, with sections by type of communication), approve it by pull requests, and link Jira requirements to it. Pavel: the capability should be the spec. Dzmitry did not agree. Irina had raised the same problem a few days ago. All agreed to meet separately, find a way, and only then bring it to Val.

**Firmware update hang (Anton Seregin, Alexey, Sergey).** The update hangs when an older pre-release firmware is put over a newer one. The cause is the switch between firmware banks. Anton has a fix under test on a port: the loader refuses to switch to a pre-release version (and to version 001). He does not like the fix much. Pavel asked for a clear page that lists these cases. Anton said the page exists, and Andrei Klimovich commented that support for going back to pre-release builds is not needed. Wi-Fi module firmware will travel inside the update file (done by Alexeev, name as heard). The Minsk team cannot test that part. Irina wants a full manual cycle on Flex Port, with updates first.

**Autotests (Anton, Vladimir).** Anton's autotests are blocked by one question: which Flex Port counters stay and which reset after a restore. Andrei Klimovich passed it to Alexander Biratko. Vladimir returned tasks 233 and 116 to work after answers came; agents are writing autotests.

**NOVA (Alexander).** He is checking his recycler tasks on the stand (screens, validator in setup). He is also collecting the NOVA requirements and capabilities for engine and studio and will update them one by one. Irina will send him the capability map and the two stories given to him on Sunday. He must create the capability discussed yesterday.

**Cash-out problem at a location (Dzmitry, Irina).** Andrei wrote that cash-out does not work on production at one site. Irina: ten other machines there work; only the JVL machine does not, so look at hardware and wiring first (meters). Pavel: field installs always test with real money. The team waits for more details.

**Payment test (Pavel, Sergey).** Nathan asked the team to confirm, before 2 PM his time, that an old invoice passed through Business Central today. Pavel also got a notice of a $300 ACH on the Dwolla dev (sandbox) account and wondered if it is the same $300 as on production. Andrei Bosik said the secrets for dev and production are different and he checked them many times. The team thinks Nathan made a test invoice on dev. Pavel will look in Dwolla after the meeting.

**Infrastructure (Andrei Bosik).**
- Cluster updates today; services may lag a little.
- He removed 39 dead secrets and variables. Many more are unclear. He will write to each person in Teams and asks for fast answers. Goal: clean up by the end of the week.
- The jvlgaming.com certificate expires. He renews it today. GlassFish on the CMS will be down about 10 minutes.
- New GitHub standard, out today if he has time: a merge is blocked when the Claude review leaves a red mark. Fix it, run the review again, then merge. Pavel asked to allow a merge when someone answers the red mark with a reason. Andrei is testing the exception cases on a test repository.
- Grafana sends 100 to 150 error emails a day. Dzmitry will take this within MVP 2.2.
- Developers no longer have operating system access to the production accounting host, and access to one more production host was limited. Logs are in Grafana and CI/CD is complete. Work in the operating system goes through Andrei's team.
- The Nexus server in Minsk is still in use. Clean-up after New Year.

**Other.** Ivan has little left on RIS and moves to the GLI items; GLI answered and Irina will pass the answers. Sergey finished the update and RIS tasks and reviews the 2.2 capabilities today. Two Emma bots joined the call (one invited, one on schedule) and they talk over each other; this will be fixed. Dmitri reminded everyone about dates, and that yellow review marks are also worth fixing.

## Decisions Made

- **Requirements structure: the team meets separately, agrees on a proposal, then presents it to Val.** (Decided by Pavel, Dmitri, Dzmitry, Irina)
- **A merge must not pass with a red Claude review mark. Exceptions will be defined in the standard.** (Decided by Andrei Bosik; Pavel agreed after asking for an exception path)
- **Developers have no operating system access to the production accounting host. Such work goes through Andrei Bosik's team.** (Decided by Andrei Bosik)
- **The Minsk Nexus server stays for now and is cleaned up after New Year.** (Decided by Pavel and Andrei Bosik)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Dmitri Kovalchuk, Dzmitry Chudzinau, Pavel Frolov, Irina Shishko | Meet on how to structure requirements; bring a proposal to Val | TBD | High | About 1,100 requirements, unknown duplicates |
| 2 | Anton Seregin | Finish and verify the firmware update fix (bank switching) | TBD | High | Fix is under test on a port |
| 3 | Alexey Khamin | Run a full manual cycle on Flex Port, updates first | TBD | High | Asked by Irina |
| 4 | Alexander Biratko | Answer which Flex Port counters stay after a restore | TBD | High | Blocks Anton's autotests |
| 5 | Alexander Biratko | Update NOVA requirements and capabilities; create the capability from yesterday's meeting; take the two new stories | TBD | Normal | |
| 6 | Irina Shishko | Send Alexander the capability map and the two stories; send Ivan the GLI answers | TBD | Normal | |
| 7 | Pavel Frolov | Check in Dwolla what the $300 dev ACH was; confirm to Nathan that the old invoice passed | Nov 24, 2026, before 2 PM Eastern | High | Nathan's request |
| 8 | Andrei Bosik | Renew the jvlgaming.com certificate and update the clusters | Nov 24, 2026 | High | |
| 9 | Andrei Bosik | Publish the GitHub standard that blocks merges with a red Claude review mark | TBD | Normal | "Today if I have time" |
| 10 | Andrei Bosik | Ask each owner about unclear secrets and variables; clean up | Nov 27, 2026 | Normal | "By the end of the week" |
| 11 | Everyone | Answer Andrei Bosik's Teams questions about secrets quickly | Nov 27, 2026 | Normal | |
| 12 | Dzmitry Chudzinau | Fix the Grafana error emails within MVP 2.2 | TBD | Normal | 100 to 150 emails a day |
| 13 | Ivan Shpak | Move to the GLI items | TBD | Normal | |
| 14 | Sergey Tsimanov | Review the 2.2 capabilities, agree the requirements, take tasks | Nov 24, 2026 | Normal | |
| 15 | Andrei Bosik | Come back to the Nexus clean-up | After Jan 1, 2027 | Low | |

## Open Questions

- Standup time: the team talked about 12:00 or 11:45 Minsk time. No clear final answer in the transcript.
- Cause of the cash-out failure on the production machine. Waiting for details from the field.
- Whether the $300 on Dwolla dev is a test by Nathan. Not confirmed.
- Names as heard, not confirmed: "Alexeev" (Wi-Fi firmware), the second limited production host.
- Product and version labels were unclear in places (for example "MVP 22" is taken as MVP 2.2).

## Dispatch Log

---
*Processed from Teams transcript on November 24, 2026, ~6:25 PM Eastern*
*Source meeting: Daily Standup meeting*
