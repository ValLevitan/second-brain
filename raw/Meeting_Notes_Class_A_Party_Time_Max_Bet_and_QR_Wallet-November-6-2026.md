# Meeting Summary — Game_Development
**Date:** November 6, 2026, 2:04 PM – 3:08 PM Eastern
**Duration:** ~64 minutes
**Attendees:** Val Levitan (host), Michael Gottlieb, Efim Podvoiski, Lena Zhukova
**Raw transcript:** [[Meeting_Transcript_Class_A_Party_Time_Max_Bet_and_QR_Wallet-November-6-2026]]
**Related:** [[Georgia_Class_A_COAM_rules_Claude_reading_UNVERIFIED-November-6-2026]] — Val's Class A notes from this meeting (same GLC card, $50 max win, multiple pays of $50)

## Summary

**Georgia Class A game — party time.** Michael said wins are capped at $50. The team will keep normal casino math and add a "party time" feature (the competitor Primero calls it "winning streak"). Party time does two jobs: it gives the player more than $50 when needed, and it works like a small mystery progressive. First target: 12% of RTP goes to party time; it hits about 1 in 240, half as often as free spins (1 in 120). After free spins that hit the $50 cap, the next base spin goes into party time without telling the player. The $50 cap covers the whole free-spin round, not each spin. Efim said the cap matters only for bets above $1.

**Free spins stay.** Val asked why keep free spins if they eat payout, and suggested more party time instead. Michael explained: free spins give money back slowly, give two to three minutes of time on device and entertainment, and a game needs at least two things to chase. Primero failed because its free spins rarely happened and were capped. Val accepted the argument ("Solid argument, clever").

**Max bet.** Michael wanted $5. Val wanted no more than $3: high bets only show the $50 cap on every top pay, Georgia's average bet is about $1.20, and a limited-bet machine looks better to the regulator and is a simpler story for operators. Michael agreed. Bets go in 25-cent steps, so $3 means less math work for Efim. Val: if competitors go higher and the market asks, JVL can add higher bets later.

**Other game settings.** Total RTP about 92%, same as Georgia. No progressive — the $50 cap rules it out; party time replaces it. Vertical cabinet. The base is the Georgia COAM game. Skill element: pick the larger of two coins (left or right is random). Michael believes Class A needs skill, based on the Class A summary Val sent on August 31 ("Claude's interpretation", marked do not rely on it); he showed it on screen near the end. Val asked where the skill rule comes from.

**Schedule.** Concept art is approved. Production starts in January after Nebraska, on NOVA (new workflow).

**QR e-wallet flow instead of bill acceptor and printer.** Val wants two optical readers on the machine: the left one (where a printer sits) cashes out awards onto the paper ticket; the right one (where the bill acceptor sits) adds credits from the ticket. The player buys the ticket at a kiosk ($20 in, $20 QR ticket). Software must support both setups, chosen in the setup menu: bill acceptor + printer, or two QR scanners. Screen text agreed: "Scan to redeem awards" (left, arrow) and "Scan to add credits" (right, arrow), with a QR-scan picture. Val's goal is to launch with scanners; the printer setup is the fallback if the market rejects scanners. Efim asked about putting only part of a ticket into credits; Val said this exists today but slows the transaction.

**Nebraska and catalog.** Wildfire Ranch is up and playing; art and math under review. Efim's idea: a big horse animation when three reels fill with horses. Val said the snow under the horse looks off (too pink) and the hoof should sink into snow; Lena said the art is not final and colour will be corrected once all screens run together. Royal symbols stay flat and desaturated on purpose. Midnight Money got a mild update pass.

## Decisions Made

- **Class A max bet is $3** (25-cent steps) — fits a limited-bet machine story and the ~$1.20 Georgia average bet; raise later if the market asks. (Decided by Val, agreed by Michael)
- **Keep free spins and add party time** — free spins give time on device; party time pays past the $50 cap. First target 12% RTP, ~1 in 240. (Michael; accepted by Val)
- **Total RTP about 92%.** (Val; Michael agreed)
- **No progressive on the Class A game** — the $50 cap rules it out. (Michael)
- **Software supports two cash setups** in the setup menu: bill acceptor + printer, or two QR scanners with "Scan to redeem awards" / "Scan to add credits". (Val and Michael)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Michael Gottlieb | Forward Val the Class A material that refers to skill | After the meeting | Normal | Val asked where the skill rule comes from |
| 2 | Lena Zhukova | Design the new screen for the scanner setup: "Scan to redeem awards" and "Scan to add credits" with arrows and a QR-scan picture; supporting graphics for the V-deck | TBD | Normal | Michael asked Lena for the new screen |
| 3 | Michael Gottlieb, Efim Podvoiski | Tune party time hit frequency and EV against free spins | TBD | Normal | "That's going to take Efim and I some period of time" |
| 4 | Efim Podvoiski | Tell the programmers about the big horse animation in Wildfire Ranch | TBD | Normal | Lena told artists already; Efim had not told programmers |
| 5 | Lena, Efim, Michael | Start Class A game production on NOVA after Nebraska | January 2027 | Normal | Concept art already approved |

## Open Questions

- **Does Georgia law require a skill element in Class A?** Raised by Val. The team's belief rests on the unverified Claude summary. See [[Georgia_Class_A_COAM_rules_Claude_reading_UNVERIFIED-November-6-2026]].
- **Will the first Class A machines ship with QR scanners or with printer + bill acceptor?** Michael asked; Val's goal is scanners. Not settled.
- **What wording and programmer behaviour does the scanner flow need?** Michael: the programmers must define it.

## Dispatch Log

---
*Processed from Teams transcript on November 6, 2026*
*Source meeting: Game_Development*
