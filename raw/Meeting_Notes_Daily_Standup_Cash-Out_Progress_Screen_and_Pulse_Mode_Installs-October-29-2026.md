# Meeting Summary — Daily Standup meeting
**Date:** October 29, 2026, 4:46 AM – 5:22 AM Eastern
**Duration:** ~36 minutes
**Attendees:** Pavel Frolov, Alexander Biratko, Alexey Khamin, Anton Leshkevich, Anton Seregin, Daniil Stauskiy, Dmitri Kovalchuk, Dzmitry Chudzinau, Evgeny Kharetski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026]]

## Summary

Held in Russian. Audio is poor in places. Unclear names, numbers and words are marked "heard". Igor was absent.

**Field test and first installs.** The test machines were taken back yesterday, so port tests on them may no longer apply. Andrei Klimovich goes with Sebastian on Friday to United Gaming (heard), one of the largest Georgia operators, to try the port on their machines. Pavel's field summary for Dzmitry: SAS worked only with Aristocrat. On the IGT machine (heard) AFT only credits in; cash-out is not implemented. Operators say Light & Wonder AFT has never worked anywhere. So the first installs will run in bill validator + pulse mode. No installs are scheduled yet; Felipe has to name the operator and the machine and equipment list.

**Cash-out progress on the port screen.** New requirement 1960 (heard), from yesterday's talk with Andrei: show the amount on the port screen as pulses are counted, so the player sees money moving in real time. Alexander asked what happens if the machine is switched off mid-transfer. Pavel: the money goes to the port, not to a ticket, so the counted part stays on the port. Each pulse is $1, so the screen will show whole dollars, not steps of $5. The latest port builds already add up cash-outs that continue after a timeout.

**Requirement 1926 (heard) gaps.** Alexander: Andrei's requirement is not fully done. Missing: a "your money is saved, contact..." screen, a collect screen, and a partial-deposit message. He will create stories for them. Port work comes first. Pavel: the port release is expected by tomorrow. The release build must be checked, at least that update from a flash drive works.

**Who owns agent-created requirements in Jira.** Dmitri: they default to Irina; they could stay unassigned. Pavel first suggested Andrei Klimovich. Irina: requirements belong to no one. Pavel: during review, assign them to the person who reads and decides; after acceptance the assignee does not matter. No final rule set.

**New engine and browser games.** Daniil has no tasks after NFL1 (heard). Irina: reworking old games is wasted time now that a new engine is coming. Alexander: Val stopped code writing for now (heard). Pavel: the team is not ready to build the new engine, and browser games are paused; a decision on direction is needed. Pavel will talk to Igor about Daniil converting horizontal game resources to vertical. Daniil: in the two-game test, video decoders load at game select, so video-heavy games load slowly.

**Nova update system.** Val emailed about how components and games will update on the Nova platform. Pavel sent a general draft; Dzmitry will work out the server side. One game is roughly 700 MB with resources, maybe 350–400 MB compressed.

**Wi-Fi for Flex devices.** Anton Seregin worked out the Wi-Fi network for Flex-Port, Flex IQ and Flex Pay. New capabilities and requirements are coming for the server, Flex IQ and Flex-Port (access point settings, passwords, security). Pavel wants to review Anton's list today and start entering it.

**RIS with linked progressives.** Ivan: old RIS data is kept but cannot be applied, because the master controller does not know which to take. Irina: linked progressives cannot be a reason to reject old RIS. Evgeny needs a requirement and criteria. Pavel: separate short meeting at 12:40 (Minsk time).

**Jira standards.** Dmitri showed the Knowledge repository standards. Each GitHub repository has its own Jira project; tasks go in the project of the repository where the commit will land. Old projects such as BEP and Core Technology are not in the table and will be archived. There is also a Jira hierarchy standard (feature → capability → epic), in Russian and English. Anton Seregin asked to mark BEP so Claude stops suggesting it.

**Other updates.**
- Pavel: Andrei's AI created ports 177 and 178 (heard).
- Alexey: could not install from SD card to the terminal yesterday; doing it first today; will also try flash; autotests on hardware continue.
- Anton Leshkevich: updating resources for Nebraska (heard).
- Anton Seregin: capabilities and features generated. Left: a spike on how dense or large a QR code the scanner reads reliably, tested on an installed port. Pavel: use a few Flex-Port or Flex IQ features with many acceptance criteria already covered by autotests as the reference; tests are generated from criteria where possible.
- Daniil: opened a PR for NFL1 (heard); Rambo and Cali (heard) are merged; Anton should review the PR in Lover Fortune (heard).
- Evgeny: cleaned Jira; RIS progressive mostly done; next the JSON agent and bug fixes.
- Irina: autotests and features, MVP-2 first.
- Ivan: built to check Pavel's installer changes; continues RIS work.
- Sergey: made a separate feature for firmware transfer; PR created; closing his task.
- Vladimir: reviewing backlog tasks 127 and 142 (heard); a data text-id for autotests is low priority.
- Dmitri: Jira dates mostly fine; some tasks lack due dates.
- Dzmitry: back today. The main server is failing again (heard "swaha") after one of our machines was connected; math needs fixing.

## Decisions Made

- **First installs run in bill validator + pulse mode** — SAS/AFT cash-out works only on Aristocrat. (Pavel)
- **Port cash-out screen shows the running amount in whole dollars** — each pulse is $1. (Pavel; Alexander agreed)
- **Alexander creates stories for the missing screens and message in requirement 1926 (heard)** — the team does not object to them. (Alexander, Pavel, Irina agreed)
- **Separate meeting at 12:40 Minsk on applying old RIS with linked progressives.** (Pavel)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexander Biratko | Create stories for the missing screens and partial-deposit message in requirement 1926 (heard) | TBD | Normal | Port work first |
| 2 | Alexander Biratko | Check the port release build, at least update from flash | Oct 30, 2026 | High | Release expected by tomorrow |
| 3 | Alexey Khamin | Install from SD card to the terminal; also try flash | Oct 29, 2026 | Normal | Failed yesterday |
| 4 | Pavel Frolov | Talk to Igor about Daniil converting horizontal game resources to vertical | TBD | Normal | Daniil has no tasks |
| 5 | Pavel Frolov | Review Anton Seregin's Wi-Fi list and start entering capabilities | Oct 29, 2026 | Normal | |
| 6 | Dzmitry Chudzinau | Work out the server side of the Nova update system | TBD | Normal | Pavel's draft sent |
| 7 | Pavel Frolov, Ivan Shpak, Evgeny Kharetski, Irina Shishko | Meet at 12:40 Minsk on old RIS with linked progressives | Oct 29, 2026 | Normal | |
| 8 | Anton Leshkevich | Send Vladimir the new engine requirements page | Oct 29, 2026 | Low | Vladimir to read it |
| 9 | Dmitri Kovalchuk | Send the link to the Jira standards; update standards to mark BEP and old projects | TBD | Normal | So Claude stops suggesting BEP |
| 10 | Anton Leshkevich | Review Daniil's PR in Lover Fortune (heard) | TBD | Normal | |
| 11 | Anton Seregin | Run the QR scanner spike on an installed port | TBD | Normal | |

## Open Questions

- Who owns agent-created requirements in Jira — Irina by default, unassigned, Andrei Klimovich, or the reviewer? Raised by Dmitri; not settled.
- Where the game team goes next while the new engine is not ready and browser games are paused. Raised by Pavel.
- When installs start: Felipe has not finalized operator and equipment list. Raised by Dzmitry.

## Dispatch Log

---
*Processed from Teams transcript on October 29, 2026*
*Source meeting: Daily Standup meeting*
