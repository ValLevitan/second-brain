# Meeting Summary — Game_Development
**Date:** July 31, 2026, 2:00 PM Eastern
**Duration:** ~34 minutes
**Attendees:** Michael Gottlieb, Juan Martinez, Val Levitan, Efim Podvoiski, Lena Zhukova
**Raw transcript:** [[Meeting_Transcript_Georgia_Game_Math_Performance_Review-July-31-2026]]

## Summary

Weekly game-development review, focused on the Georgia game math and the early field numbers.

**Twin Bison math tuning.** Michael reported the Georgia math is now about where they want it. They dropped the 10 out of the royals and shifted the paytable so the high-value "oil"/royal symbols come up much less and the animals (bison, big bear) come up more. The big change was moving to **fractional pays** (pays under a dollar) — Michael questioned the original Peach paytable logic with Efim (it was copied from unsuccessful IGT games) and the fractional-pay version is now behaving correctly. They also bumped up the frequency of the reel-3 wild (bison runs across the screen and turns the reel wild), and Michael sent Lena notes on that behavior. Free spins are "a hammer" and playing well; a couple of bugs remain (sound effect for the bison lock / snow-and-ice freeze). For South Dakota they worked through win-capping messaging across all combinations (win cap in free spins, with progressive pending, in base game, etc.); the requirement was updated and a new build is expected.

**Early Georgia performance data.** Juan cautioned the data is far too early to be conclusive — some machines have only 2–6 days, the longest 16 days; he wants another ~30 days. He color-codes on ~$1,500 coin-in and ~$200/day as a solid number. Hold is running high in JVL's favor so far: games are set at 92% base + 2% to the meter = 94% all-in. Juan wanted the games close to the well-performing original Peach setups; if numbers slip they will cut the progressive 1% before touching base percentages. Spread across games is smooth; Ocho swung from bottom to top depending on location; Rodeo Queen is lower than expected (Michael's theory: the market is ~70% male and women bet less/less aggressively). Arc is a standout at $4–5k coin-in days. Jackpot Rush titles with "Add Any Bet" are pleasing and improve as meters run.

**Themes and roadmap direction.** Michael wants another pass at Egyptian themes (competitors are going heavy there; JVL has Keops Wild and others needing an art pass), noting competitors have gone light on Chinese. Rodeo/horse themes are not disliked — possible "Jackpot Rodeo" reskin of Jackpot Rush. La Rosa still fits Hispanic locations. Midnight Money and other character-less games should keep the conventional paytable (the simplified/character paytable only helps games with a strong character focus).

**Attract ("coming attraction") videos.** Competitors run full-screen attract videos with no buttons when a machine has no credits. Lena plans to have Vitaliy start recording videos next week (Jackpot Rush, Lines, Waves games first, which are in good shape), then fine-tune Lion and Bison. The underlying attract flow code has not been built by Anton yet, and Anton is on vacation next week — Lena may reassign the attract flow to Igor (who built it for South Dakota). Juan will gather competitor parameters (video length, how many games shown, touch-to-start messaging) by next week.

**Submission timing.** Given the remaining work and Anton's absence, Michael recommended pushing the Georgia submission out a week or two past mid-August to get it right. Juan agreed. A concern flagged: Jackpot Rush still shows "max bet required to win" messaging when it is now available on any bet — incorrect messaging that may be dampening play and must be fixed.

**Lion game bug.** Lena flagged that the Lion pick-bonus "click" behaviour is broken (you always get lion; the click-spins stacking/clicking area is not working). Michael was frustrated that a years-old, proven game could regress from what is essentially an art swap (only reel and symbol sizes changed); he suspects the outsourced team's revision control reintroduced an old bug. Expected fixed in the next build, along with golden arrows in free spins and full Locket Wild stages. Audio: Michael sent Vladimir the free-spins vibe reference ("Rawhide"/"Bonanza" for Twin Bison); Lena to confirm with Anton and Vlad that the new audio is inserted.

**Economy hardware platform.** Val reported a substantial experiment with what he expected to be the "economy" hardware board — results "spectacular." It is not a faster processor; it is a different **RK-based (Chinese) architecture**, the same they use for transactional products. It runs six games at 60 FPS. The only issue was a momentary freeze on the base-to-bonus transition, traced to minimal memory; they are expanding to 16 GB, which should handle six games with transitions (even 25–30 FPS would be acceptable). FP7 remains the elaborate/high-end platform. Michael noted Stern Pinball similarly migrated its platform to Raspberry Pi.

**Strategy — Nebraska next.** Val, candidly, said he is overwhelmed ("frozen") by the number of simultaneous initiatives — the hardware switch, moving to the Novo/Omni platform, the new "Galaxy" backend, and changed internal file-keeping and production-push processes all at once. Direction: after Georgia V3, the battleground shifts to **Nebraska** starting September — it is a fertile market that would immediately help the bottom line; Nebraska is currently not performing and they have eliminated the 25-cent bets. South Dakota is performing "okay" and should improve with Kinos out; PD still has to finish South Dakota (paused for Georgia).

## Decisions Made

- **Push the Georgia submission out a week or two past mid-August** to finish the math, messaging, attract videos, and bug fixes properly. (Michael, Juan)
- **Adopt fractional pays and the retuned Twin Bison math as the Georgia standard**; cut the progressive 1% before base percentages if field numbers slip. (Michael, Juan)
- **Keep the conventional paytable for character-less games (e.g. Midnight Money);** reserve the simplified/character paytable for games with a strong character. (Michael)
- **Shift the next battleground to Nebraska from September, after Georgia V3.** (Val)
- **Move the economy hardware to the RK-based board with memory expanded to 16 GB.** (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Lena Zhukova | Deliver the next Georgia build with the Lion pick-bonus/click bug fixed, golden arrows in free spins, and full Locket Wild stages; contact Anton before his vacation | Next few days | High | Build crashed on Bisons yesterday/today; fixes are on Anton's side |
| 2 | Lena Zhukova | Start recording attract/coming-attraction videos (Vitaliy) beginning with Jackpot Rush, Lines and Waves games; resolve who builds the attract flow (Anton vs Igor) given Anton's vacation | Next week | Normal | Full-screen, no-button attract when no credits; Anton hasn't built the flow code yet |
| 3 | Juan Martinez | Collect competitor attract-video parameters (length, number of games shown, touch-to-start messaging) and confirm whether the new Georgia installs are fresh or replacing prior Peach units | Next week | Normal | Needed before setting JVL's attract behaviour |
| 4 | Michael Gottlieb / team | Fix the Jackpot Rush "max bet required to win" messaging to reflect any-bet availability | Before submission | High | Incorrect messaging may be suppressing play |
| 5 | Val Levitan | Expand the RK economy board memory to 16 GB and confirm it handles six games with base-to-bonus transitions; report a timeframe | TBD | Normal | Momentary transition freeze traced to minimal memory |
| 6 | Michael Gottlieb (PD) | Finish South Dakota (win-capping build) once Georgia work allows | TBD | Normal | South Dakota was paused to focus on Georgia |

## Open Questions

- Whether the new Georgia installs are fresh placements or replacements of the earlier Peach vertical release. (Michael, Juan)
- Which competitor attract-video conventions to adopt (length, games shown, touch-to-start). (Juan)
- Final Georgia submission date after the 1–2 week push. (Michael, Juan)
- Whether reassigning the attract flow from Anton to Igor makes procedural sense. (Lena)

## Dispatch Log

---
*Processed from Teams transcript on July 31, 2026, 4:00 PM Eastern*
*Source meeting: Game_Development*
