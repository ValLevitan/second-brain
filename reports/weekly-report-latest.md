# JVL second brain — weekly update, Saturday November 8 2026

This week's update completed. Everything checked out.

## What came in

Seventeen meetings from Friday October 30 (afternoon) to Saturday November 7. One late Oct-30 recording, five Minsk stand-ups, two Felipe sales calls, and nine planning or design meetings. One Teams chat capture (the IO-board repair chat) was set aside as out of scope, as the rules say.

Note on the run itself: the Saturday-morning run stopped partway after writing its first meeting. The evening run found that work intact, kept it, and finished the week. Nothing was lost or redone.

## What the brain learned

- **Class A (Georgia).** On Oct 30 party time moved off a flat $50: wins now scale with the bet, the paytable is never capped, and bets move in 25-cent steps on screen. On Nov 6 the numbers were set: max bet $3, free spins stay, party time takes 12% of the return at about 1 in 240, total return about 92%, no progressive. The software will support either a bill acceptor and printer, or two QR scanners with the kiosk ticket as the wallet. Production on NOVA starts in January after Nebraska.
- **Georgia V4 and Colombia.** You confirmed another Georgia software release with "perceived persistence" games. Colombia gets 6 to 12 Class 3 games on NOVA, made from the updated Georgia games, before the contracts expire in December 2027. Market questions go to Martha as structured lists.
- **What "done" means.** On Nov 4 you ruled that a release is done only when the cleaned build sits on the production server under a number. Ivan is release manager, reporting to Irina. Claude writes the release notes and an exception report. "Request Review" leaves the feature workflow. You also forced the Flex-Port build download into MVP 1: "if the client cannot take it, it does not exist."
- **MVP 2 cut down.** On Nov 5 MVP 2 was narrowed to Wi-Fi, remote Flex-Port update, robust installation and install diagnostics, due November 20. MVP 3 is aimed at about January 20. MVP 1 is planned for Monday November 9 internally, with the client told Wednesday.
- **Georgia tilt bug.** The Intralot block was a false handpay caused by the Collect button on tilt dialogs. Your rule: "a tilt is a tilt" — during a tilt the machine does nothing else, on every machine. The fix ships free with the RIS improvements, to Eclipse on November 16.
- **Modems.** The modem stays always on. An operator who refuses it can switch it off only through a deliberate QR-scan and activation-code routine. Scope is about three days of work.
- **NOVA 2.** Rage is finished. NOVA 2 is Anton's Rust engine with Lua-scripted games and a studio with a built-in agent. The team agreed to work agile, code first. All work moves into corporate repositories under Bosik. The sound library is being rewritten in Rust.
- **Remote update and registration.** Every software component is signed separately, with one server signature at update time. Registration and RIS move into Cloud Galaxy. At the Saturday session only two things were decided: at manufacture only the base must come up, and there is no jurisdiction check at registration. The one-scan serial scheme and the Dallas-chip replacement are still open, and you took the transcript to think.
- **Sales.** You set a rule of thumb for software upgrades: about $500 a game, $7,500 for a 15-game library, about $1,500 for a premium game. Felipe does not quote trade-in prices; you are in the middle of every trade-in deal. Ray's 5-plus-5 D27 order goes to Nebraska.
- **New person.** Daniil Stauskiy, the Minsk developer rewriting the sound library, now has his own page.

## Held for you

- Someone said "we lost our product owner, nobody can replace him" at the Nov 6 remote-update review. The transcript gives no name; the notes say Juan. The brain recorded it as a guess only. Who, and when?
- Your Nov 6 "code first" agreement narrows the Oct 29 order to describe the engine fully before code. The brain annotated the old decision rather than closing it. Confirm or close it.
- You told Klimovich "since yesterday you are already ours". Whether his status changed formally is not in any source.
- The Nov 1 release date has slipped (you said 40 days late on Nov 4) and no new date replaced it. The plan of record stays, with the actual beside it.
- Several names are recorded as guesses: Slava (modem document), Artur (Nebraska updates), the Georgia SIM location, two unresolved Andreis, and the Pyramid acceptor owner (Alekseev or Khamin).

Personal passages in five transcripts were cut at intake and are not in the brain. No pay or compensation was recorded.

## Health

Everything checked out. 172 facts were checked by hand against the recordings and all 172 held. Twelve older facts were re-checked and all hold. The catalog is exact, no broken links, no orphan pages. One housekeeping fix: 95 catalog lines had fallen behind their pages' source counts and were refreshed.
