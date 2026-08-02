# Meeting Summary — Recycler Redemption — Partial vs Full-Only Decision
**Date:** July 24, 2026, 8:07–8:55 AM Eastern
**Duration:** ~48 minutes
**Attendees:** Val Levitan, Andrei Klimovich, Juan Martinez, Alexander Biratko
**Raw transcript:** [[Meeting_Transcript_Recycler_Redemption_Partial_vs_Full-July-24-2026]]

## Summary

The call settled Alexander's question: does the recycler support partial redemption? The answer is split by stage. Scope was restricted to the Georgia recycler, under the working assumption that cash payout becomes permitted there.

**Terminology.** The printed QR paper a player carries between machines is the "JVL temporary wallet" (not "e-wallet"). It lives only inside one location, for a short time. Two cards exist: Prize Pay (Incom's current gift card, replaced the old yellow Georgia lottery card, $2 issue fee, not reloadable) and Skill Play (the new card, not live yet; spelled with "play"). Skill Play's purpose: play at any machine, or get cash at an ATM.

**Redemption flow decided.** Step 1: at the recycler, the JVL temporary wallet is always redeemed 100% — no split. All money moves to Prize Pay. Val expects Prize Pay to become a virtual background step; the player physically ends up with a Skill Play card. Total fees to the player: $5 ($2 Prize Pay + $3 Skill Play at redemption). Val said Incom takes no share of the $3 (per John), though it is worth re-confirming. Andrei noted FlexPay allows split redemption, but Val ruled it out as a precedent — FlexPay was frozen a year to a year and a half ago.

**Step 2: cashing out a Skill Play card at the recycler.** Partial IS allowed here. The player inputs the amount he wants. The recycler checks the amount against the bills it actually holds and, if it can't pay the exact figure, offers the nearest options (e.g., "80 or 90"). The player never chooses denominations. The cash-out fee is fixed per location, set at install ($2–5 range, competing with ATM fees) — not dynamic, but the on-screen message must reflect the configured value.

**Limits.** Each recycler will have a configurable per-transaction maximum (perhaps $400–500; experience will decide), based on mechanical capacity, not legislation. No jackpots are paid from the recycler. Large amounts (e.g., $1,500) get sent to the window/attendant — Val expects every recycler location to also have a Flex IQ, and location owners to welcome that.

**Card locality.** Cards issued at location A cannot be redeemed at location B. This is the location owner's rule (industry standard, like casino tickets in Las Vegas), not a JVL limitation. Regular bank/debit cards and outside gift cards are not accepted — the recycler only pays cards issued at that same location.

**Service and security requirements (for Alexander).** The recycler needs an administrator mode for filling and removing money (it has both; some models add a stock-feed add-on holding 30–50 bills). The system must always know the cash box count (cash box is separate from recycling cassettes, ~1,000 bills) and trigger a collection service call at ~800 bills, since locations are remote and every device will have a modem. Cassette removal (recycling or cash cassette, power on or off) must raise an alert. Because bills can't be recounted after reinsertion, an unlawful cassette removal is a red-alert condition: stop operation and require the cassette to be fully emptied, recounted, and refilled. Val called cassette skimming "the perfect theft" this procedure must block.

**Scope.** Georgia is the focus now only because it has the most clarity; if Texas or Nebraska becomes clearer, direction can shift. Skill Play timing per Incom: originally Q4, latest word late August–early September. Its API is called "Alder"; it may not have been officially requested yet.

## Decisions Made

- **JVL temporary wallet is always redeemed in full at the recycler — no partial redemption at that step.** All funds move to the card. (Decided by Val; agreed by Andrei, Juan)
- **The recycler always dispenses a physical Skill Play card — no cash-or-card choice at that step.** Operators and locations want the card dispensed; it preserves the counter relationship with players. (Decided by Val, supported by Juan)
- **Partial cash-out from a Skill Play card at the recycler is allowed.** Player inputs an amount; machine verifies against its bills and offers nearest feasible amounts; no denomination choice. (Decided by Val and Andrei, confirmed to Alexander)
- **Cash-out fee is fixed per location, set at installation** — same model as ATM fees. (Decided by Val)
- **Per-transaction payout maximum is a location-level configuration**, driven by mechanical capacity; no jackpot payouts from the recycler. (Decided by Val; config requested by Alexander)
- **Cards are location-bound; foreign cards and regular bank cards are not accepted.** (Decided by Val and Juan)
- **Unlawful cassette removal is a red-alert event** requiring full empty/recount before the cassette returns to service. (Decided by Val)
- **Current scope is the Georgia recycler**, while staying open to other states if clarity improves. (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Juan Martinez | Share this meeting's recording and transcript with Andrei as soon as ready | July 24, 2026 | Normal | Andrei asked at close of call; Juan said "Absolutely" |
| 2 | Andrei Klimovich | Update the recycler requirements and add the missing parts based on this conversation | TBD | High | Alexander's development work depends on these requirements |
| 3 | Val Levitan | Re-confirm with Incom (John) whether they take a share of the $3 Skill Play redemption fee | TBD | Low | Val: "it's worth asking again" |
| 4 | [Unassigned — needs clarification] | Officially request the Skill Play card API ("Alder") from Incom | TBD | Normal | Raised by Andrei; Juan unsure whether it was formally requested |

## Open Questions

- **PCI / ATM-network requirements** — Incom did not reply about JVL joining their ATM network; ATM-class rules (accessibility, Braille, etc.) could force recycler adaptations. (Raised by Juan)
- **Does the Skill Play card have a PIN?** (Raised by Andrei; Val unsure)
- **Does Incom take a share of the $3 redemption fee?** Val believes not, per John; to be re-confirmed. (Undertaking #3)
- **Has the Alder API been officially requested?** (Undertaking #4)

## Dispatch Log

---
*Processed from Teams transcript on July 24, 2026, 10:05 AM Eastern (scheduled watcher run)*
*Source meeting: Recycler Redemption — Partial vs Full-Only Decision*
