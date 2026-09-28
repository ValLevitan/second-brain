# Meeting Summary — Crane CPI (Jacob Blair): BNR vs SCR recycler consultation

**Date:** February 23, 2026, 2:59 PM Eastern
**Duration:** approximately 31 minutes
**Attendees:** Val Levitan, Juan Martinez, Genadi Peari, and Jacob Blair (Crane CPI, Cincinnati-based, calling from Seattle). Chadwick Pinson (at EuroShop in Germany) and Luis Fuller did not join.
**Raw transcript:** [[Meeting_Transcript_Crane_CPI_Jacob_Blair_BNR_vs_SCR_Recyclers-February-23-2026]]
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Calendar pairing:** Outlook event "Crane CPI Recyclers - JVL Discussion", 3:00–4:00 PM ET, organiser Juan Martinez, attendees Jacob Blair, Chadwick Pinson, Luis Fuller, Genadi Peari. "Jacob" named on the call; confirmed on both keys.
**Context:** this is the engineering origin of the recycler path that later becomes critical (the Aug 25 "CPI Recycler Identified as Critical Path" recording and the Flex-Recycler-Slim work). Notable irony: CashCode — Val's former company — is a Crane brand; Jacob confirmed the "SC head" in the Fujitsu solution "is us."

## Summary

Product deep-dive on Crane CPI's two recycler families for JVL's skill-market kiosk/machine cash handling. Juan framed the need: smaller emerging skill markets, 5–15 machines per location, coins disappearing (pennies cancelled), operators needing a seamless accept-and-dispense experience without armored-car float.

**BNR (Banknote Recycler) Advance.**
- Up to 4 denominations recycled ($1/$5/$10/$20) from two roller-drum recycling cassettes (2 drums each, drum = denomination), 180-note recycling capacity, 600-note cash box, plus a 250-note batch loader cassette (any orientation; validates through the head then routes to the right drum; auto-replenishes low drums).
- Configurable chassis: drop the loader, enlarge the cash box, or add a third recycler (up to 3 cassettes / 6 drums — but still max 4 denominations; two drums can share $20s).
- Val probed swapping loader→recycler cassettes in the field: technically possible but pinned/locked into the spine and labor-intensive — not a field operation. Recycling cassettes are open when out of the machine (security note).
- $50/$100 notes: accepted but routed to cash box only — Jacob is "99% sure" the BNR logic does not recycle them. **The deal-breaker question**: Val is "99.9% sure it's a matter of engineering willingness," and JVL wins exceed $100, so without $50/$100 recycling every solution risks being cost-prohibited. Jacob to confirm with engineering whether the capability exists today (a development business-case otherwise).
- Not marketed for gaming (never a GLI question) — its homes are retail self-checkout (Walmart, Target, Five Below) and transport.
- Price: ballpark $4–5K high side; volume tiers 50/100/250/500; 250-tier pricing needs a minimum commitment.
- Variant: **BNR BNF** (Bunch Note Feed) — 50-note bulk feeding bezel, loader optional, third recycler possible; similar cost.

**SCR Advance.** The SC Advance acceptor (same head as MEI/SC installed base) plus recycling: two stacked recyclers (front/back), 4 drums, 120-note total capacity (30/denomination at four denominations), 600 or 1,200-note cash box (push cassettes — Val's field wisdom: real capacity runs 10–20% below spec), single-note front loading only. Price ~$2–2.5K — deliberately positioned against the Fujitsu dispenser (~$2K dispenser; the market's combined Fujitsu+SC accept/dispense solution lands ~$3K, not $4K as Jacob first suggested — Val corrected him). Genadi's observation: two SCRs ≈ one BNR in capacity and price, with full redundancy and better serviceability; Val agreed and noted the doubled volume earns a better discount. Integration: BNR has the fuller stack (UAPI, device-level, Java); SCR is RS-232/USB only.

**The lean.** If $50/$100 recycling is confirmed nowhere, and it is "a market test regardless," JVL leans **SCR** — proven mass-deployed device, flexible, redundant in pairs, right price. BNR at $4–5K is "cost prohibitive — a non-starter, even if it's a better unit."

**Logistics.** Jacob to have engineering share SDKs/APIs/firmware command lists — Val asked for **GitHub, not OneDrive** ("GitHub is much more appropriate for us"); Jacob to check. Contact info exchanged via Juan.

## Decisions Made

- **The $50/$100 recycling confirmation is the gating question for the whole product choice.** (Val)
- **Working lean: SCR Advance (possibly paired) over BNR on cost, redundancy and field-proof.** (Val, Genadi)
- **Integration materials to be delivered via GitHub if possible.** (Val's requirement)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Jacob Blair | Confirm with engineering whether BNR and SCR can recycle $50/$100 today | ASAP | Critical | Deal-gating; JVL wins exceed $100 |
| 2 | Jacob Blair | Have engineering share SDKs/APIs/firmware docs (GitHub preferred) | ASAP | High | Genadi executing integration |
| 3 | Jacob Blair | Send the BNR/SCR data sheets | ASAP | Normal | Promised on the call |
| 4 | Jacob Blair | Send his contact info | Same day | Low | Val asked for the record |
| 5 | JVL (Juan/Genadi) | Reconvene on next steps once the 50/100 answer lands | After #1 | High | "We can sync back up and go through next steps" |

## Open Questions

- $50/$100 recycling capability (the whole decision hangs on it).
- Real volume commitments JVL can make for tier pricing.
- Whether GLI certification ever becomes relevant for a retail-marketed recycler in skill-gaming use (Genadi raised it; not fully answered).

## Possible mis-transcriptions (not in glossary — confirm before fixing)

- "Fidget Two" (00:16:15) — **Fujitsu**; "ACR" (00:21:47, 00:24:35) — **SCR**; "PR" (00:22:03) — **BNR**; "MEI Advanced SCN Advanced" (00:24:35) — **MEI / SC Advance**; "nodes" (00:24:56 ff) — **notes**; "the eliminations" (00:25:21) — **denominations**; "Jay" speaker tag at 00:00:36 — this is the Crane call, not AKS; mislabeled voice profile.

## Dispatch Log

---
*Processed from Plaud recording on September 24, 2026 (backlog batch 2)*
*Source recording: 02-23 Bill Recycling Solutions Consultation: BNR vs. SCR for Skill-Based Gaming (Plaud)*
