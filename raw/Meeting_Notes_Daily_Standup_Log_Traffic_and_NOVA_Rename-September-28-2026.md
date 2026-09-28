# Meeting Summary — Daily Standup meeting
**Date:** September 28, 2026, 4:56 AM – 5:29 AM Eastern
**Duration:** About 33 minutes
**Attendees:** Pavel Frolov (chair, organizer), Alexander Biratko, Alexey Khamin, Andrei Bosik (joined at the end), Anton Seregin, Daniil Stauskiy, Dzmitry Chudzinau, Dmitri Kovalchuk, Evgeny Kharetski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026]]

## Summary

Held in Russian. The speech recognition is poor in places, so some task numbers and names below are uncertain. Round-the-table status, then two short announcements at the end.

**Log and metrics traffic.** Dzmitry ran an overnight test. Logs and metrics use about **120 MB per day** in normal idle mode, with no updates. That is a bit more than **3 GB per month**. Some logs are junk: a printer service and a scanner send the same data again and again. These can be cached or sent every 5 minutes. Dzmitry thinks this can cut traffic about **2 times**. Pavel said 3 times (about 1 GB) would be good. Going further needs lower log levels (info instead of debug), which loses detail, and a look at what the operating system sends. Dzmitry will tell Andrei, so Andrei can judge if this is critical.

**Omni renamed to NOVA.** Andrei Bosik announced that everything named **Omni is now named NOVA**. Pull requests were made in the affected repositories. The maintainers of those repositories must accept and merge them. Andrei posted the list in the chat. Most of the repositories are Alexander's.

**Say the CAP and feature number.** Dmitri Kovalchuk said two daily reports now arrive: **Jira hierarchy** (linked to MVP 1) and **Jira discipline** (statuses and dates). He asked people not to break statuses: if work is really in progress, set it In Progress. He also proposed that at standups people name the exact **CAP and feature** they work on, because these meetings may later be read by AI. Today only Alexander did this, and Dzmitry partly. Pavel agreed.

**FlexPort on a real machine.** Pavel said the latest FlexPort version should be installed on a real machine. The recent fixes were tested only on the emulator. At the start, work done only on the emulator did not all work on the machine. Ivan said he will install it on his machine. Ports exist on 2 or 3 machines; Pavel has 2 more ports, the newest ones, with Wi-Fi.

**Engineering menu task.** Vladimir works on a service menu for the port and did not know which capability to link it to. They agreed not to create a new capability. Pavel will add a **new requirement under capability 235** (screens and texts) for diagnostic / engineering menu screens. A new feature will then come from it.

**Card dispenser.** Alexander is working on capability 134 (features 1284, 1285, 1286): full card dispenser support, like Flex IQ. Two card dispenser types are supported; at start the software checks both and picks the one that answers. Pavel asked that it **tries Syncotek first**, because it will be used in about 99% of cases.

**Individual status.**
- **Alexander Biratko** — capability 137 (updates) mostly done; long install checks still running. Capability 134 planned to finish today. Capability 133 (choose which bills to accept) worked on over the weekend; to close it he must insert bills in the kiosk and check. He expects 133, 134 and 137 to close soon. Next: the GSM modem, moving the control code to FlexPort. Pavel asked him to put start and end dates on his tasks.
- **Alexey Khamin** — autotests. The cash-out (withdrawal) test he wants to close today. He will spread Ivan's autotests across the repository by the new rules. Task 16 (deposit to EGM) is barely started: one scenario written.
- **Anton Seregin** — finished the move on Saturday. Made a plan to move the accumulator to Flex IQ; first task looks done, he is checking. The bridge takes contracts from both Flex IQ and the accumulator. The tool gave its own dates; Irina said surely not until October 21. The build on GitHub Actions has quick endpoint tests. Pavel said these will help later for automatic tests.
- **Daniil Stauskiy** — made a copy of a game in LGS with denominations; it loads and plays, and he is fixing asset loading. He has no assets for the game select screen. Igor has one and should move it this week. The select screen needs 2 games. Pavel suggested **Dragon Rain**, which may be in a runnable state. Alexander said Dragon Rain is a copy with the same math; only images differ. Igor's games are not Class 3. Daniil has no access to that repository; Pavel said they will open it.
- **Dzmitry Chudzinau** — with Andrei, aligned product terminal names for updates; builds install and work. Card activation done. Tests are finishing on his container; will push today. Will also push capability 237 today (dashboard of activated cards). Pavel said the overdue tasks can be closed by payment hub.
- **Evgeny Kharetski** — moved the data center to LGS over the weekend. Anton fixed gaps in the services for him. Next: continue adding services.
- **Irina Shishko** — must re-plan with Vladimir and see when he can join (to help create autotests). Will close unneeded features and tasks in Jira.
- **Ivan Shpak** — priorities: (1) create an installation; (2) review drafts sent on Friday, certificates expected today; (3) autotests; (4) the instruction promised for Monday will not be ready today. Irina said a feature is needed for it. Ivan will keep working on his draft autotest after the meeting, so he has something to show.
- **Sergey Tsimanov** — finished wallet creation on Flex IQ. Took the next task on wallet creation (name not clear in the transcript). A Grafana dashboard task (type TPT-INT, in the integration repository) may already be done; he thinks he updated the dashboards when he added link-quality metrics. Irina said the task belongs in the integration repository only if its result is committed there.
- **Vladimir Samusenko** — service / engineering menu for the port (see above).

## Decisions Made

- **Card dispenser: try Syncotek first.** — It will be used in about 99% of cases. (Decided by Pavel Frolov)
- **Engineering menu goes under capability 235 as a new requirement, not a new capability.** — Simpler. (Decided by Pavel Frolov, agreed by Vladimir Samusenko)
- **At standups, name the exact CAP and feature being worked on.** — The meetings may be read by AI later. (Proposed by Dmitri Kovalchuk, agreed by Pavel Frolov)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexander Biratko | Put start and end dates on his Jira tasks; finish capability 134 | Today (Sep 28, 2026) | Normal | |
| 2 | Alexander Biratko | Test bill acceptance on the kiosk to close capability 133 | TBD | Normal | |
| 3 | Alexander Biratko (and other repo maintainers) | Accept and merge the Omni → NOVA rename pull requests | TBD | Normal | List in chat from Andrei Bosik |
| 4 | Alexey Khamin | Close the cash-out autotest; spread Ivan's autotests across the repository by the new rules | Today (Sep 28, 2026) | Normal | |
| 5 | Ivan Shpak | Install the latest FlexPort version on his real machine | TBD | High | Recent fixes tested only on emulator |
| 6 | Pavel Frolov | Open repository access for Daniil to Dragon Rain | TBD | Normal | |
| 7 | Daniil Stauskiy | Look at Dragon Rain for testing the game select screen | TBD | Normal | |
| 8 | Dzmitry Chudzinau | Push card activation tests and capability 237 (activated cards dashboard); close overdue tasks | Today (Sep 28, 2026) | Normal | |
| 9 | Dzmitry Chudzinau | Remove junk logs to cut traffic; tell Andrei about ~3 GB/month | TBD | Normal | |
| 10 | Pavel Frolov | Create a new requirement under capability 235 for the engineering / diagnostic menu | TBD | Normal | |
| 11 | Irina Shishko, Vladimir Samusenko | Meet after the standup to agree when Vladimir is free; re-plan | Today (Sep 28, 2026) | Normal | |
| 12 | Irina Shishko | Close unneeded features and tasks in Jira | TBD | Low | |
| 13 | Sergey Tsimanov | Check the Grafana dashboard task; if done, comment and close | TBD | Normal | |
| 14 | [Unassigned — needs clarification] | Create a feature for Ivan's instruction | TBD | Normal | Instruction was promised for Monday; not ready today |
| 15 | All | Keep Jira statuses correct; name CAP and feature numbers at standups | Ongoing | Normal | |

## Open Questions

- Is ~3 GB per month of log traffic critical? (Dzmitry, for Andrei)
- When Vladimir will be free to help with autotests (Irina).
- Whether the Grafana dashboard task is already done, and which repository it belongs to (Sergey, Irina).

## Dispatch Log

---
*Processed from Teams transcript on September 28, 2026 (meeting-watcher recovery sweep)*
*Source meeting: Daily Standup meeting*
