# Meeting Summary — Transactional MVP1 Launch Plan: Brackets, Daily Caps, MVP2 Scope
**Date:** October 14, 2026, 3:49 PM – 5:32 PM Eastern
**Duration:** About 1 hour 43 minutes
**Attendees:** Val Levitan (Speaker 2); Andrei Klimovich (Speaker 1; confirmed by Val 2026-10-15); Speaker 3 (few words, not identified)
**Raw transcript:** [[Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026]]
Source: Plaud recording (offline), via Plaud-Inbox/JVL
**Initiative:** promoted by Val 2026-10-15 to [[Transactional_MVP-2]] (hub: [[Transactional_MVP-2_Hub]]).
Glossary ruling by Val 2026-10-15 applied to the raw file: "income" → InComm (3; Cyrillic "Инком" left as spoken).

Calendar: no matching event. [Personal passage removed — owner ruling 2026-09-28: the JVL brain holds JVL matters only. Original kept in the source vault.] Held in Russian. Follows the ATL COAM demo: [[Meeting_Notes_ATL_COAM_Transactional_Demo_Show_Special_and_Daily_Caps-October-14-2026]].

## Summary

**When is MVP1 "released"?** Andrei wanted the product team to run all main cases on Flex-IQ (9 areas, about 10 tests each, 1–1.5 days). Val said that is a waste of time now: MVP1 counts as released only when the end-to-end tests on the acceptance criteria in the requirements pass. Field/beta tests come after. User experience is subjective and takes hours, not days. Val saw "November 9" this morning as the end-to-end date but was not sure.

**Path to the first 10 locations (target November 1).**
- **Covers:** not here yet. Val: use monitors from stock with "JVL — We Take Our Games Seriously", screen inactive. 3D-printed covers are the other option.
- **Printers:** shipping today; identical to the test printers, in an enclosure.
- **Ports without Wi-Fi:** do not wait and do not replace ports. The first release is sold without Wi-Fi. About 100 Flex-IQ and 100 ports exist; 100 more ports (with Wi-Fi) arrive in about two weeks. Pause after the first ~10 locations.
- **Other makers' machines:** the test machines arrived; tomorrow the team connects ports. Val is 95% sure it works.
- **Brackets:** Val first said retrofit brackets are the master's job (JVL can release drawings; it is not ethical for JVL to supply brackets for other makers' machines). Then: for the first location JVL makes them. IGT and Aristocrat brackets may already be done; Light & Wonder not. Order brackets for 10 locations and find a local distributor. Andrei will get the exact machine models; Val: hand it to Sebastian (not Mikhail) to find the distributor, cc Genadi.
- **Harnesses:** Genadi makes drawings; a China supplier builds and ships by air. To hold November 1, the first 10 sets are made by hand here (Anibal, Sebastian). Order more than 10 sets. About 60 ports needed for 10 locations at 6 each.
- **Network parts:** Mikrotik switch, a spool of Cat6 cable, good crimping tool and connectors (a bad tool causes intermittent faults).
- **Modems:** none in stock; 100 on order; no tracking link yet.
- **Installs:** at most two per day, JVL present at each; 20 locations take at least a week.

**Daily caps and funding (Val's live pitch to the customer, now to be built properly).** JVL sets the daily cap because JVL guarantees the money to InComm. Val has started talks with InComm to extend JVL's payment window to 5 days (now about 3; the contract says 1, as he recalls). Each location (or operator) needs a backup: a guarantor account and a credit card for pre-authorization. Sign-up today asks only for an ACH bank account. A balance-check service (name heard as "Duala") lets JVL check the balance; contract terms should allow checks every hour or two when funds are short, with a small fee per check (about $0.20–0.50). Escalation: SMS and email notices (auto-call later, needs opt-in) → secondary account → master → automatic block of the location (including its Flexports). Auto-block was left out of MVP1; Val called it "MVP 1.5" — a couple of locations can start without it.

**Contracts.** JVL has no templates for operators or locations. Likely: operator contract for equipment and the monthly fee; location contract for access to its bank account. Val takes the contract architecture; Andrei Klimovich reviews. Accounting reports may need to extend to masters and locations.

**Sign-up model.** Master account → linked locations → each location's financial info plus a secondary card. Masters see their locations; locations see only themselves.

**November 1 stays.** Val: run AI over the November 1 MVP in Jira to see what this talk missed.

**Magazine ad.** JVL pays for a monthly page. Redo it around transactional equipment plus the machine, with a tagline like "if you do not have this, you are late." Andrei will write the brief for subcontractors and check the deadline (contact heard as "Ferrik") to make the November issue. Audience is mainly locations. Whether to combine machine and equipment in one ad is open.

**Trade show.** Val goes with someone (heard as "Ubach") on Monday the 22nd (as heard). Plan was to show Flex-IQ; parts are stuck. They may go with the current status.

**MVP2 scope (discussed).** Slim dispensers working with Flex-IQ. Val's priorities: Wi-Fi; connection and diagnostics, including a screen where the location sees what disconnected; a basic inspector report; cash-out split into up to 9 location-defined categories (lottery ticket, gas, groceries…); polished remote update and reconnect for Flexport and Flex-IQ; configurable optional features (e.g. TIN code); low-funds notifications to operators; e-signing of all contracts (DocuSign/Dropbox/PandaDoc) from templates with tracking and reminders. No new card integrations now.

**Cloud backup.** Today all transactions live only in the Flex-IQ; if it fails, the location's history is lost. Val: first step is a backup of each unit to the cloud (about two days kept). Andrei agreed. The full dashboard is primitive now; a proper one is likely MVP3.

**Machines.** Andrei: 10 machines left, Black Friday ahead, monitor question still unresolved. Val said he missed it and takes it. Sales this year are slightly below last year's (about 90+).

**Vysotsky.** Andrei gave him the 7,000-location Georgia list; he runs AI to find contacts and will propose a bot that calls locations presenting as a marketing agency. Val suggested buying c-store show visitor databases. Val was very impressed and would hire him; Andrei noted he needs direction.

**Capacity.** Andrei worries he is the bottleneck for the developers; another product manager may be needed. Val: work within the limit.

## Decisions Made

- **MVP1 is released only when the end-to-end tests on acceptance criteria pass; no separate product-team test pass now.** (Val Levitan)
- **November 1 first-location date stands.** (Val Levitan)
- **First locations use stock monitors with the JVL slogan instead of waiting for covers.** (Val Levitan)
- **First release ships Flexports without Wi-Fi; no port replacement.** (Val Levitan)
- **JVL makes brackets for the first location; order for 10 locations; Sebastian finds the distributor, Genadi in copy.** (Val Levitan)
- **First 10 harness sets are made by hand to hold November 1.** (Val Levitan)
- **Location auto-block moves to "MVP 1.5"; a couple of locations may start without it.** (Val Levitan)
- **First cloud step: per-unit backup to the cloud.** (Val Levitan; Andrei agreed)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val Levitan | Ask Genadi which brackets exist (IGT, Aristocrat, Light & Wonder) | TBD | High | |
| 2 | Andrei Klimovich | Get the exact machine models; pass to Sebastian to find a bracket distributor, cc Genadi | TBD | High | |
| 3 | Val Levitan | Talk with Genadi and Elizabeth so harness drawings are done and 10 sets are hand-made | Before Nov 1, 2026 | High | |
| 4 | Genadi Peari | Harness drawings; order harnesses from China by air | TBD | High | |
| 5 | Val Levitan | Find the tracking link for the 100 modems | TBD | Normal | |
| 6 | Andrei Klimovich | Buy Mikrotik switch, Cat6 spool, crimping tool and connectors | TBD | Normal | |
| 7 | Team | Connect ports to the other makers' test machines | Oct 15, 2026 | High | |
| 8 | Val Levitan | Contract architecture and templates (operator, location); Andrei reviews | TBD | High | |
| 9 | Andrei Klimovich | Magazine ad brief; check the November deadline | TBD | Normal | |
| 10 | Val Levitan | Resolve the monitor question for the last 10 machines | TBD | Normal | Black Friday ahead |
| 11 | Andrei Klimovich | Send action-point emails (Val, Genadi, Mikhail) | Oct 15, 2026 | Normal | |
| 12 | [Unassigned — needs clarification] | Run AI over the November 1 MVP in Jira to find gaps | TBD | Normal | |

## Open Questions

- Can JVL see a backup credit card's limit? (Andrei) — Val thinks not.
- Exact end-to-end test completion date — November 9? (Val)
- One ad or two (machine and transactional equipment)? (Val)
- How many harnesses per machine model, given different connectors? Ask Raoul (heard "Рау"). (Val)
- Operator and location contract structure. (Andrei)

## Dispatch Log

---
*Processed from Plaud transcript on 2026-10-15*
*Source meeting: 10-14 Product Release Roadmap and Deployment Strategy Alignment*
