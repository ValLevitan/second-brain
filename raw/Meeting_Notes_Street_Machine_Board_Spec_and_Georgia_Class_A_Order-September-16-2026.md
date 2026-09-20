# Meeting Summary — Alignment call-September-16-2026
**Date:** September 16, 2026, 12:30–13:00 PM Eastern (recording 12:35–13:41)
**Duration:** ~1 hour 6 minutes
**Attendees:** Val Levitan, Genadi Peari, Pavel Frolov
**Raw transcript:** [[Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026]]
**Source meeting:** Alignment call-September-16-2026 — Microsoft Teams

*Spoken in Russian. Teams transcription mangles most English technical words (board names, part names, place names come back transliterated). Where a term was unclear it is marked below.*

## Summary

The regular alignment call with Genadi and Pavel. It began with short status updates, then Val reported what he is hearing in the market, and the rest of the hour was a working session on the cheap "street machine" — what its electronics must contain and what the cabinet should look like.

**Genadi's status.** He is releasing the plastics for Georgia — quoting and ordering now. He is working on the monitor scanner update, moving the scanner to a different place. He needs a quotation and then will release it. The day after tomorrow he moves to the TITO printer. Next week he switches to the street machine.

**Pavel on AI game conversion.** Two experiments are running. First: take a horizontal game, describe in words what the video is doing, then test whether a background video can be generated from that description. Pavel expects something to come of it. Second: take an existing vertical game with a vertical layout — for Georgia, say — and build a different game with different maths for a different market, such as Texas, under the same layout. If both work, converting games becomes fast. Val pressed on what "fast" means: days, not weeks. Pavel would not commit until the first game is finished and its bugs are closed, but said one thing is certain — the long stretch of the pipeline that used to go on developing and tidying graphic assets will definitely shrink. (The tool Val names for this comes through the transcript as "склад код" / "склодам"; in context it is Claude Code.)

**Val's travel.** He is in Texas on the 2nd, in Nebraska on the 5th, 6th and 7th, and back in Georgia on the 12th.

**What Val is hearing in the market.** In Texas it looks like JVL can place machines with its own port and its own recycler. In Georgia it looks like JVL can place Class A games — today Georgia work is Class B, which is the skill product. Val explained Class A: these are limited machines that were written into the law twenty years ago and nobody paid attention to them, because the maximum pay per spin was $50. One company then found an interesting way around the law — the machine still pays a maximum of $50 per spin, but when a spin starts it runs multiple spins one after another, each paying $50.

He brought Michael Gottlieb in with him on Monday evening; Michael spent yesterday driving every location, taking photographs and video, having gone over it with Efim beforehand. Today Val met the number-one company in Georgia (Lucky Bucks, which has renamed itself) and they gave him an order for Class A machines. That company alone puts out about five machines a week, and Val expects them to take about two a week from JVL. Once they start, the others follow. The same machines go to Texas — what JVL calls street machines.

**What a street machine is.** A very simple machine at around $1,000. It runs on the RK3576. It carries a bill validator as usual, and JVL's own FlexPort. Val doubts they will use a validator at all, but if they do it will be backlit; a peripheral printer should be fitted anyway just in case. Two SAS ports. The panel should be smaller than the current 21" and will mostly be buttons — Val thinks around eight, to be confirmed with Michael once the design is finished.

**Electronics must move to eye level — this came from the technicians, not from Val.** Val wants the electronics taken out of the box and mounted behind the monitor, fixed to the back of the TV inside a metal box on screws, so that a person standing at their own height does not have to sit down or crawl anywhere. Genadi pushed back hard — "you are saying a great deal about how to do it, I think that is wrong." Val answered that he is speaking for the record so it can be written up and voted on, and that he is not dictating the method.

Val then gave the reason. He has a recording of technicians swearing about the machines and refusing to buy them. They will not hang a TV: the women working there cannot lift it, and it takes two people to change one. They will not work with a board that needs a flashlight, bending down, and pushing connectors into a narrow gap sideways. They want the TV to open with the board in front of them, plenty of room, no flashlight. Val offered to send Genadi the recording or take him to meet the technicians himself. Genadi said he believed him, and that he was hearing this for the first time — if the conversation had started from what the technicians are asking for, he would have understood.

**Monitor opens like a cupboard door.** Val wants it hinged like a kitchen door, not lifted — lifting is very awkward. It must not open more than 90 degrees, and the hinge must hold the weight, like a car door. Genadi objected that machines could then not be installed side by side; Val said casino machines are not pushed right up against each other, there is a distance. Genadi then said perimeter lighting would be impossible; Val said the lighting runs around the monitor, which is the only place it is needed. No separate podium, no base, and no need to convert from two screens to horizontal.

**Cutting cost out of the boards.** Pavel and Genadi worked through what can come off. Low-power mode — monitoring the doors while the machine is off — is probably not needed on a street machine. The real money is the ferromagnetic memory: six 256 banks, currently used to store per-game statistics (the last ten games played and the last fifty free spins for each of six games). If that requirement is dropped, one 256 chip is enough and the statistics move out to an SD card or to the eMMC, accepting that they may not always be written correctly. Genadi's point was blunt: they pay around $600 a board today, and a $60–70 I/O board cannot sit inside a $1,000 machine. Val agreed on the proportions but noted memory prices will fall back to the old level in two or three years.

On low-power mode Val first said it is absolutely not needed, then reversed himself: JVL already has it, it costs little, the routines are written and tested, and no time has to be spent on it. Whether they will ever use it, he does not know. The compromise Genadi proposed and Val accepted is to lay the components into the design but not populate them.

**What the new I/O board must carry.** USB hub, two SAS, one printer port, one bill acceptor port, and support for whatever lights are specified. The bill acceptor must be ID003 and ccTalk — pulse cannot be used in gaming, so that is settled without asking. The board sits at the front of the machine with all the connections reachable. The amplifier can be dropped and the TV's own used; there are no serious audio requirements and no subwoofers. Val was firm that a cell modem and WiFi are both mandatory. Electromechanical counters: no. That lands on two electronic boards — the I/O board and a button/counter board for the buttons and basic lighting. Pavel agreed.

**Machine identity.** Today the "passport" is an encrypted piece of memory tied permanently to the cabinet, which is how the cabinet ID is determined. Pavel proposed dropping that and identifying the machine by the processor board instead. Genadi preferred JVL's own I/O board, as the more reliable part — JVL does not change its own board, but might change processor-board suppliers. Val approved removing the passport construction and binding identity to the I/O board. The procedure for what happens when a board is replaced was raised by Genadi and not answered.

**Certification and tampers.** Val confirmed street machines do not need to go through GLI. With no enclosure boxes there is then no need for tampers; only door monitoring, setup and audit. Val partly walked this back later — he had said no box because he thought there would be no certification, but Nebraska may change that, and he does not remember what was done there. Genadi recalled that the lab (heard as "clips" in the transcript) always wanted a local box for the electronics and did not want tampers. Val's conclusion was to contact them and ask what the Nebraska parameters are.

**Board mounting — unresolved.** Pavel wants the board fixed to the back of the TV so the LVDS is connected once and never moves, because LVDS will die after about ten openings. Genadi does not see the logic in separating the motherboard from the I/O board and thinks both should sit together, with a single cable to the monitor. Pavel suggested keeping the perimeter fixed and hinging only the centre section with the touchscreen; Genadi declined to comment on it and asked what problem it solves and what it costs. HDMI versus LVDS for the main monitor was also raised and left open, with Genadi warning that technicians will swear at any connector they cannot orient by feel.

**Cabinet look.** Genadi wants to start the visual design next week and asked for a reference picture. Val has none — there is no competition, which is exactly why he is in a hurry. What he described: a vertical TV at the current tilt angle but thinner, a smaller panel, cup holders for drinks (mandatory), and possibly a small elongated video camera. Body in plywood with sanded boards, and a plastic finish on the monitor. Genadi read it back as essentially today's 43" machine with a small camera and a cup holder, a reduced panel, a monolithic door and a shallow cabinet — the same thing, only simpler. On lighting Val wants light around the monitor without question; a halo light from behind the monitor works well and would let the perimeter light be dropped, but the whole lighting scheme still needs review against how much expense it justifies.

**Other items.** Val told Pavel to extend the development environment — a new SDK is needed for the new board. Val told Genadi to release the IQ moulds and tooling; Genadi will do it today or tomorrow. On the recess on the underside where a sticker sits, Val does not want it left ugly and would prefer a separate plastic piece rather than a sticker, though nothing was settled and it does not affect the tooling. Finally, shipping to Belarus: it goes through third countries — Turkey, China, Uzbekistan or Kazakhstan. Poland is a bad option because of sanctions. Nobody in Uzbekistan is known who could organise the parcel, and the question was left open.

## Decisions Made

- **JVL takes the Georgia Class A order.** The number-one Georgia operator (Lucky Bucks, renamed) placed an order; they put out about five machines a week and Val expects to supply them about two a week. The same machines serve Texas as street machines. (Val Levitan)
- **Street machines do not go through GLI certification.** Asked directly by Pavel, answered directly by Val. (Val Levitan)
- **The street machine carries two electronic boards: a new I/O board and a button/counter board.** The I/O board takes a USB hub, two SAS, one printer port, one bill-acceptor port and support for the specified lighting. (Genadi Peari, Pavel Frolov, confirmed by Val Levitan)
- **Bill acceptor is ID003 and ccTalk. Pulse is not used.** Pulse is not permitted in gaming, so it was ruled out without further discussion. (Genadi Peari)
- **No electromechanical counters.** (Val Levitan)
- **Cell modem and WiFi are both mandatory.** (Val Levitan)
- **The audio amplifier is dropped; the TV's own amplifier is used.** No serious audio requirement, no subwoofers. (Genadi Peari, agreed by Val Levitan)
- **Low-power mode stays in the design as unpopulated components.** Val first said it was not needed, then kept it because it already exists, costs little and is tested; Genadi's "lay in but do not populate" was accepted. (Genadi Peari, Val Levitan)
- **Machine identity moves off the cabinet passport and onto JVL's own I/O board.** The encrypted passport tied to the cabinet is removed. Genadi's argument won over Pavel's processor-board proposal: JVL controls its own board, but may change processor suppliers. (Val Levitan, Genadi Peari, Pavel Frolov)
- **The electronics mount behind the monitor at eye level, in a metal box on screws; the monitor opens sideways like a cupboard door, no more than 90 degrees.** Driven by technician complaints, not preference. No separate podium, no base, no two-screen-to-horizontal conversion. (Val Levitan)
- **Lighting runs around the monitor.** A halo light from behind the monitor is the preferred approach and would replace perimeter lighting; the scheme still needs a cost review. (Val Levitan)
- **Release the IQ moulds and tooling.** (Val Levitan)

Considered and not adopted: identifying the machine by the RK3576 processor board (replaced by the I/O board); keeping six FRAM banks for full per-game statistics (reduced to one, with statistics moved out); hinging only the centre touchscreen section while leaving the perimeter fixed (raised by Pavel, not taken up).

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi Peari | Release the IQ moulds and tooling | Sep 16–17 | High | Val said release; Genadi said he would do it today or tomorrow |
| 2 | Genadi Peari | Get the quotation for the Georgia plastics and release them | This week | High | Quoting and ordering already under way |
| 3 | Genadi Peari | Finish the monitor scanner update — scanner moved to a different position | This week | Normal | Needs a quotation before release |
| 4 | Genadi Peari | Move to the TITO printer | Sep 18 | Normal | "Day after tomorrow" in his own plan |
| 5 | Genadi Peari | Start work on the street machine — electronics requirements now settled, then the visual design | Week of Sep 21 | High | He asked Val for a reference picture; none exists |
| 6 | Genadi Peari | Design the new I/O board — USB hub, 2 SAS, printer port, bill-acceptor port (ID003 + ccTalk), lighting support, front-mounted connectors | TBD | High | Plus the separate button/counter board |
| 7 | Pavel Frolov | Finish the first AI-converted game and close its bugs, then confirm how fast conversion really is | TBD | High | Val wants the answer in days, not weeks |
| 8 | Pavel Frolov | Test whether a background video can be generated from a written description of a horizontal game | In progress | Normal | Experiment 1 of 2 |
| 9 | Pavel Frolov | Test rebuilding a different game with different maths for a different market under an existing vertical layout | In progress | Normal | Experiment 2 of 2 — Georgia layout, Texas maths |
| 10 | Pavel Frolov | Extend the development environment and build a new SDK for the new board | TBD | High | Val instructed it directly |
| 11 | Pavel Frolov | Confirm what must still be written to FRAM once per-game statistics move out, and size the single chip accordingly | TBD | Normal | Says "need to look at the requirements" |
| 12 | Val Levitan | Confirm the button count on the panel with Michael Gottlieb once the design is finished | TBD | Normal | Val's estimate is around eight |
| 13 | [Needs Val's confirmation] | Contact the Nebraska lab and ask what the certification parameters are — electronics box and tampers | TBD | Normal | Val said "it is probably worth contacting them and asking"; no owner was named aloud |

## Open Questions

- What happens when the I/O board is replaced, now that machine identity is bound to it? Genadi asked for the board-change procedure; nobody answered.
- HDMI or LVDS for the main monitor. Raised, not settled. Pavel warns LVDS dies after about ten openings unless the board is fixed to the TV and never moves.
- Where the I/O board and motherboard physically sit. Pavel wants the board on the back of the TV to protect the LVDS; Genadi wants both boards together next to each other. Unresolved.
- Nebraska: Val does not remember what was done there and does not know the parameters. The lab has historically wanted a local box for the electronics, which would undo the "no box, no tampers" decision.
- Whether the full lighting scheme (halo plus perimeter) is worth the expense — needs review.
- How to ship to Belarus. Turkey, China, Uzbekistan or Kazakhstan are the routes; Poland is ruled out by sanctions. Nobody is known in Uzbekistan who could organise the parcel.
- What to do with the recess on the underside — sticker, separate plastic piece, or a scan symbol. Does not affect tooling, so it was left open.

## Dispatch Log

---
*Processed from Teams transcript on September 16, 2026*
*Source meeting: Alignment call-September-16-2026*
