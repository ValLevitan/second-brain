# Meeting Summary — Daily Standup meeting
**Date:** November 26, 2026, 3:45 AM Eastern
**Duration:** 40 minutes
**Attendees:** Pavel Frolov, Alexander Biratko, Alexey Khamin, Andrei Bosik, Anton Seregin, Dmitri Kovalchuk, Dzmitry Chudzinau, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Jira_Tasks_for_Non_Code_Work_and_MVP2_2_Dev_Branch-November-26-2026]]

## Summary

**Jira tasks for non-code work.** Alexander spends much time writing NOVA requirements, but it does not show in Jira. He asked if such work should get its own tasks. Irina: earlier the rule was not to make such tasks. Vladimir: spikes already exist for work with no code. Pavel: a task makes sense only if the result must be documented; otherwise the requirements carry the labels NOVA and NOVA engine and can be listed by label. Dmitri: Emma often finds small organizational tasks after meetings (add something, write to someone), and there is no project for them. He proposed an organizational project. Example: from the Nov 25 MVP 2.1 meeting, the alpha build to Andrei Klimovich and Alekseev's Wi-Fi module test are not recorded anywhere. Pavel: Val has always been against such projects; an alternative is a separate issue type inside the existing Capabilities and Requirements projects. No decision.

**Bill validator as a service.** Alexander is adding hooks so the RIS recycler can be tested almost without touching it. Button presses, door opening, screen taps and screenshots are automated. Only the real recycler still needs cash put in; a virtual version exists. Pavel: Evgeny asked if the bill validator module (EBDS protocol) should become a separate service. Alexander: the code is Java; the only native part was the serial-port exchange, which they rewrote, so it runs on RK. It is not a separate service. Both agreed a service would be a plus: validators and the emulator could be switched on the fly.

**Flex-Port update failure (Alexey).** Alexey made about 20 test firmwares, one for each update stage. The code itself has a comment: after a certain stage the device cannot return to the base application, because it is already erased. This contradicts the requirements linked to "port 13" (as heard), which say it must return. That item is closed. Pavel: write to Alekseev to ask if the old application can be kept. Irina: we cannot cancel the requirement without his confirmation. Alexey will list his findings.

**GitHub variables and cluster (Andrei Bosik).** Andrei reworked secrets and variables for the Flex products and the Flex recycler on main. Anyone building from a branch must pull main. Cluster updates go on until the New Year holidays: more than 100, each a pause of about 2 minutes. One big update of about 2 hours will come later, not this week; he will announce it.

**Review rounds (Anton Seregin).** Anton closed items 235 and 130 and is reviewing 128 and 234. The local Claude review now runs up to 4 rounds, even for text changes, and can take an hour. Vladimir: the standard says self-review before the pull request until no issues are found, at most 4 rounds; the bot then reviews once more on the pull request. Alexey is working on narrowing the reviews after the bot's first comments (check only the changes, use medium or high effort, not the highest). Most time and tokens go to these follow-up reviews; he has statistics. Pavel: much review time is wasted on text changes; they will keep improving it.

**MVP 2.2 branch.** Dzmitry is sending MVP 2.2 questions to Andrei. Pavel: capabilities whose text is stable should move to the next status; Val saw that nothing for 2.2 is planned yet. Dzmitry: 2.2 work starts now, but 2.1 needs at least another week; where does the code go? Agreed: a "dev" branch off main; when 2.1 is released, it merges into main. Andrei Bosik: treat it as an experiment, not a standard yet. Dzmitry asked to keep it out of the reports; Andrei will do that.

**RIS for Sebastian (Ivan).** Ivan is checking the tests Claude wrote for Sebastian. He waits for fixes (number heard as 730) and hopes to give Sebastian a build with all fixes at the end of the day. Sergey's CMS changes must be released to STG; there is no task for it, and Pavel said to make one. The font in the new field Sergey added looks a little too big on STG; Ivan will send a picture. Pavel: a small front-end change is also needed (task about 146). Andrei: the accounting host may need internet access today; Ivan will tell him later.

**SMS release from main.** Andrei: the policy now lets the SMS release go out only from main. Sergey disagreed: the release action trims files and commits straight to main, so a bad release means reverting commits made by Git. Earlier they used a separate release branch. Andrei: release now, discuss later; either can adjust the action or the policy.

**Flex recycler to production — not now.** Andrei Bosik proposed adding Flex recycler support to the over-the-air update and putting that build on production, because the customer will soon ask. Dzmitry, Sergey, Irina and Alexey objected: no recycler in the current MVP, no requirements for it, no guarantee it affects nothing; let them test on STG. Andrei gave in.

**Master role capability.** Sergey finished SMS, will release it, and can start MVP 2.2: master registration, authentication and authorization, and report visibility. Location billing tasks may go to Nathan. Pavel moved the master capability to Accepted; Sergey should move it to To Do and create its features. Pavel explained the status flow: Proposal (first view) → negotiation between development and product owner → Accepted (all agree) → assign MP → To Do.

**Tests and dates.** Vladimir closed test items 116 and 107; 108 and 111 are in work. Pavel: far too many tests; more people are needed. A student will join soon (Alexander). Dmitri: Irina has 14 overdue items; they are MVP 2.2 items not yet assigned to people. Irina will remove their dates and plan them later.

## Decisions Made

- **Create a "dev" branch off main for MVP 2.2 work; merge it into main when 2.1 is released.** — 2.1 needs at least another week and 2.2 work starts now. Treated as an experiment, not a standard yet. (Pavel, Andrei Bosik, Dzmitry)
- **Do not put Flex recycler support on production now.** — No recycler in the MVP and no requirements; testing can be done on STG. (Dzmitry, Sergey, Irina, Alexey; Andrei Bosik agreed)
- **Ask Alekseev before changing the Flex-Port update requirement.** — The requirement cannot be cancelled on the team's own reading of the code. (Pavel, Irina)
- **Master capability is Accepted.** — Next it goes to To Do with features. (Pavel)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexey Khamin | List his findings on the Flex-Port update failure (base app erased) | TBD | High | Input for the letter to Alekseev |
| 2 | Pavel Frolov | Write to Alekseev: can the update avoid erasing the old application? | TBD | High | Requirement conflict |
| 3 | Andrei Bosik | Keep the MVP 2.2 dev branch out of the reports | TBD | Normal | |
| 4 | Andrei Bosik | Announce the 2-hour cluster update in advance | TBD | Normal | Not this week |
| 5 | Everyone | Pull main into working branches after the variables change | TBD | Normal | |
| 6 | Sergey Tsimanov | Move the master capability to To Do and create its features | TBD | Normal | |
| 7 | [Unassigned — needs clarification] | Create a task to release Sergey's CMS changes to STG | TBD | High | Sebastian waits for it |
| 8 | Ivan Shpak | Give Sebastian a build with all fixes | Nov 26, 2026 | High | "End of day" |
| 9 | Ivan Shpak | Send Sergey a picture of the font size issue on STG | TBD | Low | |
| 10 | Sergey Tsimanov | Fix the font size in the new field on STG | TBD | Low | |
| 11 | Ivan Shpak | Tell Andrei Bosik when the accounting host needs internet access | TBD | Normal | |
| 12 | Sergey Tsimanov | Release SMS | TBD | Normal | From main |
| 13 | Alexey Khamin | Narrow the follow-up Claude reviews after the bot's first comments | TBD | Normal | |
| 14 | Irina Shishko | Remove dates from unassigned MVP 2.2 items and plan them later | TBD | Low | |

## Open Questions

- How to record non-code and organizational work in Jira: separate project, separate issue type, or labels only. Raised by Alexander and Dmitri; not decided.
- Whether the bill validator module becomes a separate service. Evgeny asked; Alexander and Pavel in favour; no task set.
- How the SMS release from main should work (release action commits to main). Sergey vs Andrei Bosik; to discuss after the release.
- Terms heard unclearly: "port 13" (the closed item with the update requirements), fix number "730" and the name "Дженни", task "146", "в леге" (where SMS is released).

## Dispatch Log

---
*Processed from Teams transcript on November 26, 2026, ~10:00 AM Eastern*
*Source meeting: Daily Standup meeting*
