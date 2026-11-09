# Meeting Summary — Game_Development
**Date:** October 30, 2026, 2:00 PM – 3:09 PM Eastern
**Duration:** ~69 minutes
**Attendees:** Val Levitan, Michael Gottlieb, Efim Podvoiski, Lena Zhukova
**Raw transcript:** [[Meeting_Transcript_Game_Development_Class_A_Party_Time_and_Colombia_Refresh-October-30-2026]]

## Summary

**Nebraska dual box.** Michael changed the winning-spin flow. Reels stop, the dual box comes up, and the win meter shows 0. The game racks only after the player picks the correct coin. The bonus also triggers only after the correct pick. Michael told the developers yesterday; a new build is expected soon. Val asked if showing 0 is good. Michael is "a hundred percent" sure.

**Class A Georgia — free spins and party time.** Free spins are capped at a $50 win. Michael and Efim worked through the flow: party time can trigger on the spin after free spins; a cash-out or a bet change disables it. Michael's rule is that party time pays at least twice, but after free spins there may be money for only one. Michael thinks one is fine ("surprise and delight"). Val: "seems logical."

**Party time value and frequency.** Efim: party time frequency depends on the bet, because the award is always $50. Val argued that most players bet about $1 to $1.50, not $5–$6. At those bets party time is too rare. He prefers smaller wins more often ("3 × 10 is better than 1 × 50"). Val's facts on the competitor Class A machine (Primero): some locations make $6 a day per machine, some $40; operators do not find the play interesting; "it does not have legs." The market excitement is the loophole: today about 47,000 machines, Class A could take it to about 100,000. Felipe played low bets next to Val and lost; Val won about $800.
Michael first wanted to start with $50 and test. After Val's facts he said "Okay, I'm sold." New approach: treat party time as a low-level mystery progressive. The value goes up with the bet (example 10, 20, 30, 40, 50). Within one party time session all wins have the same value. Fund it by shaving the top of the paytable. Michael did not accept Val's idea of mixed values in one session; Val said he was only talking, not designing. Efim said many math questions are still open (how to make exact $10 wins, etc.).

**Paytable cap by bet.** On the competitor game the top award stays the same at higher bets. Val called this "insulting." Efim: "We will not do it." Efim shared older data (from Jacob): about 25–29% of money comes from $3–$5 bets.

**Bet levels and VDEC.** Val: this is a street business, not a casino; five bet buttons from 50 cents to $2.50 are fine; no need for $5. Michael wants 25-cent up/down steps on screen, like Aristocrat, IGT and Light & Wonder. Reason: players can bet exactly the money left (e.g. $1.75) and zero out — less friction, and "set it and forget it." Efim: 25-cent steps mean about twice the math (10 maths instead of 5) and more testing, but he trusts Michael's call. Val agreed with the zero-out reason and said "set it and forget it" is the compelling argument. Michael would not spend money on a VDEC for a Class A cabinet; Val: all you need is one slam button.

**Georgia V4.** Michael asked about the new curved cabinet for the fall Georgia show. Val: there will definitely be another Georgia software release. Michael has the games blocked out, including "perceived persistence" games. Val supports this and calls them large format games, like Bison.

**Colombia.** JVL's Colombia contracts expire December 2027, so the whole installed base needs new games. Val wants Bison, wolves and lions — the updated Georgia games made into Class 3. Minimum 6, maximum 12 games. Most machines are horizontal, dual screen, with VDECs. Platform is NOVA (Lena asked). Efim: Colombia used plain Class 3 math, no special denomination math. Michael has a top-games list for Colombia: pub crawl is popular; fruit games were popular, but Val thinks they have run their course. Diamond Link did not do well there. Michael will talk with Martha. Val's advice: give her a list of questions, then verification questions; she researches with operators and answers with facts, not opinion.

## Decisions Made

- **Nebraska: win shows 0 when the dual box appears; rack and bonus only after the correct coin pick.** — Better flow now that the win meter mechanic is gone. (Michael; Val did not object)
- **Class A party time moves away from a flat $50: value scales with the bet and hits more often, like a low-level mystery progressive with a fixed value per session.** — Most players bet about $1; the competitor's flat $50 model is not earning. Considered and superseded: start with $50 and test. (Val, Michael)
- **No paytable cap at higher bets.** — Capping gives no reason to bet more. (Efim, Michael, Val)
- **Class A uses on-screen bet up/down in 25-cent steps (Aristocrat/IGT style).** — Lets players zero out credits; less friction. Accepted despite double math and test work. (Michael; Efim and Val accepted)
- **There will be a Georgia V4 release.** (Val)
- **Colombia refresh: NOVA, Class 3, 6 to 12 games, based on the updated Georgia games (Bison, wolves, lions).** (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Michael Gottlieb | Play the new Nebraska build with the changed dual box flow and check the feel | TBD | Normal | Developers told Oct 29 |
| 2 | Efim Podvoiski | Work out Class A party time math: bet-scaled values, hit frequency, shaving the top of the paytable | TBD | High | Many open math questions |
| 3 | Michael Gottlieb / Lena Zhukova | Finalize the Georgia V4 game list (incl. perceived persistence games) | TBD | Normal | |
| 4 | Michael Gottlieb | Talk with Martha about the Colombia market (what is popular, what earns) | TBD | Normal | Val: send a question list |
| 5 | Efim Podvoiski | Pull Colombia top-games data for the last 6 months only | TBD | Normal | To see if fruit games still lead |
| 6 | Michael Gottlieb / Lena Zhukova | Draw up the list of 6–12 Class 3 games for the Colombia NOVA release | TBD | Normal | After Martha's answers |

## Open Questions

- Class A max bet: Val says up to $2.50 is enough; Michael's 25-cent steps were agreed, but the top bet was not set.
- VDEC on the Class A cabinet: Michael would drop it; Val mentioned one slam button. Not decided.
- How exactly to build fixed-value party time wins in the math (Efim).
- Mix of game families for Colombia (Lines & Waves, Jackpot Rush, Fiery Ice) — Val deferred to Michael and Lena.

## Dispatch Log

---
*Processed from Teams transcript on 2026-10-31 11:45 ET*
*Source meeting: Game_Development*
