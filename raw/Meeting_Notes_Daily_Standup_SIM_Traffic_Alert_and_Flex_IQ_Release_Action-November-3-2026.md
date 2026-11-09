# Meeting Summary — Daily Standup meeting
**Date:** November 3, 2026, 5:15 AM – 5:42 AM Eastern
**Duration:** ~25 minutes
**Attendees:** Pavel Frolov, Alexander Biratko, Alexey Khamin, Anton Leshkevich, Anton Seregin, Daniil Stauskiy, Dzmitry Chudzinau, Evgeny Kharetski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko, Dmitri Kovalchuk
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026]]

## Summary

Held in Russian. Audio is poor in places. Unclear names and words are marked "heard".

**Georgia location lost LTE: SIM data ran out.** Dzmitry: at the Barry House (heard) location the LTE showed "connected" but the terminal was offline. The SIM card had used up its 2 GB of data. He proposed a separate service with alerts: data running out, money running out, SIM-to-terminal binding, traffic per device, and later commands or SMS to the device. No owner was assigned.

**Flex IQ one-button release action.** Dzmitry took the task. Question: should the action also rebuild the SDK, or take a chosen SDK version? Pavel wanted an SDK version parameter (latest, specific, or rebuild). Alexey said rolling back to an older SDK will be rare. Agreed: keep it simple, one button builds both the Flex IQ release and the SDK; the SDK version will match the Flex IQ version; an SDK selector may be added later. Dzmitry needs developer access so the Flex IQ repository can see the SDK repository and run its action.

**Legacy CMS SMS report.** Dzmitry finished the report and a log analysis. Unknown games or unregistered machines will go to a separate table so data transfer is not blocked. Deploy to STG today or tomorrow. Open: recheck the machine and statistics first, or verify on production. Pavel asked that the CMS machine-state view and basic diagnostics keep working for connected machines; Dzmitry: should, if nothing broke, but current machines are far ahead of the ones that logic was built for.

**Jira: old HFM tasks.** Alexander is working the tasks moved from Yavorsky; many pull requests are waiting to be merged; bugs found are mostly rare SAS and printer-command cases. The tasks still sit under the old HFM project. Pavel showed the Jira Move function; the link survives, so Alexander's agent will still find the task. Alexander will move them to the Flex-Port project.

**Handpay reprint bug (Evgeny).** Bug from Irina's request (from the field): if the key is turned right away the handpay ticket prints; after a reboot the event is not sent and the ticket does not print. Looks like a JVL bug; needs checking, plus the settings. Ivan asked if they saw it in release 1; Irina: maybe nobody tested with a reboot. Evgeny also got outside access to the RIS machine via Altai (heard); access had been opened to the wrong place for two days.

**Modem "connect to server" setting.** Pavel: Slava's document describes a full implementation (an access code must be scanned to untick "connect to server"; the server grants permissions). It is controversial. Pavel will discuss today whether to do the full version now or a limited one: the checkbox is on by default when a modem is present, and an operator can turn it off through an extra confirmation screen.

**Echo machine (Ivan).** Pavel: check the Echo machine has both SAS outputs, connect the bill validator (heard "ситолтовский", BV-50 via adapter) and a Gen 2, Gen 5 or Nanoptix printer to confirm protocol 2 still works. Ivan has an Epic 950 working. An external printer is likely (TransAct in external housing was chosen for Flex IQ).

**Other updates.** Alexey: hardware autotests continue; Flex-Port export release version 1; waiting for Dzmitry on the Flex IQ action. Anton Leshkevich: Nebraska updates from Arthur; building a spike skeleton for the NOVA studio editor as a native development environment. Pavel: the spike must hang under a capability about engine and framework architecture for the new platform; Anton will create it. Anton Seregin: CF-8 and CF-9 in progress; built a page of QR codes with different pixel densities to test the scanner. Daniil: moving the sound library to Rust; will review Dependabot dependency requests. Irina: finishing tests, then writing the Wi-Fi features, which are urgent. Sergey: QR task with our implementation; updating the Flex Pay implementation on the cloud side; needs to commit accumulated work. Vladimir: port task 142 done after Andrei's comments; port task 193 done, waiting to merge; Pavel: Flex-Port can be merged now. Next he starts NOVA 2 onboarding, collecting meetings and correspondence. Dmitri Kovalchuk: everyone except Sergey and Evgeny must set an end date on their tasks (not backlog); Pavel has the most without dates.

## Decisions Made

- **Flex IQ release action: one button builds both the Flex IQ release and the SDK; no SDK version parameter for now.** — Rollback to an older SDK is rare. (Pavel, Dzmitry, Alexey)
- **Old HFM tasks move to the Flex-Port project with Jira Move.** — Links survive. (Pavel; Alexander agreed)
- **Vladimir's port task 193 can be merged to main.** (Pavel)
- **Tasks not in backlog must carry an end date.** (Dmitri Kovalchuk)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexander Biratko | Move remaining HFM tasks to the Flex-Port project; merge the waiting pull requests | TBD | Normal | |
| 2 | Anton Leshkevich | Create a capability for engine and framework architecture and link the editor spike to it | TBD | Normal | |
| 3 | Dzmitry Chudzinau | Deploy the legacy CMS SMS report to STG | Nov 4, 2026 | Normal | "today or tomorrow" |
| 4 | Dzmitry Chudzinau | Build the one-button Flex IQ release action (release + SDK); get developer access to the SDK repository | TBD | Normal | Who grants access not named |
| 5 | Dzmitry Chudzinau | Talk with Andrei and Pavel about reverse SSH through AWS | Nov 3, 2026 | Low | |
| 6 | Evgeny Kharetski | Check the handpay-after-reboot bug and the printer settings | TBD | High | |
| 7 | Pavel Frolov | Discuss today: full or limited implementation of the modem "connect to server" setting | Nov 3, 2026 | Normal | Slava's document |
| 8 | Irina Shishko | Write the Wi-Fi features | TBD | High | "starting to burn" |
| 9 | Ivan Shpak | Echo: confirm 2 SAS outputs, connect the bill validator, test a Gen 2 / Gen 5 / Nanoptix printer | TBD | Normal | |
| 10 | Vladimir Samusenko | Merge port task 193 to main; start NOVA 2 onboarding | TBD | Normal | |
| 11 | Team (except Sergey, Evgeny) | Set an end date on every task not in backlog | TBD | Normal | |

## Open Questions

- Who builds the SIM traffic alert service, and when. (Dzmitry's proposal)
- Legacy CMS report: recheck the machine and statistics before deploy, or verify on production. (Dzmitry)
- Modem "connect to server": full or limited implementation. (Pavel, decides today)

## Dispatch Log

---
*Processed from Teams transcript on November 5, 2026*
*Source meeting: Daily Standup meeting*
