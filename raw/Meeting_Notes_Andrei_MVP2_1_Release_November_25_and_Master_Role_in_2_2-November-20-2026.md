# Meeting Summary — MVP2_1 and MVP2_2 review, pt2
**Date:** November 20, 2026, ~9:02 AM – ~10:01 AM Eastern (recording)
**Duration:** ~59 minutes
**Attendees:** Andrei Klimovich (organizer), Val Levitan, Pavel Frolov, Irina Shishko, Dzmitry Chudzinau, Sergey Tsimanov
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Andrei_MVP2_1_Release_November_25_and_Master_Role_in_2_2-November-20-2026]]

## Summary

**Release 2.1.** Pavel: the main open item is many unpublished requirements; he moved his to request review, some to Irina for the last word. Irina still has 5 items. The 2.1 scope is frozen: Wi-Fi, remote port update, "Goods" instead of lottery, phone numbers, SIM cards, closer barcode reading. Development is done; autotests remain, and they may find bugs. Val asked if they could define what goes in and release within a week; he does not want releases less often than once a week. The Jira release date must include written and passed autotests. Irina would add a couple of days. **Release 2.1 date moved from Nov 23 to Wednesday Nov 25.**

**Task 399 moved to 2.1.** Alexeev's firmware that flashes the Wi-Fi module was on 2.2. Pavel: without it Wi-Fi will not work in Georgia (Genadi ruled out flashing by cable a week ago). Moved to 2.1; Pavel expects Alexeev to finish over the weekend.

**No central rollback to an older build.** Andrei asked for the option to push the previous build if a release breaks business logic. Dzmitry: the device already falls back if an update fails its checks, but pushing an older version can break the database (schema changes between versions); fix forward with a same-day patch instead, like phones do. Andrei agreed.

**Master (operator) role in 2.2.** Andrei explained the Georgia market: manufacturer (JVL), location owner (small shop with a licence), and master/operator who owns the machines and places them at locations. One location has one master. Locations link to a master by the master licence number. 2.2 adds master registration (like location-owner registration: email, phone, business data, master licence number), a master list in the admin, login, and a view of locations with his licence number, with reports limited to his period. Changing a location's master would be a manual edit of the licence number; old statistics must not show to the new master (Pavel). InComm must be told by hand when a location's master changes.

**Val's view on master changes.** Val: nobody will unlink and relink; only what the law requires matters — the IQ is registered to the location and master; what is connected is connected. We should not chase operators asking what happened. The question is what the law requires when a location changes master. Andrei: a terminal registered with InComm at one location must not work at another. Dzmitry and Pavel: today a moved terminal would keep working; there is no reliable way to detect a move (IP location is rough; GPS and motion sensors could help later as an alert). Dzmitry suggested later: link terminals to the master first and let the master assign them to locations. Not for 2.2; Andrei may put it in 3.

**2.2 scope and date.** Main topics: master and reporting (with growing locations, data lost later is lost). Val suggested moving very large capabilities out (2.2 → 2.3). Dzmitry: most are independent cloud services; review first, then see what blocks what. SAS statistics in bill-validator mode moved to MVP 3 during the meeting. People free from 2.1 start reviewing 2.2 now; others after the 2.1 release. 2.2 date cannot be named until scope freeze (~2 weeks after 2.1).

**MVP 3: cloud wallet and offline.** Andrei asked whether MVP 3 moves tickets/wallets to the cloud. Dzmitry: the sooner the better; he is against creating tickets offline and syncing later (like an ATM without a bank link). Andrei and Pavel: Georgia mobile coverage is poor; a 20-second drop would block all money in, out and machine-to-machine moves. Pavel: real money moves (to card) need internet; moving credit inside a location maybe not. Dzmitry: offline then needs shared number rules to avoid collisions. Val backed Dzmitry: design for always-on internet; solve weak coverage with better connectivity, not exceptions in the architecture. Parked for a full discussion.

## Decisions Made

- **Release 2.1 date: Wednesday November 25, 2026 (was Nov 23).** — Autotests may find bugs. (Andrei, Irina, Pavel)
- **Task 399 (Wi-Fi module firmware) moves from 2.2 to 2.1.** — Wi-Fi will not work in Georgia without it. (Pavel, Dzmitry)
- **No central rollback to an older build; fix forward with a quick patch.** — Older versions can break the database. (Dzmitry; Andrei agreed)
- **SAS statistics in bill-validator mode move to MVP 3.** (Andrei, Val)
- **2.2 is about the master role and reporting; master changes are manual edits for now.** (Andrei, Pavel)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | "Alexeev" (likely Evgeniy Alekseev — [Needs Val's confirmation]) | Finish task 399: firmware that flashes the Wi-Fi module | ~Nov 22 | High | Pavel's expectation; Alexeev not in the call |
| 2 | Irina Shishko | Finish her remaining 2.1 requirements (5) | Before Nov 25 | High | |
| 3 | QA team | Finish 2.1 autotests | Before Nov 25 | High | Over the weekend |
| 4 | Team members free from 2.1 | Start reviewing 2.2 capabilities; comment gaps | TBD | Normal | Andrei answers |
| 5 | Dzmitry Chudzinau | Review 2.2 capabilities and check which block others | TBD | Normal | |
| 6 | Andrei Klimovich | Add to MVP 3: master manages own terminals; terminal move detection | TBD | Low | |
| 7 | [Unassigned — needs clarification] | Find out what Georgia law requires when a location changes master | TBD | Normal | Val's question |

## Open Questions

- What does the law require when a location moves to another master? (Val)
- MVP 3: should any money moves work offline? Parked. (Andrei, Dzmitry, Pavel, Val)
- Can one building hold two locations? Andrei thinks not, not sure. (Dzmitry)

## Dispatch Log

---
*Processed from Teams transcript on November 20, 2026, ~10:40 PM Eastern*
*Source meeting: MVP2_1 and MVP2_2 review, pt2*
