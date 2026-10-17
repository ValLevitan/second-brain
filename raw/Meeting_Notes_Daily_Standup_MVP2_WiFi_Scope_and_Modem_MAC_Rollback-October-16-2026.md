# Meeting Summary — Daily Standup meeting
**Date:** October 16, 2026, 4:46 AM – 5:20 AM Eastern
**Duration:** ~33 minutes
**Attendees:** Pavel Frolov, Alexander Biratko, Alexey Khamin, Anton Leshkevich, Anton Seregin, Daniil Stauskiy, Dmitri Kovalchuk, Evgeny Kharetski, Igor Metelski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026]]

## Summary

Held in Russian. Dima (Dzmitry Chudzinau) is on vacation and returns in about a week.

**MVP2 scope (reported by Pavel).** At yesterday's coordination meeting on the transactional product, what was called MVP2 (Flex Pay) was renamed MVP3. MVP2 now holds only two things: Wi-Fi on Flex-Ports and Flex IQ, and remote update of ports through Flex IQ. Val does not want to mix everything, because it is hard to test and launch in parallel. The next 3 weeks go to Flex IQ / port improvements, including Wi-Fi and remote update. Capabilities and requirements must be checked and missing ones created; most are non-functional, so the team can generate them. Irina will look at the MVP2 capabilities after finishing her open tests.

**Flex IQ modem MAC rollback.** Pavel and Dima made a commit that sets a MAC address on the modem when Flex IQ boots (all modems share one MAC). It does not work and breaks the modem connection. **Pavel will roll this commit back.** The same MAC on all modems is not a problem; the network keeps working. It is the lesser evil.

**Alexander.** Took FP 1335 (a loader; board name unclear in the transcript). Needs at least read access to that board's firmware repository and will request it. Took capability 138 (bezels; most ports already closed). He asked where the bezel lights for validator and printer connect. Pavel thinks they plug into the board with 2 COM ports, the same board the printer uses now; the card dispenser uses its own built-in light (it blinks when a card is ejected). Alexander will confirm with Genadi. He also needs new parameters in Terminal Hub so Flex Pay can be updated through the hub; he can add them himself with repo access. **Pavel: Alexander creates a task to add the parameters to the Terminal Hub project, with git repo access for it.**

**Alexey.** Still working on CI tests on real hardware. The AI agent created a task for him ("193" as heard); he accepted it and took it into work. The FlexPort feature for Evgeny Alekseev's memory-chip branch is created with the right parent; that capability is in progress. He also reviews and fixes incoming tests so they run on emulators.

**Anton Leshkevich.** Continues the Clover Fortune port (heard as "отлор форча"). Yesterday he generated the vertical layout and fixed resource problems from the port. Today he tests and hopes to finish. He also ported a Georgia game into the new Nebraska project; many resources are missing because Lena and the designers are still making them (Nebraska 2, horizontal). One or two more games are left to port.

**Anton Seregin.** Will close tasks 102, 103 and 129 today. Moved to a terminal where scanner and printer work together: scanning and printing at once, reprint of lost or torn tickets, printer connection, paper jam. Found that a paper jam is only seen at the next print; the screen stays as if all is fine. Sergey: alerts show only on certain screens (Home, per requirements), so the ticket did print. These cases could not be seen in emulator scenarios. Today he finishes the printer scenarios.

**Daniil.** Left the board running overnight; no more memory leaks seen, and it works a bit better. Next he gets 2 screens from Pavel. Pavel: last time the backlight on 2 screens did not turn on without pressing buttons; that should be fixed. They will prepare a test stand. The Chinese board maker keeps asking how the tests are going and if help is needed.

**Evgeny.** Analyzing RIS. Solved one question with Sergey; they may still need a call. Pavel: if not 100% sure of the answer, discuss it all together.

**Igor.** With Anton Leshkevich, adding games and resources to NAD 2 (one GPRA game, one other). The vertical Dutch Mill is done: all scenes are created. Efim packed Dutch Mill math in a container for the OMNI format; Igor will run the server locally. Nothing blocks him: he made generated art with programmatic animation instead of background video, and offered to show it. Sergey Klimenovich's video work is stuck because his account on the video AI tools is blocked; Andrei looked into accounts yesterday. Pavel suggested writing a request for the needed video in parallel. Igor and Pavel think a meeting with Val is needed on next steps. **Pavel: the AI PM should clarify with Andrei Bosik the access to video-generation AI tools for Sergey Klimenovich.**

**Ivan.** In one test, if a FlexPort's machine IP changed by DHCP and a transaction ran right after, the port was not yet registered and the first transaction failed with 0x89. He created a task for himself, to fix with Claude and have Pavel review. Pavel: likely not a real case — moving a FlexPort to another machine means cutting power, and it then registers automatically. Ivan will ask what the fix involves; if it is not needed, they skip it. He left comments on PR 226 (Alexey), has another PR open, is on 66, then TIN 80. Pavel asked if yesterday's release was FlexPort only or Flex IQ too; Ivan did not do it and does not know.

**Sergey.** Finishing his first rework task today, then the RIS update/retrieval task (maybe nothing to do there). Then reports (3 tasks, e.g. 35 and 21), as video alarms: one report fires when an event happens; one gives statistics over N days. Pavel agreed. **Payment hub:** Sergey's Stripe card-payment experiment must also be built, but no timeline was set yesterday; Nathan has something to finish. It runs through the billing service; the UI needs design (pay one invoice, list of unpaid invoices, partial payment). **Pavel: focus on RIS first.** Later, have Claude draw screens for several unpaid invoices from existing screens and show them to Val and Andrei. Only Stripe was checked so far; fees differ by vendor, but Stripe is one of the largest in the US.

**Vladimir.** GALAXY autotests: closed 71 and 72; finishing 71 and 31 (waiting for a hardware run); PR on 33. He opened a backlog story: after changing connection priority, the modem does not come up until reboot. **Pavel: this should not happen and needs a fix.** Next 57 and 63, maybe on the weekend.

**AI PM and Jira (Dmitri).** Tasks the AI agent assigns must be handled within 24 hours — moved from AI Draft to another status (Reject or To Do) — or they disappear. **Pavel: show AI Draft in the dashboard To Do column; Dmitri will do it.** Yesterday the agent made 3 tasks (2 for Alexey, 1 for Anton, already in work). It also commented on NAD 2 and linked LGS 1226 and LGS 1228; someone must check that these are the right tasks. Jira report: some parents are closed while children sit in Backlog. Pavel: looks like an error. Vladimir proposed allowing tasks with no parent (unsure items, parked for discussion). Pavel: then a regular grooming step is needed to review new tasks with no parent.

## Decisions Made

- **MVP2 = Wi-Fi on Flex-Ports / Flex IQ + remote port update through Flex IQ; former MVP2 (Flex Pay) is now MVP3.** — reported by Pavel from yesterday's coordination meeting; Val does not want to mix it all. (Decided by Val, reported by Pavel Frolov)
- **Roll back the Flex IQ commit that changes the modem MAC at boot.** — it breaks the modem; a shared MAC is the lesser evil. (Decided by Pavel Frolov)
- **Payment hub / Stripe UI waits until RIS work is mostly done.** (Decided by Pavel Frolov)
- **AI Draft status goes into the dashboard To Do column.** (Pavel Frolov; Dmitri Kovalchuk agreed)
- **Modem not coming up after a connection-priority change is a bug to fix.** (Pavel Frolov)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Roll back the Flex IQ modem MAC commit | TBD | High | Breaks modem connection |
| 2 | Alexander Biratko | Create a task to add Terminal Hub parameters for Flex Pay updates; request repo access (Terminal Hub, FP 1335 board firmware) | TBD | Normal | |
| 3 | Alexander Biratko | Confirm with Genadi where the bezel lights connect | TBD | Normal | Capability 138 |
| 4 | Anton Leshkevich | Finish testing the Clover Fortune port; port the remaining 1–2 games | Oct 16, 2026 (port) | Normal | |
| 5 | Anton Seregin | Close 102, 103, 129; finish printer scenarios | Oct 16, 2026 | Normal | |
| 6 | Pavel Frolov / Daniil Stauskiy | Give Daniil 2 screens, fix the backlight, prepare the test stand | TBD | Normal | |
| 7 | [AI PM] | Clarify with Andrei Bosik the video-AI access for Sergey Klimenovich | TBD | Normal | |
| 8 | Igor Metelski | Show Pavel the generated art and animation; set a meeting with Val on next steps | TBD | Low | |
| 9 | Irina Shishko | Finish open tests, then review MVP2 capabilities | TBD | Normal | |
| 10 | Team | Check MVP2 capabilities and requirements; create missing ones | TBD | Normal | Next 3 weeks |
| 11 | Ivan Shpak | Find out what the 0x89 DHCP fix involves; fix only if needed | TBD | Low | Likely not a real case |
| 12 | Sergey Tsimanov | Finish rework task, RIS update task, then 3 report tasks | TBD | Normal | |
| 13 | Sergey Tsimanov | Later: draw payment-hub screens with Claude and show to Val and Andrei | After RIS | Low | |
| 14 | Vladimir Samusenko | Finish 71, 31, 33; then 57, 63; show Pavel the modem story | TBD | Normal | |
| 15 | Dmitri Kovalchuk | Add AI Draft to the dashboard To Do column | TBD | Normal | |
| 16 | [Unassigned — needs clarification] | Check that LGS 1226 and LGS 1228 are the right tasks for the NAD 2 comments | TBD | Low | |

## Open Questions

- Where exactly do the validator and printer bezel lights connect? (Alexander Biratko → Genadi)
- Should Jira allow tasks with no parent, and who runs the grooming of them? (Vladimir Samusenko, Pavel Frolov)
- Was yesterday's release FlexPort only, or Flex IQ too? (Pavel Frolov)
- Timeline for the Stripe payment-hub work and what Nathan must finish. (Pavel Frolov)
- Does the 0x89 first-transaction failure after a DHCP change need a fix? (Ivan Shpak)

## Dispatch Log

---
*Processed from Teams transcript on 2026-10-16*
*Source meeting: Daily Standup meeting*
