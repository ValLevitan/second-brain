# Meeting Summary — Daily Standup meeting
**Date:** November 25, 2026, 3:46 AM Eastern
**Duration:** about 40 minutes of talk
**Attendees:** Pavel Frolov, Irina Shishko, Dzmitry Chudzinau, Andrei Bosik, Sergey Tsimanov, Alexander Biratko, Anton Seregin, Vladimir Samusenko, Dmitri Kovalchuk, Alexey Khamin, Ivan Shpak
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_BEP_Cleanup_and_Port_Update_Requirements-November-25-2026]]

## Summary

**Firmware tests (Alexey).** Yesterday he tested Flex updates by hand: updates, cash in and cash out, and update through the server. All worked, except going back to the previous release. Today he will make a broken firmware on purpose. He expects the device to fall back to the previous version after the failed update. He keeps reviewing the firmware repository. He saw about 10 to 15 branches that are merged but not deleted. Irina said she deleted hers and will check again.

**Emma (AI-PM bot) creates duplicates.** Alexey saw a story where the author and the assignee are the same person. Andrei Bosik will check this. Pavel saw two cases where Emma created very similar features. Andrei said Emma already checks for duplicates before she creates something. Dmitri asked everyone to send concrete pairs of duplicate features, so the team can find the cause. Andrei is not sure Emma should be allowed to create capabilities.

**NOVA requirements (Alexander).** He finished the review of all capabilities in IP-481. He sent them to Daniil, Igor and Zhenya to check if they are done. Some are already solved in the engine and framework and can be closed. Next he will write the missing requirements for the studio and for the engine. The engine has almost no good capabilities. He also created a capability for a studio phase (name heard unclearly). The three port tasks from Irina are done. He will take a port from Irina to run tests. Irina asked if the engine should be tested alone. Pavel said yes: with good engine autotests, a bug can be fixed in the engine only, without retesting the whole product.

**4:00 meeting on capabilities and requirements.** Irina said a meeting at 4:00 covers this topic. Dzmitry Chudzinau is not invited. Alexander said this is bad and will bring him in. Dzmitry agreed. Alexander said the meeting came from a talk between Zhenya and Val yesterday.

**Power loss during update (Anton Seregin).** Anton made a fix for the port: the old loader now refuses the update. He is still blocked on two items. Item 128: how to count some counters in the test after a restore. Item 130: if power is cut during an update, the port recovers and updates, but the terminal does not learn about the failure. The requirement says it should. Pavel said this has little value. It costs time for one developer and one autotest writer. Adding update states to the firmware looks like a separate MVP and makes the design more complex, which raises the chance of failure. Grafana logs show two download starts, so the failure can be seen by indirect signs. Vladimir and Irina said: propose the change in the requirement (for example in red text) and ask the owner to approve. The requirement owner is Andrei Klimovich (acceptance criterion 4). Anton will add a comment to the requirement.

**Dzmitry.** He finished some MVP 2 items and is studying capability 365 (number heard unclearly). Pavel said there is an MVP 2.1 status meeting today. Dzmitry said his part is closed.

**Sergey.** He reviewed the 2.2 capabilities. He is making a new release of the port firmware. He is also doing Ivan's fixes in parallel. Nothing was uploaded to production yesterday. He said he was told to "do it where you want", and then Philip may not like the result on STG. Pavel said requirements must be clear.

**BEP project must not be used (Dzmitry, Dmitri, Ivan).** Items are still created in the BEP project. Dzmitry: the standard now gives each repository its own feature prefix. Dmitri: projects like BEP must not be used, and everything there will be deleted. Irina said BEP should be closed for new items. Ivan will move his stories to the CMS project. Dzmitry: Ivan's job is stories; developers create capabilities and features. Stories with no parent are a problem, and Val will send emails if he finds them. Pavel: for old projects with no capability, create a new capability, even for small changes. Irina showed capability 253 living under IP-747. Dzmitry leads the legacy capabilities in IP-435. Irina will move it to 435. Pavel: RAGE and CMS/NOVA will each have their own capabilities. He said order must be restored.

**Vladimir.** Tickets 116 and 107 are in review; he took 108. He will slow down today because only 10% of his Claude limit is left. One ticket takes one to two days with all checks and review rounds. Pavel asked about giving him another account. Dmitri said the account could be banned. Andrei Bosik said each person has a reset button in Claude Desktop. Vladimir said he pressed it twice and it failed; he will press it if he must. Andrei will look at it again. Vladimir also made a "standards" plugin that reminds you of team standards. It has been in the team marketplace for two weeks with a readme. He will send the two lines of install code in the chat.

**Infrastructure (Andrei Bosik).**
- He sent emails yesterday: the GitHub application setup changed on main in all repositories. He did not change branches, because that would break them. The email has text for Claude to update a branch. There are many old branches; the branch report shows them.
- He cleaned many variables. Some are still used by dead code. Dzmitry needs to remove dead code in his legacy project first, and this needs a capability. Andrei will create the capability for Dzmitry, then delete the variables.
- Cluster updates continue (more than 100). He hopes to finish by New Year. Today there may be short drops of up to 2 minutes.

**Other.** Irina will finish the autotests for 2.1. Ivan continues with RIS; Zhenya released fixes, and Ivan will rebuild and check. Zhenya sent Pavel questions about a modem; it needs a SIM card, and Ivan will come to Pavel for the modem. Pavel will prepare the RK3576 so Zhenya can use it for the new installer. The Flex IQ MVP 2.1 release is today on paper, but Irina said it will not happen today. Pavel thinks MVP 2.1 will go on all devices, because MVP 1 is not installed yet, and 2.1 allows remote firmware updates. Some devices have no Wi-Fi module, so wires are still needed. Dmitri reminded about deadlines; Anton has the most. Anton and Vladimir said Emma did not move their dates when asked. Dmitri asked both for screenshots.

## Decisions Made

- **The BEP project is not used. New items go under each repository's own prefix. Everything in BEP will be deleted.** (Decided by Dmitri Kovalchuk and Dzmitry Chudzinau)
- **Changes to old projects get a new capability, even small ones.** (Decided by Pavel Frolov)
- **The power-loss-during-update case is not built now. Anton comments on the requirement that the failure is seen by indirect signs; the owner approves.** (Decided by Pavel Frolov; Anton agreed)
- **Dead-code removal needed to delete GitHub variables goes through a capability.** (Decided by Dzmitry Chudzinau; Andrei Bosik agreed)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexey Khamin | Make a broken firmware and check the device falls back after a failed update | Nov 25, 2026 | High | Return to previous release still not working |
| 2 | Irina Shishko | Check again that merged branches in the firmware repository are deleted | TBD | Low | 10 to 15 branches seen |
| 3 | Andrei Bosik | Check why Emma sets the same person as author and assignee | TBD | Normal | |
| 4 | Everyone | Send Dmitri concrete pairs of duplicate features created by Emma | TBD | Normal | |
| 5 | Anton Seregin, Vladimir Samusenko | Send Dmitri screenshots of Emma chats where dates were not moved | TBD | Normal | |
| 6 | Anton Seregin | Review his deadlines | TBD | Normal | Dmitri's reminder |
| 7 | Alexander Biratko | Bring Dzmitry Chudzinau into the 4:00 capabilities and requirements meeting | Nov 25, 2026 | Normal | |
| 8 | Alexander Biratko | Write the missing studio and engine requirements; run tests on a port from Irina | TBD | Normal | |
| 9 | Anton Seregin | Comment on the power-loss requirement (acceptance criterion 4) and ask Andrei Klimovich to approve | TBD | High | Blocks item 130 |
| 10 | Ivan Shpak | Move his stories from BEP to the CMS project | TBD | Normal | |
| 11 | Irina Shishko | Move capability 253 from IP-747 to IP-435 | TBD | Normal | |
| 12 | Andrei Bosik | Create a capability for Dzmitry to remove dead code, then delete the variables | TBD | Normal | |
| 13 | Andrei Bosik | Finish cluster updates | Dec 31, 2026 | Normal | "By New Year" |
| 14 | Andrei Bosik | Look again at the Claude limit reset button | TBD | Normal | Failed twice for Vladimir |
| 15 | Vladimir Samusenko | Send the "standards" plugin install code in the chat | Nov 25, 2026 | Low | |
| 16 | Sergey Tsimanov | Make the new port firmware release and Ivan's fixes | TBD | Normal | |
| 17 | Irina Shishko | Finish the autotests for 2.1 | TBD | Normal | |
| 18 | Ivan Shpak | Rebuild RIS with Zhenya's fixes and check; get the modem from Pavel | TBD | Normal | |
| 19 | Pavel Frolov | Prepare the RK3576 for Zhenya's new installer | TBD | Normal | |

## Open Questions

- Item 128: how to count the port counters in the test after a restore. Anton waits for answers.
- Whether Emma should be allowed to create capabilities. Andrei Bosik is not sure.
- Whether Vladimir should get another Claude account. Dmitri warned about a ban; no final answer.
- Whether MVP 2.1 goes on all devices at release. Pavel thinks so; not decided.
- Names and terms heard unclearly: the studio phase Alexander created a capability for ("холпов/хупов"), "capability 365" (Dzmitry), "полиса клиру" (Alexander), "IP ему/мма" (taken as Emma), "Влик спорт флег хайкью" (taken as Flex Port / Flex IQ), "ЦСЦЕ/смеси" (taken as CMS), "рейч/рейд" (taken as RAGE), "2 модем" (which modem), "Philip" and "STG".

## Dispatch Log

---
*Processed from Teams transcript on November 25, 2026, ~12:30 PM Eastern*
*Source meeting: Daily Standup meeting*
