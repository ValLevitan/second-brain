# Meeting Summary — Intralot and JVL meeting
**Date:** October 13, 2026, 9:54 AM – 11:45 AM Eastern
**Duration:** ~1 hour 51 minutes
**Location:** Intralot, 11360 Technology Circle, Duluth GA
**Attendees:** Val Levitan, Felipe Miranda Giorgi (JVL). Intralot: Bill (Bill Avgeris), Chris (Christos Tzoumaras), plus others not named in the recording. Georgia Lottery: a man addressed as "Chris", most likely Chris Boncek (see Notes on the transcript).
Source: Plaud recording (offline), via Plaud-Inbox/JVL-Customer-Visits
**Raw transcript:** [[Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026]]
**Visit note:** [[2026-10-13 Intralot]]
**Calendar:** paired to Outlook event "Intralot and JVL meeting", Oct 13 10:00–11:00 ET (Intralot and Felipe both named in the transcript).

## Summary

Val's first face-to-face meeting at Intralot, the Georgia central system operator. Breakfast was brought. The meeting had two parts. In the first part a Georgia Lottery representative was in the room. In the second part he had left, and Chris (Intralot) spoke about Intralot's plans for the route business.

**Part 1 — JVL machines going out of service.** Val's main issue: JVL machines sometimes lock and sit out of service, and JVL does not know about it. Felipe explained the field pain. A technician finds the machine locked. The call center tells him it is the wrong software. He does a hard reset or a decommission and recommission. But the software never changed, and simply setting the machine from locked to operational in the menu works. Felipe said masters and technicians have learned to live with it, so most cases are never reported to JVL. An Intralot technical person said an earlier investigation found the machine takes too long to answer a signature request from the site controller, and that times it out. Val asked how the same commissioned game can send a different signature.

Val explained why this matters. JVL sales dropped from about 600–700 machines a year to almost zero. JVL kept releasing new games because it thought the games did not earn. Val now believes the software is good and the problem is technical: machines are "technically out of service". He also said JVL RTP is too high (about 95% against competitors' 90–92%) and will be adjusted. He said he is not blaming anyone; he wants to find JVL's own edge-case problems (timing, negative cases), which GLI and Eclipse lab tests do not cover.

Bill said Intralot sees only two or three JVL machines disabled at a time, which looks like normal operations. Val asked whether that is because Intralot does not see the lockout signal; Bill said they do not see the lockout. Felipe said everything started after Intralot introduced the new site controller, about three years ago.

**Million-dollar payout spikes.** Bill explained that these come from technicians RAM-clearing a machine without calling Intralot. The system reads it as a meter rollover. The amount stays pending, is not counted in any average or in what operators pay, and is corrected with lottery authorization in about two to three days. Val said he did not know this. The Lottery representative said calling in the meters before a hard reset makes the correction easier.

**Testing access.** Val asked for a test setup like the one JVL has in South Dakota, where the lottery gave JVL a Light & Wonder controller. Bill said only the certification labs and the lottery have access to the test environment, so it is a lottery decision. The Lottery representative said the site controller is proprietary and has never been loaned to a manufacturer, but he would take the request. He advised Val to put two options in one letter: (1) a site controller in JVL's possession, and (2) testing at Intralot's lab. He said they likely have more appetite for testing in house. He also noted the prototype JVL loaned to the lab is the old tabletop and an upgraded unit would help.

Then Bill proposed not to wait for the lottery: Intralot has ten ports, so JVL brings ten machines and testing starts now. The Lottery representative agreed to move ahead. Intralot will also scan the whole field for JVL machines.

**Transactional equipment.** Val described Flex-IQ (POS), the kiosk and Flexport. The answer: this is outside the game, Intralot has nothing to do with it, and nothing needs to be tested there. Val said JVL is not offering the recycler; the Lottery representative said that is a relief to many. He expects gift-card cash access to be a hot topic in the legislature in the spring, and HB 353 may be fine-tuned. Today digital gift cards are acceptable, but rules may stop them becoming a path to cash. Enforcement: by law a non-compliant location first gets a warning, then a violation. There is no reporting requirement on JVL's transactional system.

**Promo credits.** Val asked about promo credits over SAS. The Lottery representative said promo meters are not part of the current Georgia requirements (version 1.8). Turning them on would need a requirements update and a wider legal discussion on inducements, because the money would come from a manufacturer to a player. He suggested legal representatives and probably Joe Kim. For the legislative side he named HB 353, the Regulated Industries committees, and Representative Alan Powell, who is involved with the GACS show (the transcript says "GAX"); Felipe said JVL is signed up for that show on the 22nd.

**Part 2 — Intralot's route plans (Chris).** Chris said Intralot's position in Georgia is delicate: its only customer here is the Georgia Lottery. He described the group: Soo Kim (chairman of Bally's) bought about 60% of Intralot from Kokkalis. Intralot acquired Bally's Interactive (iGaming) and is buying a sports-betting group (William Hill, 888, Mr Green) by year end. The missing piece is the route business. Targets he named:
- **Nebraska:** about 30 operators; Intralot runs the lottery system. Idea: the lottery as route operator with lottery-branded machines in lottery locations (maybe 500 of about 2,000). The lottery and the tax commissioner liked it. He expects something in 2027.
- **Ohio:** if it is regulated early 2027 (they expect Class B type, possibly like Illinois), partner with a large Class A / jukebox operator with about 1,300 locations.
- **Wyoming:** the lottery has about 500 locations; target 200. He is a close friend of the lottery director.
- **Idaho:** a legal pull-tab "lottery machine" on Intralot's system.
- Also Arkansas, Puerto Rico and the Dominican Republic.

He wants a route partner and a machine supplier. Options are open: revenue share, cap, or Intralot taking equity in the manufacturer. He said clearly that nothing is signed; it is conceptual and his board wants a 2027 plan. He wants a "full solution" for lotteries: Intralot, JVL as game maker, and a repair depot — Renova, an Atlanta shop that repairs Aristocrat bill acceptors (Luigi, son of the owner).

Val said JVL wants the same thing. JVL has a family office with cash ready (he said the 2026 tax law allows a 100% write-off). JVL is building a budget street machine: no bill acceptor, no printer, one player screen, with a modem for software download. JVL has a Nebraska licence and machines but they are not earning yet. Val said he would happily join Intralot in meetings with lotteries, and that Wyoming interests him most.

**Social.** Dinner was moved to tonight (October 13): drinks at 5:45 PM, table at 6:30 PM at Frankie's, with Luigi (Renova) joining. Val invited the group to a basketball box at State Farm Arena on Monday November 9 at 6 PM, and asked for head counts early.

## Decisions Made

- **JVL will place ten machines in Intralot's lab (ten ports) and testing starts now, without waiting for the Lottery's formal answer.** Mixed vertical and horizontal, not all new, different software, maybe one Altera. (Bill proposed; Lottery representative agreed; Val agreed)
- **Val's formal letter will ask for two options together: a site controller in JVL's possession (loan or purchase), and testing at Intralot's lab.** (Val, on the Lottery representative's advice)
- **Intralot engineers will scan the whole field for JVL machine lockouts.** (Bill)
- **JVL transactional equipment (Flex-IQ, kiosk, Flexport) does not need testing at Intralot.** (Lottery representative / Intralot)
- **JVL is not offering the recycler.** (Val)
- **JVL RTP (about 95%) will be adjusted down toward competitors.** (Val)
- **Val will join Intralot in meetings with lotteries on the route idea, in principle.** (Val; nothing signed)
- **Dinner moved to tonight, Oct 13, 6:30 PM at Frankie's, drinks at 5:45 PM.** (Chris and Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Bill (Intralot) | Investigate the lockout case and get back to JVL | Fri Oct 16 | High | "We will get back to you by Friday" |
| 2 | Intralot engineers | Scan the whole field for JVL machines that lock or disable | TBD | High | To settle "many vs few" |
| 3 | Val Levitan | Send the formal letter with the two options (site controller / Intralot lab testing) | TBD | High | Ask for an exception |
| 4 | Val Levitan / JVL | Ship ten machines to Intralot's lab | TBD | High | Fill the ten ports |
| 5 | Felipe Miranda Giorgi | Forward the email that documents the unlock steps, so the call center can be taught | TBD | Normal | Who asked is unclear in the recording |
| 6 | Lottery representative ("Chris") | Take the site-controller request to the Lottery for discussion | After letter | Normal | Historically never done |
| 7 | Chris (Lottery) and Chris (Intralot) | Tell Val head counts for the Nov 9 basketball box | Soon | Low | Val needs to set tickets aside |

## Open Questions

- Why do JVL machines lock: a site-controller signal, a timing issue, or the machine itself? Nobody knows yet. (Val)
- JVL says many cases; Intralot sees two or three. Is it that Intralot does not see the lockout signal? (Val, Bill)
- Did the lockouts start with Intralot's new site controller about three years ago? (Felipe)
- Will the Lottery loan or sell JVL a site controller? (Lottery representative)
- Can promo credits be allowed in Georgia, and who rules on it — legal, Joe Kim, the legislature? (Val)
- Intralot route partnership: which states, revenue share or equity, and when. Nothing is signed. (Chris)

## Notes on the transcript

- Plaud speaker labels: Speaker 3 is Val; Speaker 2 is Felipe; Speaker 1 is Bill (Val calls him Bill). Speaker 4 is the Intralot executive Val has dinner with ("Chris") — taken to be Christos Tzoumaras. Speaker 5 speaks for the Lottery ("we have to give them a warning by law", "known to GLC") and is addressed as "Chris"; he leaves before Part 2 ("the bad guy is gone"). He is most likely Chris Boncek (GLC), who was Cc'd on the invitation — **needs Val to confirm.** Speakers 6 and 7 are not named.
- Glossary: 1 fix applied (JBL → JVL).
- Possible mis-transcriptions, not fixed: "income" ×6 meaning InComm (scoped rule, needs Val's call); "intraday" / "intra lot" → Intralot; "set controller" / "side controller" → site controller; "Fred Lipa" → Felipe?; "Mr. Levitin" → Levitan; "Xavier machines"; "SaaS" → SAS; "Chromo" → promo; "Keyos" → kiosk; "Altera"; "Arca" / "Ark" → ARC?; "Banti" / "Bandy" / "Pante" → Bunty (United)?; "Gazelman" → Gauselmann?; "Evolve" → Evoke?; "Shukin" / "Sukim" → Soo Kim; "Jamie Patel" (ex-IGT CEO); "John Claunch" (Wyoming lottery director); "GAX" → GACS?; "noy" → Illinois?; one line at 01:17:28 is in Hindi script.

## Dispatch Log

---
*Processed from Plaud recording on October 14, 2026*
*Source meeting: 10-13 Technical Troubleshooting and Multi-Jurisdictional Route Expansion Strategy Meeting*
