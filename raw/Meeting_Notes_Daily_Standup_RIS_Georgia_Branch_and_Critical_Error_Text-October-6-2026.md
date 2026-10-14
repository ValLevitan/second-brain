# Meeting Summary — Daily Standup meeting
**Date:** October 6, 2026, 4:54 AM – 5:41 AM Eastern
**Duration:** ~44 minutes
**Attendees:** Pavel Frolov, Dmitri Kovalchuk, Sergey Tsimanov, Anton Seregin, Irina Shishko, Andrei Bosik, Dzmitry Chudzinau, Alexander Biratko, Alexey Khamin, Daniil Stauskiy, Evgeny Kharetski, Igor Metelski, Vladimir Samusenko, Ivan Shpak
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026]]

## Summary

Tuesday standup run by Pavel. Held in Russian.

**RIS / passport work for Georgia (urgent).** Pavel told Evgeny to do the urgent RIS and passport changes before his own planned work: CAP-252, 255, 246, 254 (258 is the build). Mostly LGS changes. Time: under two weeks, to the end of next week. Target is Georgia only, on the SVN branch, as a continuation of the v1.14 line (Peach 3). Irina: take the version delivered as 1.14, add only these changes, nothing else. Irina will find which 1.14 data-center version it ran with. Pavel may move the branch to git without the extra commits if that is easier. Pavel already wrote the features and will move them to To Do; they still need estimates. The carousel for Liza is dropped for this branch; statistics come only when the operator scans them. Unplanned items such as reusing the RIS saved in non-volatile memory after a factory reset will likely join this list.

**Critical error screen.** The yellow critical-error screen must show the cause in plain text a technician understands (e.g. "cannot read Dallas"), not a Java exception. Ivan must first confirm the critical error still repeats; it may only have happened on an old Peach 1. Evgeny asked how anyone can confirm all error places are covered; Pavel: settle the method when the task starts.

**Mutagus removal.** Dzmitry took PORT-82 (two SAS connections) and will remove Mutagus (the activation protocol) from the code completely: screens, tests, old Payment Hub parts. He said Val ruled it is gone. Pavel asked what happens if it is needed again; Sergey and Dzmitry: git history allows restore. Irina: Mutagus still appears in requirements and Claude must be stopped from using it.

**Prose, contracts, ADRs in repos.** Alexey raised prose coverage from 46% to 87% (Val asked for at least 85%). A rule now makes Claude check prose in pull requests. He will share how Val's percentage is calculated (Biratko asked; Pavel doubted a commit-based measure can reach 100% for repos where prose came later). Alexander handed parts of the repo list to Daniil and Igor; about 5 repos still lack full prose and contracts. Anton added prose and ADRs to the SDK UI kit (was at zero) and to the Flex IQ Pay dispensers repo. Contracts are written by hand. For a front-end app, Pavel agreed the contract can say it offers no outside interface except the user flow, and point to the back-end contracts it uses. Daniil writes contracts and prose for unfinished repos. Igor will merge Dragon Pays prose to main today.

**Requirements for work already built.** Irina asked what to do with built items that have no requirements. Agreed: a session to go through finished capabilities; Vladimir lists what is missing; Pavel and Irina accept the requirements; tests are not put aside. Vladimir: text gaps are easy; missing designs and translations are the problem (test 69). Agreed: Vladimir adds missing texts himself and opens a ticket for Andrei to check and approve them.

**Jira.** Kovalchuk: watch your due dates. When all features are Complete but the capability is still blue, Jira shows a warning triangle. Pavel: keep the triangle; it makes the team open the capability and decide on tests or closing. The status flow (Proposed, Accepted, To Do) stays as is. Closed items with no due date: Pavel said no need to fill; Kovalchuk said fill them if the report keeps flagging them. Pavel asked Bosik about a branch flagged daily in a report; "all" vs "active" branches explained by commit age.

**Other.**
- Alexander: CAP-143 (Wi-Fi module on Flex): FP-1324, 1325, 1330 (SSH) in progress, some in review. BOM validator (CAP-5) errors still being fixed.
- Anton: FQ-67 accuracy done; needs a terminal for a few hours to check. Will clean up his Jira.
- Daniil: closed 1386; one converter PR still open.
- Dzmitry: closed the unclaimed-money bugs and Alexey's older bugs on the stand. Prefers a check on a real machine too.
- Evgeny: closed DC work and SAS log tests; GitHub cleanup per Val's email.
- Igor: NOVA 2 games with Anton Efimovsky's math. NOVA center will later need new progressive products (Nebraska and others); not urgent. Working on Dragon Pays tests and a vertical scene. Needs a Dragon Pays feature from Pavel for a separate branch.
- Vladimir: asked Anton to check FQ-112 (Anton Vishkevich's daemon change into the emulator) and Pavel to check PORT-91, which blocks his task 34; Pavel is working on it. Pavel moved FIT-127 to backlog.
- Ivan: South Dakota production min bets ran fine overnight; Igor's crash did not repeat. If South Dakota holds for an hour, Evgeny releases the DC. Battery tests: Pavel set three cases with the machine off (swap a 3 V cell for a charged one; same at ~2.86 V; same at a low "problem" voltage). Ivan needs an adjustable-voltage device; Pavel will look for a USB one.
- Sergey: feature 55 (alerts on Flex IQ screens). After Dzmitry's update a terminal ran out of memory and booted badly. Cause found: logs can grow to almost 2 GB while the update partition is about 3.9 GB. Sergey writes a feature. Irina asked him to link FIX-135 to the right feature.

## Decisions Made

- **Urgent RIS/passport changes (CAP-252, 255, 246, 254) go to Georgia only, on the v1.14 (Peach 3) line, with nothing extra; Evgeny does them first.** — Requested for this branch; under two weeks. (Decided by Pavel Frolov, Irina Shishko)
- **The Liza carousel is dropped for this branch; statistics only when scanned.** (Decided by Pavel Frolov, Irina Shishko)
- **Critical-error screen shows the cause in plain text for technicians.** (Decided by Pavel Frolov, Irina Shishko)
- **Mutagus is removed from the code fully; git history is the fallback.** — Val's earlier ruling. (Dzmitry Chudzinau, team)
- **Missing texts: developer adds them and opens a ticket for Andrei to approve.** (Decided by Pavel Frolov)
- **Built capabilities without requirements get a review session; requirements accepted by Pavel and Irina, tests not deferred.** (Decided by Irina Shishko, Pavel Frolov)
- **Front-end contract may state "no outside interface except user flow" and reference back-end contracts.** (Decided by Pavel Frolov)
- **Keep Jira's warning triangle and the current status flow.** (Decided by Pavel Frolov, Dmitri Kovalchuk)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Evgeny Kharetski | Do CAP-252, 255, 246, 254 for Georgia on the 1.14 branch before other work | ~Oct 16 (end of next week) | High | RIS/passport |
| 2 | Pavel Frolov | Move the RIS features to To Do and estimate them | TBD | High | |
| 3 | Irina Shishko | Find which 1.14 data-center version the Georgia build used | TBD | High | |
| 4 | Ivan Shpak | Confirm whether the critical error still repeats | TBD | Normal | Before the error-text work |
| 5 | Dzmitry Chudzinau | PORT-82; remove Mutagus from code | TBD | Normal | |
| 6 | Alexey Khamin | Share how Val's prose coverage % is calculated; recheck and close task 61 | TBD | Normal | |
| 7 | Vladimir Samusenko | Add missing texts for test 69; open a ticket for Andrei to approve | TBD | Normal | |
| 8 | Vladimir Samusenko | List built items missing requirements for the review session | TBD | Normal | |
| 9 | Anton Seregin | Look at FQ-112 (daemon change into emulator); tidy his Jira | TBD | Normal | |
| 10 | Pavel Frolov | Finish PORT-91 (blocks Vladimir's task 34) | TBD | Normal | |
| 11 | Pavel Frolov | Create a Dragon Pays feature for Igor's branch | TBD | Low | |
| 12 | Igor Metelski | Merge Dragon Pays prose to main | Oct 6 | Normal | |
| 13 | Pavel Frolov | Find an adjustable-voltage (USB) device for Ivan's battery tests | TBD | Normal | |
| 14 | Ivan Shpak | Run the three battery-swap cases | TBD | Normal | |
| 15 | Sergey Tsimanov | Write the feature for the log size / update partition memory issue; link FIX-135 | TBD | Normal | |

## Open Questions

- How exactly Val's prose coverage % is computed (Alexander Biratko, Pavel Frolov).
- How to verify that every critical-error source is covered (Evgeny Kharetski).
- Who executes the memory-issue feature, Sergey or Dzmitry (Sergey Tsimanov).
- When to plan NOVA center products for new progressives (Igor Metelski).

## Dispatch Log

---
*Processed from Teams transcript on 2026-10-06*
*Source meeting: Daily Standup meeting*
