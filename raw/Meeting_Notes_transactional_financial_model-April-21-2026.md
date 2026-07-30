# Meeting Summary — Transactional Financial Model / Competitive Landscape
**Date:** April 21, 2026, 7:02 PM Eastern
**Duration:** ~1h 14m
**Attendees:** Val Levitan, Juan Martinez, Felipe Miranda Giorgi, Andrei Klimovich

## Summary

The meeting was originally scheduled to discuss JVL's pricing strategy for the transactional/POS product, but within the first two minutes Val pivoted the agenda. He argued that discussing pricing before mapping the competitive landscape would be "shooting ourselves in the foot," and the group unanimously agreed to redirect the session to discovering competitors, cataloguing their product capabilities, and tabulating their pricing — with pricing strategy deferred to a later meeting once that landscape document exists.

**Competitor inventory (Georgia focus, with some adjacent markets).** Felipe led off with the list he'd shared with Andrei the previous Friday. The competitors named:
- **Incomm** — dominant transactional processor (characterized as a "$6 billion processing company" per Val). Distributes the **Pax 80** handheld (an off-the-shelf Android device). Holds ~95% market share in Georgia per Juan.
- **Vanilla Games / Cadrex** — Cadrex is a hardware manufacturer.
- **EasyLynx** — SaaS / TITO provider for multiple solutions.
- **Intuitive Financial Systems** — gift-card dispenser, distributed by **Ivy Promotions** (Fred Ivy). Felipe reported that locations have been removing these units due to uptime/service complaints. IGT's M3T kiosk, distributed the same way, has also been pulled from locations — reputedly due to poor customer service in Georgia rather than device malfunction.
- **Win Systems / Winners Marketing**
- **Gewete (GWT)** — Austrian, part of Germany's Merkur group. Produces the **Count R** kiosk, well-established and deployed in Nebraska. Actively pushing at every Gamoa event.
- **Banilla** — has a product (details not deep-dived).
- **Access** — sometimes bundled as AFT + printer.
- **Arc (Dean's company)** — Mark Martinez contacted Felipe about configuring JVL machines to print both a Mother Goose ticket and a TITO ticket from the back-end (no physical printer on the machine). The design uses dual SAS with the secondary SAS and shared signal from bill-acceptor / flashing cables to produce a TITO ticket at the cashier for inter-machine portability. Felipe asked Mark for an email spec; not yet received.
- **Bulldogs Gaming Kiosk, Ultra, Inna Max** — proprietary Georgia/Nebraska operators that will stay on their own solutions.
- **SGK** — Texas-based. Andrei noted they have a full ecosystem with published pricing: **kiosk $7K, printer $169, link board $200, "redemption tablet" $700** (the tablet sounds functionally like a Pax 80). They also offer a free root management application and mobile app. Coverage: Texas, Puerto Rico, Virginia, Georgia, North Carolina, Wisconsin. Juan recalled they were positioned directly opposite JVL at last year's show.
- **Blue Scale Kiosk** — Felipe believes this is the white-labeled solution behind Mims Amusements' setup, which uniquely lets a player card back into the games after funds are received (gift card → player card transfer).
- **Billy Luke** — pitching a phone-to-bank digital wallet model. Juan/Val flagged hardware dependency (machines don't natively talk to phones, no display for QR) and legal barrier (Georgia only permits deposit on prepaid cards, not direct-to-bank).
- **Ready Payouts** — in Felipe's report, claims cash-to-card self-service with load-to-wallet.

**Pricing intel captured.** Pax 80 is either $800 or $1,000 per device in JVL's records — Juan suspects that's legacy/high (it's "a glorified Android device"). Val separately estimated Incomm's actual Pax cost at ~$250 with a $300 sell, i.e. Incomm is running the hardware at a loss to secure the transactional relationship. SGK pricing captured above.

**Incomm's posture and the fraud problem.** Val's thesis, endorsed by Juan: Incomm is a transactional processing company, not a hardware house, and doesn't want the Pax business — it's a stopgap to secure the market ahead of the July 1 enforcement. Pax is fully manual (employee enters payout amount, encodes blank card), which creates massive shrinkage risk — Incomm itself had reportedly seen $20K–$30K/day in theft at one point. Incomm has already signalled to JVL that when its contracts start expiring, it will happily yield the POS position to JVL if JVL can deliver a secure dispenser-based POS that locks cards and reads the win signal directly from the machine (intercepting between Mother Goose and the printer to expose a single yes/no confirmation, eliminating 90–95% of fraud).

**The double-conversion legal flow (Georgia).** Val walked Andrei through the regulatory framework: winnings move from e-wallet → prize card (dispensed) → skill card → ATM-redeemable cash. Incomm has told JVL that GLC has approved a forthcoming card variant that, for a service fee ($2.50–$5 per transaction, up to a believed $1,000 cap — Felipe challenged this, noting ATMs typically cap ~$200 per withdrawal), can be redeemed at any ATM. Expected live ~September. Val and Juan agreed this will "kill everyone else" not adopted to support it. Val pointed out the experience is designed so cardholder sees win-to-cash in ~5 seconds even though legally the money passed through every step virtually — "within one millisecond" was his rhetorical device.

**Product direction: POS first, then dispenser, then recycler (FlexSlim).** Val described a phased evolution:
1. **POS alone** — already eliminates much of Pax's manual-entry fraud because the win amount comes from the machine signal, not keyboard entry.
2. **POS + dispenser** — physical cards locked in a preloaded dispenser of ~500 cards; 90–95% fraud elimination claimed.
3. **POS + recycler (FlexSlim)** — ultimate target. Recycling technology means no cash-refill logistics (contrast with Texas/Nebraska dispenser-only setups that require armored-truck refills — "incredibly expensive"). Val also floated a long-term vision of machines being built with the recycler integrated (parallel to the 1998 bill-acceptor side-mount "dog house" era), noting recyclers will drop below $1,000 at volume.

**FlexSlim status.** First production units targeted June 20 (Juan confirmed a shipment leaving Mexico City the following day). Alpha release dated May 1 per the shared screen (HFM 513 was May 15 production). Alpha will stay in the Georgia office only — 3D-printed plastic housing, only two sets, internal demo/QA purpose.

**Economics of the status-quo retrofit.** Val did the math live: ~6,500 locations × $7,000 per kiosk = ~$45M; plus ~35,000 machines × $1,000 for bill-acceptor + printer + install = ~$35M; ~$80M total pre-labor. Plus ~20% of current inventory (5,000–7,000 machines) has only a single SAS port already occupied by the Lottery Corporation and cannot be retrofitted at all. Val and Juan framed this as a non-starter for masters/operators — "it will be a 10-year project," performed in-field at gas stations with custom harnesses and downtime.

**Market urgency and sales posture.** Felipe reported that in the last two weeks he's seen masters starting to call with genuine urgency ahead of the July 1 enforcement — none have enthusiastically adopted any single solution. Val coached the sales approach extensively: present JVL as unjustly rushed by legislation (aligning with the customer's resentment), position the POS as a deliberate starter MVP, never argue with Pax holders, acknowledge their choice, and frame JVL as a partner whose product will grow week-by-week. He also gave Andrei explicit demo-sequencing guidance for ethnic sub-communities in the Georgia operator market (acknowledged on record as ethically fraught and flagged for HR-sanitization by Juan).

**Andrei's upcoming Georgia trip.** The group settled on Andrei arriving around May 13 for the May 14 meeting — not May 1 as previously discussed. The Alpha product won't be installed at customer sites; it stays in the Georgia office. Purpose of the trip is customer relationship-building and market familiarization, not product demonstration. Val counselled against digitizing the visit with agendas or commitments — approach customers as a learner seeking intelligence, ideally over a steak or hamburger.

## Decisions Made

- **Meeting agenda pivot** — Deferred pricing strategy; prioritized competitive landscape discovery first. (Decided by Val, endorsed by Juan, Felipe, Andrei)
- **Product roadmap sequence** — POS → POS+dispenser → POS+FlexSlim recycler. POS is the no-brainer first rollout because masters will not absorb the $80M retrofit cost. (Val's thesis, unchallenged)
- **Andrei's Georgia travel** — Arrive ~May 13 for the May 14 meeting. Do not arrive May 1. Alpha will stay in-office; trip purpose is customer discovery, not product demo. (Decided by Val, agreed by Juan and Andrei)
- **Sales positioning** — Present JVL as sympathetic to operators burdened by legislation; POS is a starter MVP, not a finished product; never argue with Pax holders. (Val coaching; Andrei accepted)
- **Next meeting** — Wednesday April 29, 2026, same time. Val to send the invite. Moved from Tuesday to accommodate Juan and give Andrei more research time. (Agreed by all)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Gather competitor intelligence and organize it into a side-by-side capability and pricing comparison table covering all named competitors (Incomm/Pax, Gewete/Count R, SGK, Vanilla/Cadrex, EasyLynx, Intuitive Financial/Ivy, M3T/IGT, Arc/Dean, Blue Scale, Win Systems, Banilla, Billy Luke, Ready Payouts, Bulldogs, Ultra, Inna Max) | April 29, 2026 (next meeting) | High | Foundation document required before any pricing strategy conversation can be productive — Val's explicit gating condition |
| 2 | Andrei Klimovich | Share the SGK website link in the meeting chat | Same day (April 21) | Normal | Juan requested it during the call |
| 3 | Felipe Miranda Giorgi | Follow up with Mark Martinez (Arc / Dean's company) to request a written email spec describing what they need from JVL to support their Mother-Goose + TITO dual-print kiosk integration (dual SAS, bill-acceptor signal sharing, secured-enhanced AFT configuration) | End of April 21, 2026 | Normal | Customer is rushing to install; earlier verbal conversation was incomplete. Felipe needs written requirements to hand to the engineering team |
| 4 | Juan Martinez | Double-check JVL's recorded Pax 80 device price ($800 or $1,000); he believes it's likely lower | Before next meeting (April 29) | Normal | Input to Andrei's competitive pricing table; current number may be stale/legacy |
| 5 | Val Levitan | Send calendar invite for next meeting — Wednesday April 29, 2026, same time as this one | Before April 29 | Normal | Val explicitly volunteered |
| 6 | Andrei Klimovich | Plan and book Georgia travel arriving ~May 13 for the May 14 customer meeting | Before May 13 | High | Alignment already reached; logistics still Andrei's to execute |
| 7 | Felipe Miranda Giorgi | Coordinate with Andrei on signing him in / escorting him to the May 14 meeting; Felipe confirmed Andrei can "just show up with me" | Before May 14 | Normal | Customer-facing event Andrei attends as a learner, not a presenter |

## Open Questions

- **Pax 80 actual price** — $800 vs $1,000 in JVL's records, Juan believes lower. Juan owns the double-check.
- **ATM redemption withdrawal cap** — Val said $1,000 per card; Felipe challenged, noting ATMs typically cap ~$200 per withdrawal which would force multiple-fee redemptions. Unresolved.
- **Mark Martinez (Arc) written spec** — Not yet received; Felipe to push today.
- **Billy Luke's phone-to-bank model legality** — Val and Juan flagged Georgia legislation restricts deposits to prepaid cards. Felipe noted some softening on debit (not credit) but Juan clarified not all debit cards qualify — specifically Incomm's card variants cannot enter an ATM. Resolution depends on what provider Billy Luke claims to use.
- **Readiness to demo Alpha to operators in May** — Val's view is it depends on the product's polish at the time; he deferred the judgment ("I haven't touched it, I don't know what it is"). Andrei expressed discomfort meeting customers with nothing to show after "two years of demo." Tentatively resolved as: first meeting is learner/relationship, no product required.

---
*Processed from Teams transcript on 2026-04-21*
*Source meeting: Transactional Financial model*
