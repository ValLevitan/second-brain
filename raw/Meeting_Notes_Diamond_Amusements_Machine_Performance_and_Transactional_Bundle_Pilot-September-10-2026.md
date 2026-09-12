# Meeting Summary — Meeting with JVL — Diamond Amusements, Conyers GA

**Date:** September 10, 2026, 12:29 PM – 2:28 PM Eastern
**Duration:** approximately 1 hour 59 minutes
**Location:** Diamond Amusements, 2069 Lake Industrial Ct, Conyers, GA 30013
**Attendees:** Val Levitan (JVL). From Diamond Amusements — Shawn Fellows, plus warehouse and service staff; the invitation listed Terri Spivey, Terra Horton and Igor Fernandez, and the transcript refers to "Tara and Igor... warehouse and service guys" and to "Terry". Felipe Miranda Giorgi was on the JVL invitation but is spoken about in the third person throughout, so he was not in the room. Plaud's speaker labels split the Diamond side inconsistently and are not reliable evidence of who said what.
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL-Customer-Visits
**Raw transcript:** [[Meeting_Transcript_Diamond_Amusements_Machine_Performance_and_Transactional_Bundle_Pilot-September-10-2026]]
**Visit note:** [[2026-09-10 Diamond Amusements]]

## Summary

A long working visit at Diamond's warehouse, straight after Val's morning meeting at the Georgia Lottery. It ran in three parts: Diamond's service technicians laid out everything wrong with JVL machines, the two sides went through per-location performance data together, and Val put two commercial offers on the table. It ended with a small, concrete order and three follow-up meetings.

### Service complaints — the first half hour

Diamond's technicians were direct and specific:

- **The logic box is at the top of the cabinet.** Aristocrat and Light & Wonder put theirs at the bottom. Techs want it at eye level, above the bill acceptor.
- **Monitors are hard to remount** — not so much heavy as badly designed for reassembly. One tech, who describes himself as tech-savvy, had to get a JVL technician to come and put one back on.
- **Settings cannot be restored locally.** On any other manufacturer's game a tech re-enters settings by hand. On a JVL they wait for Felipe to send the settings and a passcode key — sometimes all day — then download the settings to a thumb drive and carry them out.
- **"Peripheral not detected" does not say which peripheral.** Other manufacturers name the failing part. On a JVL the machine comes back to the shop to find out.
- **Error 704** is a meaningless tilt code. "Who the hell knows what 704 is? Nobody does" — Val's own words.
- **Machines run hot.** The advice to turn on the fan inside the logic box did not fix it.
- **Field software updates fail** if a peripheral is not picked up, leaving a game down in the field.
- **Every change requires re-commissioning.**
- On Diamond's Intralot sheet, **five JVL machines were down** — more than any other brand. One tech had pulled five games in four weeks.

The technician's summary was blunt: "It's hard for me to get him to even purchase at this point in time because of just issues."

### Val's explanations and what he committed to

Val did not argue with any of it, and explicitly took Felipe out of the firing line: "Felipe is not at fault... the problem is the design."

**Why the settings are locked (the "Passport").** JVL ran a large Latin American operation where brand-new bill acceptors were swapped out for worn ones — new equipment came back within thirty days with validators running at a 60% acceptance rate. JVL's answer was to lock every peripheral change behind a security code. It sits at the centre of the operating system, not off to the side, so it cannot simply be switched off. Val was frank that it solves a problem Diamond does not have: "For you, it's a hassle, it's a nuisance."

**Why the machines were losing money.** The latest AMD processor conflicted with Linux kernel 4.17, and Linux would silently shut the processor down. The machine froze in a state an attendant would not notice and a player would just walk away from, so it read as games that did not earn rather than machines that were off. It took about a year and a half to find, and was only understood after AMD and Linux published a bulletin. The watchdog timer that should have caught it — a ten-cent chip that resets the CPU when the heartbeat stops — had been disconnected in software by JVL developers roughly five years ago, though the chip stayed mounted on the board. Val's account is that JVL responded to the falling numbers by releasing more games, which kept earning less, for a year and a half.

**What Val promised.** Step by step, within about a year, all of the complaints get fixed — but not now, because the whole team is on the new game. Specifically: error 704 and the tilt codes get real codes a tech can enter, delivered by QR; the re-commissioning requirement goes; and the Passport lock disappears on the new internal platform, two years in development, which new games move to from January. He said he would come in personally and show them each change against the old software. He also declined to promise what he cannot do — moving the logic box needs a cabinet redesign, so it is not happening.

**Service relief on 1 October.** Val has hired an engineer from Miami who starts 1 October, an engineer by education who worked for Val in Colombia and knows the machines. He takes service load off Felipe, who is inundated.

### Performance data

Diamond pulled up a per-location ranking of every location holding JVL games — 74 JVL machines deployed. JVL placed sixth at one location, second in August at another, third and fourth elsewhere. Val saw about $19 win per unit per day on one report and said he was "perplexed": his senior VP of game design is ex-Bally and he could not see how JVL games make less money than Light & Wonder or Aristocrat.

Working through it in the room, Val landed on settings rather than game quality:

| | Aristocrat / Light & Wonder | JVL |
|---|---|---|
| Default bet | $1.00 | $0.25 |
| RTP | 90% (options generally 90 or 92) | 92–94%, no lower setting offered |
| Top progressive displayed | $6,000 (some as high as $8,000) | $2,400 |

His argument: a player walking in sees a $12,000 progressive next to a $2,000 one and goes to the big number. Displaying a large progressive means a high reset value, which means lower RTP or higher volatility. So JVL gets played as a "dribbler" or filler while the real money chases the neighbouring machine. At 94% RTP, he said, the machine "doesn't have enough time to hold money" — with only three or four active hours a day, the gap between 90% and 94% is a 40% difference in hold.

Two structural problems came out of this:

- **Georgia is unique in that the operator cannot change JVL settings** — every change goes back to JVL. Diamond sets every other manufacturer's machines per location (at the Bill Ritter location, $5 max bet, jackpots $5,000–$10,000, RTP 90–92) and mixes settings for the different players who come in.
- **Intralot's financial reports are not reliable.** Val says they generate "ridiculous data" — million-dollar payouts — typically where a configuration was changed without re-commissioning. Diamond's numbers come off Intralot. What Val actually needs is popularity and settings data, not financials, and he can get it by QR code on older machines or by modem on the new ones. Diamond already sends a QR code every two weeks for the two new machines.

Diamond agreed their field auditor — who does compliance checks and physically handles every machine anyway — can pull up the menu screen and capture settings data across the JVL fleet. Val: "we're operating blind, so that would be a fantastic help."

Fleet detail: all flex cabinets, no old cabinets left, all dual SAS except the earliest versions, and Diamond has moved a lot of "peach two and three" units over to "peach one" because they perform better. Only two of the new machines are out.

### The two offers

**Offer A — fleet trade-in.** Val asked whether Diamond would trade its entire park for the new vertical-cabinet machine at $15,750, and offered to upgrade the older "419" units with modem and software for free. Shawn declined to move on the fleet: not until there is more data, and "I'm not going to upgrade 74 games." His reason is commercial, not technical — a player has a game they use, the store across the street has the same game, and those stores compete, so how fast a player adopts a new game matters. He will look at a written proposal with pricing and consider incremental upgrades.

**Offer B — transactional bundle tied to a machine sale.** Buy one new machine per location, call it $16,000, and JVL gives that location its entire transactional set free: roughly six AFT ports (one per machine), a POS for the counter, and a self-serve kiosk that takes cash, issues a TITO-like ticket and validates it back to dispense a card. Retail on that set is $15,000. Val was explicit about what he is buying: "I'm basically buying the exclusivity of issuing cards in the location." He is agnostic about the card provider and wants into the card business. Terms he attached: $90 flat per location, excluding card processing; API free, but back-office "operator intelligence" and reporting free for now and chargeable later; and **JVL requires exclusivity in the location — no other transactional equipment.** He suggested Diamond work against it through an MCP with Anthropic or Grok rather than the raw API.

**Where the card-clearance risk landed.** JVL acts as broker and fronts its own money to the clearing house, then sweeps the location by ACH. Val asked what to do if a location does not pay. Shawn said call him first, but was firm that Diamond will not be a reseller and will not stand behind location debt: the merchant relationship sits between JVL, the bank and the location. His reasoning is that Diamond's relationship with its locations is fragile and they will not let an outside financial arrangement collapse it — they turned the same thing down with InComm years ago for the same reason, and "I don't want to lose ten thousand dollars." He did point Val at the real exposure: processing runs over 72 hours, so the risk window is the weekend, which is also the heaviest play. His illustration was $30,000 a week in redemption with $15,000 going back into replay, roughly $15,000 a day, about $45,000 over a long weekend. Val's position if a location does not pay is that he will shut the payment function off — machines keep running but cannot take money or award a winner. Shawn noted Diamond cannot shut machines down under lottery rules and that the Lottery would likely take issue.

Despite declining the financial backstop, Shawn said he would like to try one, and the meeting closed with him committing to two machines in two different types of location.

### The new machine

Submitted to Eclipse on 15 September for approval. Fifteen games, and unusually **three separate progressives on one machine** aimed at three player types: an aggressive high-volatility player, a time-on-device "dribbler", and a chase or link progressive. It is a variation of Mega Hit, the latest version, adding a bison/buffalo game and another lion game. Vertical cabinet rather than dual screen, with an LTE modem.

### Class A, and the lottery meeting reported back

Val relayed his morning meeting: even where a location has an ATM, redeeming the card **in that location** is not allowed, but redeeming it elsewhere is. Shawn summarised it back correctly — "so Justin and Chris said it's okay, just not in the same licensed facility" — and Val confirmed. Nobody at the Lottery told Val the card itself is illegal. Val also mentioned Joe Kim brushed off his meeting request twice.

On Class A, Shawn thinks the "AV games" are problematic, not what was intended, and that players are not migrating — deployment is spotty. Both men have played Primero. Shawn thinks it is a classic-style game without the RTP or prize distribution to hold players. Val disagreed in part: he had a genuinely pleasant experience playing it and was taken aback, the first time he has thought there might be something in Class A. He is not a fan of Primero's designs but respects him as a businessman. Primero has had to take the progressive off. Val told Shawn he asked the Lottery for Class A regulatory guidelines and they had none. Shawn expects the regulator to address it in the next four to six months.

### Background picked up

Diamond leases an 11,000 sq ft building and deliberately does not sit on inventory — flip it or push the sales force. They run traditional Class A boxes too, and a kiosk from American Kiosk that takes a kiosk ticket, issues a gift card and can take the card back so a player returns another day. A Diamond principal has 43 years in the business, having started with his father at 17. Shawn built a company in Atlanta with Larry Simmons and fell out with him around 2000–2001; he worked with Hess Technology out of Texas; he has lived through two states shutting down, South Dakota in 1999–2000 and then Georgia in 2002 when those machines flooded in. Across Georgia's number two and three counties plus South Carolina, Alabama and Texas, that business ran about 9,000 machines. Nothing in South Carolina now. Diamond is implementing a full Oracle enterprise system, currently runs six or seven different software packages, and has deliberately slowed down — only two acquisitions this year — to fix processes before growing again.

Val flew out that evening for the high holidays.

## Decisions Made

- **Diamond will buy two of the new vertical-cabinet machines and deploy them in two different types of location.** Shawn: "definitely let's start with two, we'll buy two and deploy two different types of locations." Val had pushed him down from ten — "don't do ten, do two." Target around 1 October, after the 15 September submission. (Decided by Shawn Fellows and Val)
- **Diamond will not trade in the 74-machine fleet now.** Data first, then a written proposal with pricing, then possibly incremental upgrades. *Considered and superseded:* Val's opening proposal to trade the entire park at once. (Decided by Shawn Fellows)
- **Diamond will not act as reseller or guarantor for card-clearance debt.** The relationship stays arm's length; JVL's exposure sits between JVL, the processor and the location. Shawn will take a call before anything is shut off. (Decided by Shawn Fellows)
- **The technical fixes come over roughly a year, not immediately, and Diamond accepted that.** Diamond: "if I sat here and promised you fix tomorrow, I would be lying. We're not expecting that." (Decided by Val and Diamond)
- **The Passport peripheral lock will be removed on the new platform from January.** Val committed to it on the basis that new games move to the new platform then. (Decided by Val)
- **Follow-up schedule set:** Shawn comes to Val's office Wednesday 16 September, around 3:00 PM, to see the transactional system; Val brings his senior VP of game design to tour Diamond's locations earlier that week, targeting Tuesday; and the three of them go to dinner on the Wednesday. (Decided by Val and Shawn Fellows)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Shawn Fellows | Identify the two locations for the pilot | Before Oct 1, 2026 | High | "Let me identify two locations" |
| 2 | Shawn Fellows | Buy two new vertical-cabinet machines and deploy them in two different location types | ~Oct 1, 2026 | High | The concrete outcome of the meeting |
| 3 | Shawn Fellows | Send Val the performance breakdown per game | TBD | High | "I'll get it and send it to you with the breakdown of each one" |
| 4 | Diamond field auditor | Capture settings / QR data from JVL machines during compliance rounds | Ongoing | High | Val: "we're operating blind, so that would be a fantastic help" |
| 5 | Val Levitan | Submit the new game set to Eclipse for approval | Sep 15, 2026 | High | Whole team mobilised on this |
| 6 | Val Levitan | Confirm his senior VP of game design is travelling, then coordinate the location tour | Sep 11, 2026 | High | "Let me just confirm that he's coming for sure" |
| 7 | Shawn Fellows | Check his team's availability and confirm the location tour day | Sep 11, 2026 | High | "Let's communicate tomorrow" |
| 8 | Val Levitan | Provide a written price and proposal for incremental fleet upgrades | TBD | High | Shawn: "I need to know what you're talking about from a price standpoint" |
| 9 | Val Levitan | Put the new Miami engineer onto Diamond's service load | Oct 1, 2026 | High | Takes work off Felipe |
| 10 | Val Levitan | Upgrade Diamond's older "419" units with the modem and software, free of charge | TBD | Normal | "That's for free" |
| 11 | Val Levitan | Fix error 704 and the tilt codes so a tech can enter a code himself, delivered by QR | Within ~1 year | Normal | "I don't want to call Felipe for every code" |
| 12 | Val Levitan | Remove the re-commissioning requirement after every change | Within ~1 year | Normal | |
| 13 | Val Levitan | Turn off the Passport peripheral lock on the new platform | From January 2027 | Normal | Tied to the new internal platform |
| 14 | Val Levitan | Customise the transactional product screens to Diamond's liking if they proceed | TBD | Low | Offered, conditional on the pilot |

## Open Questions

- **What is the trade-in price for a dual-screen flex cabinet?** Val put it back on Shawn — "you tell me, you write the deal" — and it was not settled.
- **Will Diamond take the transactional bundle?** Shawn said "I'd like to try one," but it was not committed, and it carries JVL's requirement for transactional exclusivity in the location.
- **Why does JVL underperform Aristocrat and Light & Wonder in the same locations?** Val's settings hypothesis — default bet, RTP and progressive display — is reasoned but unproven, and depends on the settings data Diamond agreed to start capturing.
- **What happens when a location fails to pay for cleared cards?** Shawn will take a call but declines any financial backstop, and Diamond cannot shut machines down under lottery rules. Val says he would disable the payment function. Untested.
- **Can Georgia operators be given direct control of machine settings?** Val says they will get it "within a year" on the new platform. Nothing firmer was agreed.
- **Is the new machine price $15,750?** The recording renders it as "fifteen seven, seven fifty," and Val separately rounds the bundle to "let's call it sixteen thousand dollars." Worth confirming before it goes into a proposal.

## Dispatch Log

---
*Processed from Plaud offline recording on September 11, 2026*
*Source meeting: Meeting with JVL (Diamond Amusements), September 10, 2026*
