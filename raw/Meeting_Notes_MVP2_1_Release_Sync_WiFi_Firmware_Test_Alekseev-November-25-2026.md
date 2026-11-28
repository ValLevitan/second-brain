# Meeting Summary — MVP2_1 release sync
**Date:** November 25, 2026, 9:51 AM Eastern
**Duration:** ~46 minutes
**Attendees:** Andrei Klimovich (organizer), Val Levitan, Pavel Frolov, Irina Shishko, Dzmitry Chudzinau (left at ~15 min), Sergey Tsimanov
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026]]

## Summary

**Wi-Fi module update cannot be tested in Minsk.** Irina: the team cannot test the update of the Wi-Fi module together with the port firmware. Pavel: only Evgeniy Alekseev has the newest Flex Port board revision with the Wi-Fi module soldered in. In Minsk the module is flashed by outside tools; on the real board it is wired to the processor. Alekseev built the firmware that flashes the Wi-Fi module with the main processor. Pavel gave him the firmware and a description; the ball is on his side. Val: send hardware from China to Minsk (new Flex Ports); Pavel: Minsk needs only the new Flex Ports, not IQ. Val: this is already being invoiced, but it will take about a month.

**Help for Alekseev.** Pavel: the Flex IQ emulator can send firmware; Alekseev must learn to use it. Anton Seregin used it most. Dzmitry: Anton can write a detailed instruction. Pavel: our undertaking, tomorrow or the day after at most, because Alekseev has most time on the weekend. Andrei: Alekseev sent 6 boards last week with Wi-Fi modules he installed by hand; Pavel confirmed he still has some.

**2.1 cannot close without this test.** Val asked if MVP 2 cannot go live until Alekseev tests. Pavel: yes, this is one blocker. 2.1 cannot close until board update, including the Wi-Fi module, is confirmed. The second blocker is the remaining autotests. Irina (after talking to Vladimir and Anton): autotests need time until the end of this week.

**Conflicting requirements.** Irina: delays come partly from missing or conflicting requirements, which the team must rewrite during work. Val: Andrei, as requirements owner, should groom them all the time, for example with an agent that reads all requirements and flags conflicts or repeats, before Irina finds them. Andrei: he processes the team's overnight comments every day with an agent; most comments come from developers working on a requirement, and he cannot catch these early. Val: conflict between developer and product owner is healthy. Pavel: an automatic agent should cross-check all linked capabilities. Andrei: he already checks for new conflicts when he edits. Dzmitry: proposed a specification per release (a fixed list of requirements, not editable after release); he is preparing a document and wants a separate meeting. Val agreed: separate meeting, other topic. Andrei: he will review his conflict agent again; before 2.2 planning everything must be clean. After MVP 1 and 2.1 are released, he wants a full meeting on process changes.

**Dzmitry left.** No questions on 2.1. On 2.2 he answered Andrei's comments and waits for answers; 2.2 review is going on.

**2.1 scope is fixed.** Pavel: scope is fixed; nothing will likely be added or removed. Irina: no questions on 2.1 except the Wi-Fi test and finishing autotests. For 2.2 she wants the same clear list of what is released. Andrei, for Val, in short: Flex Ports connect to IQ by Wi-Fi; all Flex Ports update remotely; IQ gets split goods (money not only to a debit card) and support phone numbers. Irina: inspector reports are in 2.2, not 2.1. Main three: Wi-Fi, remote port update, split goods. Andrei confirmed the list Val's Claude made from Jira (bold headings correct). Sergey: items 1 and 2 are the same.

**Remote update without Wi-Fi.** Andrei: Wi-Fi with IQ must be tested on the hardware used at locations. Pavel: new boards reach Minsk in about 3 weeks; after Alekseev checks, Georgia can flash remotely or by USB. Current boards without Wi-Fi must also update remotely; this can be tested on current boards.

**Alpha build on Saturday.** Pavel proposed an alpha build to test what does not need Wi-Fi: remote updates, split goods on Flex IQ, new screens, new TITO ticket format with small barcode. Andrei: the first location install is Friday, if all goes as planned. If Minsk gives an alpha build Saturday morning Eastern, he can test it Saturday. Pavel: no problem.

**Jira dates.** Irina: 2.1 end date in Jira is the 25th. Val read the Jira filter as all leading to capability 146; Pavel and Irina: no, all capabilities in request or in progress are equal. The filter was wrong (release name is "MVP 2_1"). Irina listed capabilities 159, 234, 289, 371. 242 is not 2.1. 397: Pavel updated it, Dima committed, date set to today. The latest date shown is November 30 (capabilities 145 and 287); 145 is the Wi-Fi tests. Irina: all 5 of these capabilities depend on autotests, which were not finished today, so they all need new dates.

**Alekseev's task.** Capability 399, feature 258, in progress, due today. Pavel: ask Alekseev if he can do it today or set the weekend. Val: write in the definition of done what he must test. Pavel added an extra item: after the update, check that the module at least scans the network.

**What to send to Minsk.** Val took this on and asked the team to list exact items. Pavel: new-revision Flex Port with Wi-Fi module, as a full assembly (touchscreen, scanner), to avoid problems later. Val: Pavel will contact Alekseev, and the schedule will change based on that. Pavel: if it works at once, the check takes 5 minutes; maybe tomorrow morning.

**2.2 scope.** Val showed his Claude's summary of 2.2. Andrei: looks correct; he will add the location onboarding email (fix addressee and disclaimers), from the email he sent yesterday. Irina asked for the time frame, because it decides what fits. Jira 2.2 dates are not set or old. Val: for 2.2 there is not even a schedule yet.

## Decisions Made

- **2.1 scope is fixed.** — Nothing added or removed. (Pavel, Irina)
- **2.1 does not close until Alekseev confirms the board update includes the Wi-Fi module, and autotests are done.** (Pavel, Val)
- **Minsk gives Andrei an alpha build Saturday morning Eastern to test non-Wi-Fi features.** (Andrei, Pavel)
- **Extra definition-of-done item on Alekseev's task: after update, module must scan the network.** — Added during the meeting. (Val, Pavel)
- **Minsk gets full assembled new-revision Flex Ports with Wi-Fi module.** (Val, Pavel)
- **Requirements process and release specification go to a separate meeting.** (Val, Dzmitry, Andrei)
- **Location onboarding email fix goes into 2.2.** (Andrei)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Anton Seregin (named by Pavel and Dzmitry) | Write a detailed instruction for the Flex IQ emulator for Alekseev | Nov 26–27 | High | Pavel: "tomorrow, the day after at most" |
| 2 | Evgeniy Alekseev | Test Wi-Fi module flashing with port firmware (capability 399, feature 258), incl. network scan | Nov 26 morning or weekend Nov 28–29 | High | Not in the call; blocks 2.1 |
| 3 | Pavel Frolov | Contact Alekseev; update the schedule based on the result | TBD | High | |
| 4 | Pavel Frolov (Minsk team) | Deliver alpha build (remote update, split goods, new screens, new TITO ticket) | Nov 28 morning Eastern | High | |
| 5 | Andrei Klimovich | Test the alpha build | Nov 28 | High | First location install Friday Nov 27 |
| 6 | Irina Shishko (QA, with Vladimir and Anton) | Finish 2.1 autotests; set new dates on the 5 capabilities | End of week (~Nov 27–29) | High | |
| 7 | Val Levitan | Send new-revision Flex Ports (full assembly) from China to Minsk | TBD (~1 month) | Normal | |
| 8 | Andrei Klimovich | Review his conflict-check agent; requirements clean before 2.2 planning | Before 2.2 planning | Normal | |
| 9 | Andrei Klimovich | Add location onboarding email fix (addressee, disclaimers) to 2.2 | TBD | Normal | |
| 10 | Dzmitry Chudzinau | Set up separate meeting on release specification; review document with Sergey | TBD | Low | Andrei: full process meeting after MVP 1 and 2.1 release |
| 11 | [Unassigned — needs clarification] | Set dates on 2.2 capabilities in Jira | TBD | Normal | Val: no 2.2 schedule yet |

## Open Questions

- Real 2.1 release date: Jira says Nov 25, but autotests need until end of week and some dates show Nov 30. (Irina, Pavel, Val)
- 2.2 time frame — Irina needs it to know what fits. (Irina, Val)
- Heard unclearly: "FI ku 251" (Pavel: item due Nov 30 on Dima); "afort 258" (feature under capability 399); "402 2 a" (Andrei's name for the board/assembly in MSBC); "Artem" (person on capability 145); "Vladimir" and "Anton" (Irina's testers — surnames not said).

## Dispatch Log

---
*Processed from Teams transcript on November 25, 2026, ~12:30 PM Eastern*
*Source meeting: MVP2_1 release sync*
