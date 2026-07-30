# Meeting Summary — GA-V2 schedule
**Date:** May 4, 2026, 4:30 PM ET (ran ~56 minutes)
**Duration:** ~56 minutes
**Attendees:** Val Levitan, Lena Zhukova, Juan Martinez, Michael Gottlieb

## Summary

The meeting was a working review of Lena's Jira-based schedule for the GA-V2 (Georgia release). Val opened by asking to focus on the schedule and quickly anchored on **IP-966 (Liquid Glass for Georgia release)**, sub-feature **AA-5737**, asking whether the many features under it are mostly copy-paste or unique implementations. Lena explained they are mostly unique — some shorter, some longer — and that the team estimated them in detail because Dima Khandel has already started assembly work on Liquid Glass home screen, UI details, and the progressive bonus.

Val pressed on the **bottleneck question**: is Dima the constraint, or is preparation of graphic assets the constraint? Lena's view: it's balanced — even if Dima got all assets at once he'd save "maybe one week, ten days at most" against the end-of-June target. She reiterated that the schedule was already aggressive when set. Val asked her to drop the date anchor and reason from first principles: if assets came faster, Dima could move faster — Lena conceded "a little bit faster." Juan asked whether reallocating to feed Dima would push South Dakota off; Val said he didn't see a forced trade-off yet because he hadn't gotten to that level of analysis.

Val then shared his screen and filtered the Jira board by Anton and Igor (the integration developers). He showed that **the developers are not actually scheduled on Liquid Glass yet** — current assignments are Twin Bison, Crescent City Carnival (July), keynote support, and South Dakota work (Anton on Cool Cat Dinner game, Igor on South Dakota attraction mode). Lena clarified this is because **the integration portion of the schedule has not been built yet** — they have not yet decided who integrates what for GA-V2. Detailed scheduling so far covers only Liquid Glass graphics work (Dima + artists), not programmer integration. Val agreed: "for liquid glass, integration is not the bottleneck" — the conversation should focus on graphic designers.

Val zoomed in on the Jira assignees in the current detailed schedule and pointed out that **the assignees are essentially Lena and Natalia**, while Anastasia and Julia are listed as reporters, not assignees. He argued that Anastasia — the company's strongest animal animator — is being held back from GA-V2 because she's been allocated to Twin Bison for the August show. Lena pushed back: Bison is a complex new game with new math, gameplay, transitions and animal animations, and Anastasia needs to start now to deliver Bison and Lions Riches as flagship pieces for the August show. She emphasized the schedule is not yet final — only Liquid Glass and art assets have a detailed plan; programmer/integration scheduling and the rest of the artist work (Natalia, Julia, Artur, Vitalik) is the subject of tomorrow's working session.

Michael challenged Val's framing as "illogical" — characterizing it as "the team builds a schedule, you tell them you want X but it should be Y." Val pushed back: he is not arbitrarily compressing time, he is trying to identify the bottleneck (which the schedule, when filtered, reveals as Natalia) and whether resources locked to August deliverables (Anastasia, Julia) could in principle be reallocated to push GA-V2 out the door earlier. Michael acknowledged the trade-off question is fair but invoked "nine guys can't make a baby in one month." Val agreed with the principle but maintained the schedule's bottleneck is real and identifiable.

The conversation then surfaced **a deeper alignment question: does GA-V2 need a mid-June release at all?** Juan stated his actual priority is the **August show**, not a July field deployment, and that pushing for a July 1 release into Felipe's hands is unlikely to yield meaningful field data because: (1) Felipe is currently consumed with rolling out the **watchdog timer**, in which an issue was discovered today (reproducible on one specific software set, root cause unknown — Pavel, Irina, Ivan, Felipe are working it on a Teams chat Val was not on); (2) gift cards go live July 1; (3) the July 4 holiday eats the early month; (4) Georgia operators are slow and historically don't move in the month before a gaming show because they want to see new product first; (5) any field deployment requires Felipe to give machines away to good locations to get fair data. Val and Juan agreed the angle of attack is to engage Felipe and ensure if anything ships, it goes to **hand-selected good locations**.

Val noted he had been operating under the assumption that mid-June was a real target — and if there is no usable field test before the August show, "then why push?" Juan and Michael both said the August show was always the actual target, and the aggressive Liquid Glass / match-3 progressive push was to hit August with a materially differentiated product (new JVL look and feel), not to chase a July field test. Val agreed not to dispute August deliverability — he believes one new game (Bison or Lions) is sufficient, two would be excellent. Michael and Juan both want both Bison and Lions Riches at the show. Val warned that without a live field test, the August show product carries elevated risk for things going wrong.

Lena asked, given the new framing, how to structure tomorrow's planning meeting — should she pull Anastasia off Bison? Val said he would do it anyway. Michael cautioned against shifting Anastasia until tomorrow's evaluation — moving her risks Bison for the show. Juan said his earlier mental model was Anastasia would jump onto a Liquid Glass piece for a week or two, then return to Bison, but deferred to Lena. Lena will work the question tomorrow.

The meeting closed with Michael asking Val whether he had seen the latest Lions Riches image; Val had not. Lena was asked to show it.

## Decisions Made

- **No formal commit on the GA-V2 release date** — decision deferred until Lena delivers the full detailed schedule (including programmer integration time) on May 5. (Endorsed by Val, Juan, Michael)
- **August show is the authoritative delivery target** for the new JVL look-and-feel package (Liquid Glass, match-3 progressive, Twin Bison, Lions Riches). A mid-June or early-July deployment to Felipe is no longer treated as a hard objective. (Confirmed by Juan and Michael; Val accepted the framing)
- **Anastasia stays on Twin Bison for now**, pending tomorrow's planning session. Lena will evaluate the most efficient redeployment but won't move her unilaterally. (Endorsed by Michael; Lena to execute)
- **Felipe rollout angle:** if anything ships to him in July, it must go to hand-selected good locations to yield real test data. Val and Juan to engage Felipe on this. (Agreed by Val and Juan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Lena Zhukova | Run the detailed scheduling working session at 9:15 AM ET May 5 (~1 hour or longer). Output: integration assignments for Anton/Igor + task/story breakdown for Natalia, Julia, Artur, Vitalik covering everything beyond Liquid Glass graphics | May 5, 2026 | High | Gate that lets Val confirm or revise the GA-V2 timeline |
| 2 | Lena Zhukova | After the planning session, message Val with a time to review the updated schedule together | May 5, 2026 | High | Drives the follow-up alignment meeting |
| 3 | Val + Lena | Schedule-review meeting to walk through the updated detailed schedule | May 5, 2026 (after Lena's planning) | High | Closes the loop opened in this meeting |
| 4 | Lena Zhukova | Decide and propose whether/how to redeploy Anastasia (keep on Bison vs. reallocate vs. short rotation); bring recommendation to the review | May 5, 2026 | Normal | Michael's concern about Bison risk for the show |
| 5 | Juan Martinez | Add Val to the Teams chat Felipe started about the **watchdog timer** issue (Pavel, Irina, Ivan also on it) — reproducible on one software set, root cause unknown | May 4, 2026 | High | Val needs visibility to react |
| 6 | Val + Juan | Engage Felipe to understand his rollout plan: gift cards live July 1, July 4 holiday, watchdog rework, hand-selected good locations | This week | Normal | Determines whether a partial GA-V2 cut is worth pushing for early July |
| 7 | Lena Zhukova | Show Val the latest Lions Riches image | May 4–5, 2026 | Low | Val missed the prior meeting |

---
*Processed from Teams transcript on May 5, 2026*
*Source meeting: GA-V2 schedule*
