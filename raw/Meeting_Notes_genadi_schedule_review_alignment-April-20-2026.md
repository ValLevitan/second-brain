# Meeting Summary — Schedule Review & Alignment
**Date:** April 20, 2026, 1:36 PM Eastern
**Duration:** 1h 6m 42s
**Attendees:** Val Levitan, Genadi Peari

## Summary

This was a status/alignment review covering the active Jira backlog for multiple HFM features and two initiatives (Flex PAY / IP 1014, and a newly-framed Slim FlexPay recycler at IP 1055). The conversation moved through a list-style review of tickets, then shifted midway into a strategic discussion about product direction for dispensers vs. recyclers.

**Tooling / HFM 507 (PayOS design molds).** The tooling design was reported as complete. Genadi estimated a minimum of 4 weeks for samples to arrive from the tooling vendor, with an additional week if corrections are needed. Val parked this item.

**Temporary plastics for Georgia.** Genadi reported that two catalysts (possibly "cates"/"katers" — auto-transcription unclear) were ordered. Val confirmed these are "FIVEN FOR" parts (HFM 514 — "critical parts for Georgia"). Genadi believes the vendor confirmed the order but had not personally seen confirmation emails.

**HFM 511 (Minsk rapid prototype).** Val needs to confirm HFM 511 is ordered in Minsk. Genadi reported he spoke with Pavel, who found a cheaper prototype variant — aesthetically poor ("wire-frame style") but mechanically sufficient for internal use. **Decision:** Use **FDM instead of SLA** (stereolithography) for the rapid prototype, per agreement between Val and Pavel. Val noted HFM 511 is in the "To Do" column but is likely actually in progress, and said he would move it to "In Progress."

**HFM 514 (Michael Perlman / Georgia shipment).** Val identified a needed follow-up with Michael Perlman on the critical-parts shipment to Georgia. Val asked when samples would arrive so that "Odessa" (team/site) would know what to do with them.

**HFM 504 (fifth-country order parts).** Genadi noted this cannot proceed without the full Bill of Materials. He committed to walking through the BOM with Mikhail today. He also mentioned some small items need to be re-ordered beyond what was previously shipped to Georgia.

**HFM 519 (sample plan specifications).** Genadi said he wants to release HFM 519 today — including the sample specifications and BOM with parts — so that the recipient (unnamed "she") can assemble. He suggested the product is simple enough that the assembly can be taught quickly.

**Audio / Rockchip issue.** Genadi flagged a remaining item Pavel is still working: audio is not coming out of the Rockchip. The associated ticket number was unclear — Genadi speculated possibly IP 977.

**HFM 508 reporter change.** Val discovered the reporter on HFM 508 was set to himself, but he is also the assignee. He changed the reporter to Pavel, citing the rule that reporter and assignee cannot be the same person. Val coached Genadi on how to change reporters in Jira and noted Genadi appears to have opened these tasks himself. HFM 506 was discussed in the same vein.

**Flex PAY (IP 1014) — Sample verification testing.** Genadi explained that Pavel is in a testing phase where he verifies full functionality on "sample strips." Pavel took this responsibility on himself because Alexeev cannot do it. All software and hardware must be verified working before release to production. The first two working samples were already sent to Georgia.

**HFM 367 / HFM 370 (Cash Dispenser / IP 1014) — Huizhou metal parts.** Metal parts were ordered from Huizhou. The vendor quoted ~$1,800 for air-shipment. Val recalled agreeing to this but Genadi noted that at the last meeting Val had told Mikhail "give me one day, you work with him" and Genadi was unsure of the resolution. Val admitted he may have dropped this follow-up and committed to checking with Mikhail. **Open:** final confirmation of air-shipping decision for HFM 370.

**Dispenser shipment status.** The dispenser sent to Minsk has been received (Genadi believes Friday). Pavel and Biratko from Minsk have been contacting Genadi asking how to connect it and how to configure it for "candles" (likely a specific payout mode). Separately, the Georgia-bound dispenser was supposed to leave Friday with a larger Georgia shipment that Mary was coordinating; Arkady was to add the dispenser, POS parts, and related components to that shipment free of charge. Val's tentative conclusion: given Minsk already has the alpha unit and is actively integrating, it makes sense to air-ship the Georgia dispenser as well.

**Strategic discussion — FlexPay product definition and pricing.** Genadi described the Flex PAY product as a side-by-side cabinet (narrower base, wider top — similar to the express cabinet form factor) housing a printer card, cash dispenser, bill acceptor, and scanner. Val laid out two go-to-market paths:

1. **Support JVL's FlagSport** directly using this product.
2. **Sell to distributors at discount** (~$8,000) so they can resell under their own brand at ~$11,000. The distributor handles the integration arrangement (e.g., their own Pyramid dongle license).

Val's cost estimate: ~$4,000 product cost. Component breakdown (Genadi): Fujitsu printer ~$1,000–$1,080, plus bill acceptor, plus a Vivo unit (~$2,000?), plus ~$1,500 more in other components. Val estimated $2,500 + $1,500 = ~$4,000 COGS.

Genadi pushed back that the distributor channel is mass-production but the volumes sound small (10–20–50 units), and questioned whether this helps JVL's core product line or pushes JVL into other OEMs' cabinets.

**Strategic pivot consideration — Recycler vs. Dispenser.** Val proposed a different bundling:

- **FlexPay with recycler + FlexSport:** FlexSport at nominal retail $1,200 (wholesale ~$990). Or bundle 5 FlexSports "free" with every FlexPay sold for ~$12,000. JVL's FlexSport cost is ~$80–$100, so giving 10 away is cheaper than putting a printer in each machine (~$300 each for Pyramid, ~$500 for Operator Nami). Val mused about pricing FlexSport at $300 to match Pyramid.
- **Slim recycler-based product (IP 1055):** Genadi confirmed this is the already-planned next generation — slim form factor, recycler printer, no operator required, no moving parts (no paper, no head to clean, etc.). Val believes they can hit a BOM around $3,000 and sell at $9,000. Genadi noted Pavel is already putting a Rockchip and Prizhevil (unclear — possibly a chip/module) in it; the hardware will be cheap.
- **Market positioning:** Val argued the recycler+FlexSport combination is the strongest product. Possibly drive the recycler to a minimum price — COGS ~$2,000, sell at ~$6,000, call paystations "mini" since they have their own module. Plus a $99/month subscription and mobile app for operators to monitor their fleet performance. Val floated abandoning the cash dispenser entirely.
- Genadi's concern: the cash dispenser is being developed for an existing market (Pyramid-printer machines) where JVL's product offers no clear benefit over incumbents. He is worried about effort-to-sales ratio ("potentially lots of effort for selling 3 units and more headaches").

**Pyramid integration / dongle.** The conversation shifted to how existing gaming machines connect their Pyramid printers — via RS-232 with a proprietary Pyramid protocol. Val asked how FlexSport would connect: Genadi explained FlexSport sits on the bill-validator line, intercepting signals. To put a JVL dispenser into a machine that already has a Pyramid printer and bill acceptor, JVL's own printer and bill acceptor are not needed — but to integrate the dispenser with the machine, there must be a Pyramid dongle in the recycler or FlexPay, which requires a contract with Pyramid. Val alternatively suggested selling to wholesalers/distributors in Georgia who could do their own integration (3–4 manufacturers there would want to sell it but lack the technology know-how). Genadi remained skeptical: "I can't quite understand the strategy here."

**Meeting wrap-up.** Val had another meeting starting in 20 minutes and could not defer. The strategic discussion was parked. Val committed to continuing the discussion throughout the week. Genadi noted he wanted to start breaking down tasks for the Slim product (IP 1055) since the feature has been created. Val confirmed IP 1055 exists with 3 features under it and per schedule Genadi should start design. **Val's ask:** Genadi to produce two schedules — a short ~2-week view and a longer-term roadmap — for IP 1055 as his undertaking, ideally today or tomorrow.

## Decisions Made

- **Use FDM, not SLA, for the Minsk rapid prototype (HFM 511).** Rationale: cheaper; mechanical properties sufficient despite poor aesthetics. (Agreed between Val and Pavel previously; reaffirmed in this meeting.)
- **Reporter on HFM 508 changed from Val to Pavel.** Rationale: a user cannot be both reporter and assignee. (Val did this live during the meeting.)
- **Pavel takes over Flex PAY sample verification testing** (previously blocked because Alexeev cannot do it). (Agreed in Genadi/Pavel earlier meeting; confirmed here.)
- **Minsk has received the dispenser** (Friday) and integration is underway with Biratko and Pavel on-site.
- **Lean toward air-shipping the Georgia dispenser** given Minsk's alpha is already live — decision not fully locked pending Val's check-in with Mikhail on HFM 370.
- **Strategic lean:** Recycler + FlexSport is the preferred product direction; cash dispenser may be deprioritized or dropped. **Not yet a locked decision** — parked for continued discussion this week.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val | Confirm HFM 511 is ordered in Minsk with Pavel and move the Jira ticket from "To Do" to "In Progress" | This week | Normal | Genadi already has verbal confirmation from Pavel; Val needs formal confirmation and ticket hygiene |
| 2 | Val | Follow up with Michael Perlman on HFM 514 — critical parts shipment to Georgia; confirm arrival timing so Odessa knows what to do with samples | This week | High | Blocks Georgia site's ability to proceed with received samples |
| 3 | Genadi | Walk through the full BOM for HFM 504 with Mikhail | Today (April 20) | High | Cannot order "fifth country" parts without complete BOM; blocks procurement |
| 4 | Genadi | Release HFM 519 sample plan specifications + BOM with parts list | Today (April 20) | High | Recipient cannot assemble without spec + BOM in hand |
| 5 | Val | Check status of HFM 370 Huizhou metal parts air-shipment ($1,800) with Mikhail — decision Val believes he may have dropped | This week | High | Unlocks whether the dispenser/parts can fly to Georgia |
| 6 | Val | Make final call on air-shipping the Georgia dispenser (likely yes, given Minsk progress) | This week | Normal | Depends on outcome of item #5 |
| 7 | Genadi | Start design work on IP 1055 (Slim FlexPay with recycler) and produce two schedules: a short ~2-week schedule + a longer-term schedule | Today or tomorrow (April 20–21) | High | Val explicitly called this "your undertaking"; schedule input is gating Val's own planning work |
| 8 | Val | Continue strategic product-direction conversation with Genadi throughout the week (dispenser vs. recycler+FlexSport pivot) | This week | High | Meeting ended before resolution; Val said he'll "bother" Genadi all week on this |
| 9 | Val / Genadi | Loop in Pavel on the Pyramid dongle / integration question (contract needed? how to connect FlexPort when a Pyramid printer is already installed?) | This week | Normal | Genadi flagged this needs Pavel's input before strategy can be locked |
| 10 | Val | Resolve HFM 506 task ownership — determine whether Genadi should remain reporter/assignee or change | This week | Low | Process/hygiene follow-up from HFM 508 pattern |
| 11 | Genadi (via Pavel) | Resolve outstanding audio/Rockchip bug (possibly IP 977 — ticket # uncertain) | TBD | Normal | Pavel owns; Genadi to track. Ticket reference needs confirmation |

## Engineering Signals

### Confirmed Signals

- **ADR: Use FDM (fused deposition modeling) instead of SLA (stereolithography) for rapid prototyping on HFM 511.** Rationale captured: cheaper variant sourced by Pavel; mechanically adequate despite aesthetic trade-off. (Val–Pavel agreement, reaffirmed in this meeting.)
- **Engineering solution: Pavel intercepts Flex PAY sample verification testing on the bill-validator line.** FlexPort sits on the bill-validator signal line, intercepting signals — not the printer line. This defines the integration point for the Flex PAY product architecture.

### Suspected Signals

- **Possible ADR: Pyramid dongle integration approach.** To use JVL dispenser/recycler inside a machine already running a Pyramid printer, the recycler or FlexPay must contain a Pyramid dongle, which requires a contract with Pyramid. Alternative: distribute to wholesalers who handle their own Pyramid licensing. No decision reached.
- **Possible REQ/CAP: Mobile app for operator fleet monitoring.** Val proposed a mobile app where operators can see performance telemetry from all their connected JVL machines. Tied to a $99/month subscription.
- **Possible REQ: Subscription service pricing ($99/month).** Val floated this as part of the bundled commercial offer.
- **Possible CAP: Slim FlexPay recycler (IP 1055) — next-generation combined product.** No printer, no bill acceptor, no moving parts, no paper maintenance. COGS target ~$2,000–$3,000, sell at ~$6,000–$9,000. Genadi confirmed the feature exists under IP 1055 with 3 sub-features.
- **Possible strategic decision (not strictly ADR): Deprioritize or drop the cash dispenser product line.** Val leaned heavily in this direction but the call is not locked — parked for continued discussion this week.

## Open Questions

- **HFM 370 air-shipping confirmation** — Val acknowledged he may have dropped this follow-up with Mikhail; needs resolution.
- **Pyramid integration contract** — Is JVL willing/able to sign a Pyramid dongle contract, or do we route through distributors instead? Genadi flagged this needs Pavel's input.
- **Audio/Rockchip ticket number** — Genadi thought it might be IP 977; not confirmed.
- **Cash dispenser product line** — continue or drop? Unresolved; Val leaning toward drop.
- **HFM 506** — unclear whether reporter/assignee changes are still needed; mentioned in passing.

---
*Processed from Teams transcript on April 21, 2026*
*Source meeting: Schedule_review_alignment-April-20-2026*
