# Meeting Summary — Vertical Roadmap (SD / Nebraska / Texas) + Rage-to-Omni Transition
**Date:** May 7, 2026, 6:02 PM Eastern
**Duration:** 21m 0s
**Attendees:** Val Levitan, Michael Gottlieb, Juan Martinez, Lena Zhukova, Efim Podvoiski

## Summary

Game-development planning call working through the post-Georgia product roadmap and the strategic Rage Studio → Omni platform transition. The conversation moved through cabinet decisions, content sizing for the next vertical release, regulator constraints, and finally a brief read of inconclusive Nebraska performance data.

**Bringing Jackpot Rush + Fiery Ice Link to South Dakota and Nebraska.** Michael opened by raising whether to bring **Jackpot Rush** and/or **Fiery Ice Link** to South Dakota and Nebraska. Juan said the **vertical product** being built for Georgia (with the liquid-glass cabinet) is the basis for both — South Dakota gets it as-is, Nebraska gets a slight variation. The Nebraska variation differs in two specific ways: **no Keno**, and **dual box (secondary skill).** Texas tracks with Nebraska on these. The Nebraska/Texas version has to go through a separate cabinet submission to the regulator, which adds time.

**Content sizing — should we release 20 games at once?** Michael walked through simple math: South Dakota vertical = 3 Keno (Black Hills, Cool Cat, Solar) + 6 Lines and Ways games + 5 Jackpot Rush + 6 Fiery Ice = **20 games**. He raised whether they actually want to release 20 games in one drop, and added a separate concern about whether the cabinet can even support 20 simultaneous pay tables, which is still an open question in South Dakota tied to the *Keno pay-tables maximum supportable game* question. Michael's recommendation: **stagger** — do 2 Jackpot Rush + 2 Fiery Ice in this release, then another 2 + 2 in the *next* SD/NE vertical release. Otherwise the team is selling a tremendous amount of content in one shot, which is unnecessary. Val and Juan agreed: "not necessary."

**Wolfpack-vs-Twin-Bison decision: deferred to data.** Michael also raised that Wolfpack would be part of the SD/NE vertical content, with **Twin Bison** as additional content. Juan pushed back on locking the order: don't pre-commit to Wolfpack first vs Bison first for SD until Georgia data comes in. If **Bison is doing phenomenal in Georgia, lead with the proven product** and make Wolfpack the second vertical release. Michael accepted the deferral. Lena confirmed Wolfpack is in scope but Bison is *not* in the *Georgia* asset set. The order question only matters for SD/NE.

**The platform decision — Rage vs Omni, and when.** Lena raised the operationally critical question for the design pipeline: *what cabinet, what framework — continue with Rage Studio, or move to Omni?* — because Omni is "a huge project" requiring all games to be rebuilt. The discussion landed:

- **Juan initial framing:** vertical SD product needed by Q4 2026 if possible. **Lena: Q4 on Omni is "absolutely impossible." Michael: "no way in hell."** They can only deliver Q4 on Rage.
- **Juan accepts staying on Rage** for the SD vertical end-of-year release. Lena noted that on Rage, only **one new game asset (Solar King)** is needed for SD; everything else can be reused, including the Jackpot Rush vertical assets they're already producing for Georgia.
- **Nebraska / Texas should also stay on Rage** alongside South Dakota. Michael was direct: *"do both or do none, because 90%+ of the work is applicable to both. The only difference between the two markets is the dual box and the lack of Keno."* Splitting SD on Rage and Nebraska on Omni in parallel would mean *creating two entirely different versions of software with the exact same games in two different platforms*. Juan accepted.
- **Texas insertion path:** Texas can be entered *without regulatory approval*, which makes it the fastest. Juan: *"we could get it into Texas without any approval, which just makes it faster, and then work backwards into Nebraska."* Michael agreed but reinforced that the entire SD/NE/TX vertical wave should be on Rage.
- **Omni first product → Q1 2027.** Val articulated his strategic preference: he wants the first Omni release to ship in **2027** and to encompass **three new cabinets** running on the **FP7** hardware. He acknowledged it is a "massive, massive release."
- **First Omni market = skill markets.** Val's call: *"the best place for Omni is skill markets."* Sequencing implication — Omni doesn't enter via the strict regulated keno/SD market; it enters via skill (Nebraska/Texas-like) first.
- **South Dakota stays on Rage longer than the others** because *"there's a regulator in place there that is a bit of a sore spot and will delay us"* — South Dakota Omni doesn't make sense right now. Juan: move SD to Omni later, after first establishing Omni elsewhere.

**Transition discipline.** Efim asked whether Omni work could start in parallel with the SD Rage release (since SD only needs Solar King new). Lena pushed back: Nebraska + Texas still need real work on the existing games — sizing and positioning adjustments analogous to the Georgia liquid-glass work — and many of the existing games don't have liquid-glass yet. Michael's framing: *"You just have to have a hard stop and say, 'this is the last Rage release.' Then as people roll off whatever they're working on, they move on to the next thing. It's not overnight."* Lena's proposed transition moment: **after** the SD/Nebraska/Texas vertical releases are complete on Rage, the team will have headroom to prepare the first Omni product. Juan confirmed that even after Omni starts, **Rage Studio products will continue to be supported** — bug fixes, tweaks. Lena, Michael, Efim all confirmed: yes, absolutely.

**Hardware confirmation for Omni.** Lena asked Val to confirm that **D27** in the Omni line would use the same updated hardware (the **FP7 board**) as the vertical. Val: *"Yeah, of course."* Both D27 and D43 are in scope for Omni.

**Cumulative-release model — implication for Omni.** Michael surfaced an architectural tension: Juan has stated a preference for **cumulative releases** (adding more games to everything already released). On Rage that's iterative. On Omni, switching means *going back and converting all already-released product*, because cumulative doesn't bridge across platforms cleanly. Juan acknowledged the trade-off but didn't commit a resolution.

**Decision direction (working consensus by the end):**
- SD vertical (D27 + Keno) on **Rage** → end of 2026.
- Nebraska vertical (no Keno, dual box) and Texas vertical on **Rage** alongside SD → end of 2026.
- First Omni product **early 2027** in skill markets (Nebraska/Texas type).
- Three new cabinets + FP7 + Omni = **2027** big release.
- D27 next on SD: not urgent. Adding Keno-via-this-next-release "buys us another year" before needing a new D27 product. No need to rush D27 in the next nine months.

**Nebraska 9-day data — inconclusive.** Juan reported pulling a quick analysis on Nebraska performance pre- vs post-installation: 9 days before, 9 days after. The data is **not apples-to-apples**:
- The "before" window included **two weekends**; the "after" window includes **only one weekend**. Weekends are the busy days, so the before naturally looks better artificially.
- The "after" window shows several days of **zero play** on multiple machines (yellow spots in the report). Cause unclear: installation timing, machines down, or possibly **watchdog reboot failures** — Juan doesn't think it's watchdog, but Denis needs to investigate mechanically.

Juan's call: discount the comparison; collect more data. **Operational pain point:** Denis has to drive 3 hours to one Nebraska location and another 2 hours to the second to collect data — and the customers don't want to do it themselves. Val: "Basically inconclusive." Juan: agreed.

**Lena missed the Nebraska email loop.** Juan apologised for forgetting to copy Lena on the Nebraska numbers. Customers were *a little excited* — anecdotal good sign — but the formal numbers are too thin.

## Decisions Made

- **SD / Nebraska / Texas vertical releases all on Rage Studio through end of 2026.** No platform split between them — 90%+ of the work is shared. (Lena + Michael + Juan + Val.)
- **First Omni release lands in Q1 2027 in skill markets, not in South Dakota.** (Val.)
- **The first Omni release will be a "massive" multi-cabinet launch: three new cabinets, FP7 hardware, both D27 and D43.** (Val's stated goal.)
- **Stagger content release: do not release all 20 candidate games at once.** Pace 2 Jackpot Rush + 2 Fiery Ice per vertical release, next batch in the following vertical release. (Michael's proposal, accepted by Val + Juan.)
- **Hold on Wolfpack-vs-Bison ordering decision** until Georgia performance data is available. (Juan, accepted by Michael.)
- **Cabinet feasibility question stays open for SD:** can the SD cabinet support 20 simultaneous pay tables (or whatever the cap actually is)? — see Open Questions.
- **Texas to be entered via the no-regulator-approval path first**, then work backwards into Nebraska. (Juan.)
- **South Dakota stays on Rage longer than NE/TX** because of regulator friction. SD migrates to Omni at a later date. (Juan + Val.)
- **Rage Studio products will continue to be supported in parallel with Omni** — bug fixes/tweaks remain. (Lena/Michael/Efim, confirmed for Juan.)
- **D27 in Omni uses FP7 board, same as the vertical.** (Val.)
- **Discount the Nebraska 9-day data as inconclusive.** Wait for more data; investigate the zero-play days mechanically. (Juan, accepted by Val.)
- **Solar King is the one net-new game asset for the SD vertical release on Rage.** All other content is reused from Jackpot Rush vertical work for Georgia. (Lena.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Juan Martinez | Plot the SD / Nebraska / Texas vertical sequencing on a calendar and bring information to the next call | Next product-development meeting | High | Specifically: what comes after the SD/NE/TX vertical wave, and exactly when Omni starts |
| 2 | Juan Martinez | Tell the team what the *first Omni product* should be (cabinet, market, content) | Next call | High | Lena: "just tell us what kind of product you would like to see first" |
| 3 | Juan Martinez | Get Denis to explain the mechanical cause of the zero-play days in the Nebraska "after" window | Within the next data-collection cycle | Normal | Watchdog reboot failure, install timing, or machines down — unknown |
| 4 | Juan Martinez | Continue collecting Nebraska performance data; do not act on the 9-day comparison | Ongoing | Normal | Current data is not apples-to-apples |
| 5 | Lena Zhukova | Confirm and plan SD vertical concept work on Rage with Solar King as the only new asset | Starting now | High | Concepts already starting; needs locked cabinet + framework answer (now confirmed: Rage Studio, current vertical cabinet) |
| 6 | Lena Zhukova | After SD/NE/TX vertical releases complete, transition art/dev team toward first Omni product | After the SD/NE/TX wave ships | Normal | Hard-stop pattern per Michael: declare last Rage release, then roll off to Omni |
| 7 | Michael Gottlieb | Continue staggering Jackpot Rush + Fiery Ice content across vertical releases (2 + 2 per release) | Ongoing per release plan | Normal | Content pacing decision |
| 8 | Val Levitan | Define the three new cabinets + FP7 vision for the 2027 Omni release | Sometime in 2026 | Normal | Strategic Q1-2027 anchor; no near-term deadline but needs articulation |

## Engineering Signals

### Confirmed Signals

- **ADR — All SD / Nebraska / Texas vertical releases stay on Rage Studio through end of 2026.** Rationale: shared 90%+ of work; Omni rebuild is infeasible in this window per Lena ("absolutely impossible") and Michael ("no way in hell"); Q4 2026 SD release is achievable on Rage with only Solar King as net-new content.
- **ADR — First Omni release targets Q1 2027 in skill markets, not in the SD regulated market.** Rationale: SD regulator friction would compound platform-migration risk; skill markets give Omni a clean first launch.
- **ADR — Omni V1 = three new cabinets + FP7 board + D27 + D43.** Multi-cabinet "massive release" rather than incremental.
- **CAP — Cumulative-release model carries forward in Rage; Omni resets it.** When Omni launches, the existing Rage content does not automatically port — it would require explicit conversion to participate in the Omni cumulative model. This is a known and accepted cost of the transition.
- **CAP — Parallel Rage support continues after Omni launches.** Bug fixes and tweaks on Rage are not retired; the team commits to dual-platform maintenance during transition.
- **Engineering Solution — Hard-stop transition pattern.** Per Michael: designate a specific last Rage release; do not have any team member working on both platforms simultaneously; people roll off to Omni as their current Rage work completes. Not overnight, not gradual mixed work.
- **REQ — FP7 hardware standardisation across Omni cabinet variants (D27 + vertical).** Val confirmed explicitly for Lena.
- **REQ — Nebraska vertical configuration differs from SD in exactly two ways: no Keno + dual box (secondary skill).** Texas tracks with Nebraska.
- **REQ — Texas market entry path: regulator-approval-free.** Material to sequencing decisions.
- **Engineering Solution — Content release staggering.** 2 Jackpot Rush + 2 Fiery Ice per vertical release, not full content drop. Avoids over-releasing 20 games in one window.

### Suspected Signals

- **Possible CAP — Cabinet maximum simultaneous pay-tables limit.** Michael flagged that whether the SD cabinet can support 20 simultaneous pay tables (vs whatever the actual maximum supportable game count is) is an unanswered question. — *Val, does this need formal capacity tracking against the cabinet spec? It came up as an *unanswered* question, not a resolved one.*
- **Possible REQ — Cabinet submission timeline for regulator-approval markets (SD).** Implied throughout but not quantified. The "slightly longer process" framing for SD suggests a hard duration that should be tracked as a known constraint.
- **Possible ADR — Data-driven product ordering decisions.** The Wolfpack-vs-Bison decision being deferred until Georgia data lands establishes a pattern: don't pre-commit content-ordering decisions until proven performance data exists for related content. — *Val, worth formalising this as a JVL product-roadmap discipline?*

## Open Questions

- **Cabinet maximum supportable game / pay-tables count for the SD vertical.** Still unanswered — gates the "do we release 20 games at once" question even if the answer is no, because the team needs to know the ceiling for future planning.
- **Wolfpack vs Twin Bison ordering for SD vertical.** Pending Georgia performance data.
- **What is the *first* Omni product (cabinet + market + content)?** Lena and Michael both said: Juan to define.
- **Cause of Nebraska zero-play days.** Watchdog reboot failure? Install timing? Hardware down? Customer-side not playing? Denis to investigate mechanically.
- **Bison status in Georgia content set.** Lena: Wolfpack is in scope for Georgia, Bison is *not* — confirm this hasn't shifted.
- **D27 next on SD timing.** Decision was: not in the next nine months. But after that, when?
- **How does the cumulative-release model behave across the Rage→Omni boundary** beyond "go back and convert"? Open architecturally.

---
*Processed from Teams transcript on May 22, 2026*
*Source meeting: Game_Development (20260507_140226)*
