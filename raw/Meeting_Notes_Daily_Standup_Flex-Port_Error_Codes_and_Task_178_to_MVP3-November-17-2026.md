# Meeting Summary — Daily Standup meeting
**Date:** November 17, 2026, 3:44 AM – 4:14 AM Eastern
**Duration:** ~29 minutes
**Attendees:** Pavel Frolov (led), Alexander Biratko, Alexey Khamin, Anton Seregin, Daniil Stauskiy, Dmitri Kovalchuk, Dzmitry Chudzinau, Evgeny Kharetski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Flex-Port_Error_Codes_and_Task_178_to_MVP3-November-17-2026]]

## Summary

First morning standup. At the start Dmitri K was testing an AI voice assistant ("Emma") in the call; the team agreed to ignore it for now.

**Release scope for Thursday.** Irina told Pavel: only what is needed for Thursday goes in; mark everything else for release 2_2. Everything is set to 21 by default; if it is not needed, set 22.

**Flex-Port error codes.** Alexander is finishing capability 372 for the Flex-Port (large); he expects to send it for review within about an hour. Irina will rebuild the port after he merges. Capability 372 adds new error codes to the Flex-Port, but Flex IQ will only show them as raw codes. Sergey: Flex IQ needs decoding so it can store them offline and send them to Grafana in readable form. Irina: then such a feature is needed.

**Task 178 (Flex-Port check from another machine).** The task sits on Ivan. Pavel saw similar behaviour yesterday when the machine was in bill-acceptor mode and SAS was also connected. He fixed it, but only for the case when both are connected. Ivan asked for a due date (Irina said the 20th; Ivan proposed Wednesday next week). In the end Pavel and Irina moved it out of this release into capability 298, which is MVP 3. Irina moves it.

**Pavel's Flex-Port work.** Yesterday he made the Flex-Port read bill-acceptor status (for example, door open) faster, instead of waiting 10 seconds for an error. This goes to the next release, not this one. He will review which features need their fix version changed.

**Wi-Fi between Flex IQ and Flex-Ports.** Sergey tested it, mostly in access-point mode, where they see each other. Through a router they did not see each other (GL 1 or GL 2, he does not remember). Pavel: on GL 2 it should work, but the port's Wi-Fi module MAC address must be registered on the router.

**Due dates.** Dmitri K asked people to try moving due dates via the agent chat; Dzmitry tried and it worked. Irina said her own Claude already sets dates. Pavel worried about too many tools. Dmitri K said tasks now close fast, rarely over 14 days. Pavel and Irina: due dates are still needed, to find stuck tasks and to plan.

**Status by person:**
- **Alexander:** also on recycler MVP 1. New vendor documentation: one bit switches between power backup and spray mode. He will test it on the device tomorrow.
- **Alexey:** reminded about features for showing phone numbers on the terminal help screen (from yesterday's call). Hardware autotests. Val asked him to compare current state laws with our regulations; he will send Val something today and ask what next. His Flex IQ build for the test stand failed twice with different errors; asked Dzmitry to look. Reminded Pavel that REQ-1833 waits for his comment. A person wrote rules for Port-157 and a long list of what we do wrong (Pavel had asked for a review); Alexey does not know what to do with it.
- **Anton Seregin:** port tests now pass (TINT-212); emulation part works; checking against a real port today, done about 2:30.
- **Daniil:** PR 1340 reviewed by Alexander; will add a commit to stop the Nexus upload and merge. Continues NewGin-54.
- **Dzmitry:** closing LTE; with Andrei on CI/CD, maybe testable on STG today; checking uninstall; then Flex IQ builds.
- **Evgeny:** ISO creation and install.
- **Irina:** autotests; will write features from the Flex capability requirements. Dmitri K asked if her drafts should go to someone else. Pavel suggested Alexander for the recycler ones, but tests follow requirements, so Pavel agreed Irina keeps them.
- **Ivan:** RIS; checked Evgeny's modem UI, works. Will connect LTE to a machine for Georgia on STG after Dzmitry deploys today.
- **Sergey:** finishing lotteries; released the SMS fix yesterday. Pavel asked him to fix due dates set for today; Sergey said he set them yesterday.
- **Vladimir:** finished contracts; FIG-206 done; answered Andrei Klimovich. On CAP-287 (Flex IQ Wi-Fi delivery), TINT-118: took 2 of 14 scenarios; questions left in Jira comments for Sergey and partly Anton. Asked people to answer. Irina: much is needed by Thursday; also nudge people directly. Asked who owns a feature when several people have stories under it; Irina: the person whose story will close last (here Sergey).

## Decisions Made

- **Only work needed for Thursday stays in release 21; the rest is marked 22.** (Irina)
- **A Flex IQ feature is needed to decode the new Flex-Port error codes for offline storage and Grafana.** (Sergey, Alexander, Irina)
- **Task 178 moves to capability 298 (MVP 3).** (Pavel, Irina)
- **Pavel's faster bill-acceptor status work goes to the next release.** (Pavel)
- **Irina keeps her draft requirement items; they are not reassigned.** Tests follow requirements. (Dmitri K, Pavel)
- **Due dates stay required.** Needed to find stuck tasks and to plan. (Pavel, Irina)
- **A feature is assigned to the person whose story will close last.** (Irina)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexander Biratko | Finish capability 372, send for review, tell Irina when merged | Nov 17, 2026 | High | Needed for Thursday |
| 2 | Irina Shishko | Rebuild the port after Alexander's merge | Nov 17, 2026 | High | |
| 3 | Pavel Frolov | Mark features not needed for Thursday as release 22; review fix versions | Nov 19, 2026 | High | |
| 4 | [Unassigned — needs clarification] | Create Flex IQ feature to decode Flex-Port error codes | TBD | Normal | |
| 5 | Alexander Biratko | Test the power-backup / spray-mode bit on the recycler | Nov 18, 2026 | Normal | |
| 6 | Alexey Khamin | Send Val the state law vs. regulations comparison and ask next steps | Nov 17, 2026 | Normal | Val's request |
| 7 | Dzmitry Chudzinau | Look at Alexey's unstable Flex IQ build | TBD | Normal | Failed twice |
| 8 | Anton Seregin | Verify port tests against a real port | Nov 17, 2026 | High | About 2:30 |
| 9 | Daniil Stauskiy | Commit to stop the Nexus upload and merge PR 1340 | Nov 17, 2026 | Normal | |
| 10 | Dzmitry Chudzinau | Deploy the LTE work to STG | Nov 17, 2026 | Normal | |
| 11 | Ivan Shpak | Connect LTE to a machine for Georgia on STG after the deploy | TBD | Normal | |
| 12 | Irina Shishko | Move task 178 to capability 298 | Nov 17, 2026 | Normal | |
| 13 | Sergey Tsimanov, Anton Seregin | Answer Vladimir's questions in Jira comments on CAP-287 / TINT-118 | TBD | High | Needed by Thursday |
| 14 | Pavel Frolov | Answer the comments on REQ-1833 | TBD | Normal | Alexey's reminder |
| 15 | Vladimir Samusenko | Reassign the feature to Sergey | Nov 17, 2026 | Low | |
| 16 | Irina Shishko | Write features from the Flex capability requirements for autotests | TBD | Normal | |

## Open Questions

- Who handles the Port-157 review list (rules and a list of what we do wrong)? (Alexey)
- Does Flex IQ to Flex-Port Wi-Fi work through the GL 2 router once the MAC is registered? (Pavel, Sergey)

## Dispatch Log

---
*Processed from Teams transcript on November 18, 2026 (scheduled meeting-watcher)*
*Source meeting: Daily Standup meeting*
