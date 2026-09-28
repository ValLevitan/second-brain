# Meeting Summary — Transactional MVP1: CAPs, REQs, UI/UX
**Date:** September 24, 2026, 8:01 AM – 9:11 AM Eastern
**Duration:** About 1 hour 10 minutes
**Attendees:** Andrei Klimovich, Val Levitan, Pavel Frolov, Irina Shishko, Dzmitry Chudzinau, Andrei Bosik, Alexey Khamin, Ivan Shpak, Alexander Biratko
**Raw transcript:** [[Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026]]

## Summary

The meeting was held in Russian.

**Mockups and change logs.** Andrei Klimovich said the mockup is now final. He fixed conflicts between the mockup and the requirements, reviewed non-functional against business requirements, and finalized the tilt logic with an error code for each tilt. Tilts stay inside the main text library, not a separate document. He added icons on the home screen. He posted an auto-generated Jira change log in a chat, but Val and Pavel had missed it. **Val ruled: written records go by email, chats are for instant matters.** Andrei will email a Jira change log at the end of any day he changes Jira.

**Bug 349 — money lost when FlexPort dies.** A player collects; money leaves the machine and sits on the FlexPort while it waits for a ticket scan. If the FlexPort reboots or loses power, the money is lost today, and no logic describes this. Dzmitry wants such money treated as unconfirmed and sent to unclaimed, because nobody knows how long it was down (it could have gone to the warehouse). Irina asked why a player standing there cannot still scan. Pavel suggested resuming the timeout after a restart; Dzmitry showed the risk — a "clever cashier" could switch off the port and later collect the money himself. Ivan noted machines and FlexPorts boot at different speeds. **Agreed simple rule for MVP1:** the transaction is saved in the FlexPort's local memory; when the FlexPort comes back, it sends the money through the gateway into unclaimed. No dialog to the player, even after a one-second blink. Watch real behaviour later.

**Bug 354 — FlexPort loses the gateway link.** Andrei proposed that a FlexPort without a gateway link is not functional and does not allow collect. He also offered the alternative (store locally, retry later). Pavel preferred money stays on the machine, because the player cannot use it on the port and would have to argue with a cashier. **Agreed: no gateway link → FlexPort goes out of service with a message; money stays on the machine.** No objections.

**Unclaimed money after the 30-second timeout.** Val challenged why a fully working FlexPort sends money to unclaimed after 30 seconds. His scenario: a player turns to talk to a friend, 30 seconds pass, and the money is gone. He suggested requiring a PIN, like AFT cards, so money stays tied to the player. Pavel explained the machine can hold money for only 8 seconds (SAS spec), and the port must be freed. Andrei said money leaving a machine is not tied to any wallet today; a session tied to a player is a real player account and a big architecture change. Pavel suggested matching unclaimed money to the nearest earlier wallet deposit on the same machine; Andrei said logs already hold this. Dzmitry gave a counter-example where the nearest wallet belongs to the wrong person. Alexander Biratko warned a cashier could misuse a redirect button. Alexey suggested the cashier could replay the withdrawal to the port. **Val and Andrei ruled: cashier handling of unclaimed money is deferred to MVP2.** For MVP1 the task is only to keep the money, not lose it.

**Receipts and service screens.** Dzmitry asked what happens on cashier screens when the idle timer expires before an action. Andrei said after 15+15 seconds the system treats it as "no receipt" and the transaction goes to records, where reprint is available. Dzmitry noted pending receipts must also be reprintable; Andrei will mark it. Pavel said out-of-service screens can show specific causes (door open, machine locked, QR scanner not working). Andrei asked for the full list of tilts and errors with a recommended action for each. Pavel is adding the **software version and serial number footer** on service screens; Andrei will add it to the mockup (service, init and idle screens only — not player screens). The status bar with icons will show on all screens except where the player is acting.

**Autotests.** Irina is creating autotest features per capability; she expects to finish all of them today or tomorrow. There are 24 capabilities with 4–5 features each. Alexey found a way for tests to run with no person: it needs a test API on the terminal (Dzmitry's task FIG-56, due today). Pavel noted Dzmitry set end dates but no start dates in Jira; Dzmitry fixed it during the call. Alexey expects his test tooling ready today and to start filling tests tomorrow. He writes tests with Claude, but the tests run on their own. **Val called end-to-end testing "extremely important" at this stage** and wants the whole team, including Andrei Klimovich, focused on it. Pavel and Andrei Bosik warned test hooks are only for the debug environment; in production they are security holes. Val floated enabling hooks remotely with a key for field diagnostics — "not MVP1, maybe not even MVP3"; Pavel said it needs thinking.

**Repository.** The autotests live in the integration repository, since they span FlexPort and Flex IQ. Nobody could say if a matching Jira project exists (Val: repository = project code). Val told Alexey to point Claude at the repository standard and consult Andrei Bosik. Pavel noted ADRs should now live in docs. **Andrei Bosik took ownership of setting this up so Val does not need to chase it.**

**Commits.** Ivan's test work (FlexPort-to-machine connections, 20-second budget) is only on his local computer. Val said he is "categorically against this": commit to GitHub several times a day, average about 300 lines per commit, never more than 300 lines sitting locally. "Everyone got amnesty for the past."

**Release date.** Irina said an October 1 release would be "50/50" on autotest coverage. Val offered **October 15**, saying he always knew it would be the 15th, and linked it to Andrei Klimovich being away on vacation. Andrei objected: 15 can become 30 the way 1 became 15; he wants the build received, installed on machines in Georgia and tested on October 1, even if half does not work. **Val agreed: "this is right."** The meeting continues tomorrow.

## Decisions Made

- **Bug 349: a FlexPort that dies holding money keeps the transaction locally and, on recovery, sends the money through the gateway to unclaimed.** No player dialog. (Andrei Klimovich; agreed by Pavel, Dzmitry)
- **Bug 354: a FlexPort with no gateway link goes out of service; collect is not allowed and money stays on the machine.** (Andrei Klimovich, Pavel; no objection)
- **Cashier handling of unclaimed money (redirect to a wallet) is deferred to MVP2.** Considered and deferred: Val's PIN-bound wallet idea and Pavel's nearest-wallet matching. (Val, Andrei Klimovich)
- **Written records such as Jira change logs go by email, not chat.** (Val)
- **Version/serial footer shows on service, init and idle screens only; status bar shows on all screens except the player action zone.** (Andrei Klimovich, Pavel, Irina)
- **Test hooks are allowed only in the debug environment, never in production.** (Andrei Bosik, Dzmitry, Pavel; Val accepted)
- **Code goes to GitHub several times a day; no more than ~300 lines kept locally.** (Val)
- **Considered and superseded: release on October 15** — replaced by keeping **October 1** for the build to be delivered, installed and tested. (Val offered 15; Andrei Klimovich objected; Val agreed)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Add the two logic changes from bugs 349 and 354 to the requirements | Sep 24, 2026 | High | MVP1 scope |
| 2 | Andrei Klimovich | Email a Jira change log to the team at the end of any day he changes Jira | Ongoing | Normal | Replaces chat posts |
| 3 | Andrei Klimovich | Mark that pending (held) receipts must be available for reprint | TBD | Normal | Raised by Dzmitry |
| 4 | Andrei Klimovich | Update the mockup: version/serial footer on service screens; status bar logic | TBD | Normal | |
| 5 | Pavel Frolov | Send Andrei the list of tilts and errors with a recommended action for each | TBD | Normal | For out-of-service screens |
| 6 | Dzmitry Chudzinau | Finish FIG-56 (terminal test API/hook) | Sep 24, 2026 | High | Blocks unattended autotests |
| 7 | Alexey Khamin | Finish the test tooling, then start filling in tests | Sep 25, 2026 | High | Tooling today, tests tomorrow |
| 8 | Irina Shishko | Create autotest features for all capabilities | Sep 25, 2026 | High | 24 capabilities |
| 9 | Andrei Bosik | Set up the integration repository per the standard (Jira project, ADR in docs) | TBD | Normal | Val: "so I do not need to chase" |
| 10 | Alexey Khamin | Point Claude at the repository standard and consult Andrei Bosik | TBD | Normal | |
| 11 | Ivan Shpak | Commit his local test work to GitHub | Sep 24, 2026 | Normal | Val's commit rule applies to all |

## Open Questions

- How will locations handle unclaimed money in MVP1, when the cashier has no action to release it? (Pavel)
- Can test hooks be enabled safely in the field with a special key? (Val; Pavel: needs thinking)
- Does a Jira project exist for the integration repository? (Val; Andrei Bosik and Pavel could not answer)

## Dispatch Log

---
*Processed from Teams transcript on September 24, 2026, 10:20 AM Eastern*
*Source meeting: Transactional MVP1: CAPs, REQs, UI/UX*
