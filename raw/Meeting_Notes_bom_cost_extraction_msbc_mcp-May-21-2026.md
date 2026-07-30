# Meeting Summary — BOM Cost Extraction from MSBC: Source Priority + Navision Bootstrap
**Date:** May 21, 2026, 1:32 PM Eastern
**Duration:** 14m 2s
**Attendees:** Val Levitan, Lev Rudky

> **Sequence note:** This is the follow-up working call to the May 11 Material Requirements MCP session (see `BC Material Requirements MCP-May-11-2026/`). Same MCP target system; this conversation pins the **cost-source priority order** that the MCP will use and the **bootstrap problem** of missing 2026 cost data in Microsoft Business Central (MSBC).

## Summary

Russian-language working call (summary in English) between Val and Lev clarifying **where cost-per-part data for the Material Requirements report should come from**, in what priority order, and how to bootstrap the data set given JVL's recent ERP migration. The MCP developer (Nathan) will implement the priority logic; the data-population problem requires bringing back **Anatoly (Toli)** — JVL's former engineer who built the Navision reports — as a contractor.

**Source confusion at the top.** Lev opened by saying he had written up an approach for getting an automatic report using only BC's internal tools. Val: *"what's the difference what tools you use — the data is what matters. For the report to be produced by any tool, the tool needs to access the source. Where is the source?"* Lev: the difference is that going through BC's standard tools versus through the MCP enables different capabilities.

**ERP migration context.** Val laid out the company structure:
- **GVL Systems** = US legal entity (was historically "Three TIMs"), runs in **Microsoft Business Central**.
- **GVE Labs / GVL Labs** = Canadian entity, also in **Microsoft Business Central**.
- **All Purchase Orders historically came from Navision** (legacy ERP).
- **JVL switched to Microsoft Business Central on January 1, 2026.** Not all purchase orders are yet flowing through BC — many are still being closed out under the Navision-era data path. Some material costs may have been entered manually into BC.

This migration state directly determines what data the cost-extraction logic can rely on.

**Cost-data source hierarchy — Lev's clarification.** BC actually exposes **three distinct cost sources**:

1. **Last paid invoice price** — most reliable; price actually paid for physical receipt of the item, after the purchase order was completed and the invoice was paid.
2. **Open purchase order price** — price on an active PO that has not yet been received and/or invoiced. Less certain than paid (terms could shift, deliveries fail), but provides a forward-looking cost signal.
3. **Vendor Card / Vendor Catalog (Item Vendor Catalog)** — manually entered per-part-per-vendor prices that can be loaded into BC independently of any PO or invoice activity.

**Critical distinction Lev emphasised.** BC's standard reports use only Source 1 (paid invoices). The **MCP path** can use all three. *"If we use just BC, only paid prices. If we use MCP, we have flexibility to pull from paid + open PO + catalog."* This is why the source-priority decision belongs in the MCP layer, not in BC.

**Val's priority decision for the MCP:**

1. **Priority 1: Last paid invoice price** (Source 1).
2. **Priority 2: Open purchase order price** (Source 2).
3. **Priority 3: Vendor Card / Vendor Catalog price** (Source 3).

If all three are absent → **explicit zero / "no data"** flag in the report, requiring human analysis. Val: *"if it's a washer or a nut, the zero doesn't matter. If it's a new board, it matters."*

**Trade-offs Lev raised (and Val accepted).** Each priority position has counter-arguments:
- Paid invoice can be inflated if it was a small-quantity / one-off purchase.
- Open PO might reflect a different vendor with different price (e.g., when a fast delivery was needed).
- Vendor catalog can be stale.

Val: *"I understand all of this firmly."* The chosen priority order is judgment + simplicity, not optimality — and the report can flag low-confidence rows for review.

**The bootstrap problem — most of 2026 has no BC cost data.** Val acknowledged: *"we mostly haven't been buying anything in 2026."* So sources 1 (paid invoices) and 2 (open POs) are sparse. To make the MCP useful from day one, **the Vendor Catalog (Source 3) needs to be populated** with historical cost data carried over from Navision.

**Bootstrap plan — get Toli involved.** Val's proposal:
- **Anatoly (Toli)** — former JVL employee, no longer working for the company — built the legacy Navision reports historically.
- The cleanest path is to ask Toli to extract the cost data from Navision and load it into the BC **Vendor Card / Vendor Catalog**.
- **First check with Toli:** (a) does he have time? (b) does he want to do it? (c) what does he charge?

**Val's caution on Toli's pricing.** Val flagged he has personal experience with a different former employee who, after being terminated, quoted such a high price for follow-up work that Val didn't even want the conversation. *"I'm not saying Toli is that person, but I want to confirm."* Lev: *"first just send Toli the request — if it's a simple ask, he may just do it. If he objects, then we negotiate."* Val: *"I don't want him doing it for free either. He owes us nothing."*

**Lev's concern about overwriting BC with Navision data.** Lev pushed back briefly: dropping old Navision prices into BC overwrites whatever's already there with potentially stale data. Val: *"in our case, prices haven't really changed."* Lev accepted, with the constraint that for any part whose price *has* shifted since Navision, the Navision-era number is wrong — but Val's call is that this case is rare enough to accept.

**Mechanism for engaging Toli.** Val: open Toli's BC account; describe what he needs to do; if the request is small, he likely just executes; if it grows, negotiate compensation. Either way Val explicitly opposed asking Toli to work without payment.

**Closing flow.** Val articulated the next-step chain:
1. Take this meeting's transcript and the May 11 transcript.
2. Feed both to Claude (via the MCP / LLM intelligence) to draft formal **requirements + use cases** for the Material Requirements MCP feature.
3. Lev reviews; if there are gaps, the requirements get revised.
4. Hand the finalised requirements to **Nathan ("Nate")** — the MCP developer — who writes the actual MCP feature with the priority logic specified above.
5. In parallel, **open Toli's BC account** and engage him to bulk-populate the Vendor Catalog from Navision cost data.

Val closed: *"Okay, opened account, transcripts, requirements, capabilities for MCP, Nathan builds. Done."*

## Decisions Made

- **Cost-source priority order for the Material Requirements MCP:** (1) last paid invoice, (2) open purchase order, (3) Vendor Catalog. (Val.)
- **MCP is the right layer to apply the priority logic** — BC standard reports cannot use sources 2 and 3 the same way. (Lev's clarification, accepted by Val.)
- **Vendor Catalog will be populated with historical Navision cost data** to bootstrap 2026, where paid-invoice and open-PO data are sparse. (Val.)
- **Toli (Anatoly) is the right person to do the Navision-to-BC cost-data load.** Engaged as a paid contractor — neither at his historical employment rate nor for free. (Val.)
- **Val will not ask Toli to work for free** — explicitly affirmed. (Val.)
- **Stale-price risk accepted as low** in JVL's case (prices haven't shifted materially since the Navision era for the parts in scope). (Val, Lev concurred.)
- **Zero-cost rows in the report require human analysis** — particularly for high-value new parts. Small commodity items (washers, nuts) get less attention. (Val.)
- **Next-step chain:** transcripts → Claude-drafted requirements + use cases → Lev review → Nathan implements MCP, in parallel with Toli loading Vendor Catalog from Navision. (Val.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val Levitan | Use this transcript + the May 11 BC MCP transcript to draft Material Requirements MCP requirements + use cases through Claude | Within the next few days | High | Becomes Nathan's specification |
| 2 | Val Levitan | Share the drafted requirements with Lev for review | Once drafted | High | Lev surfaces gaps before Nathan starts |
| 3 | Val Levitan | Open Toli's BC account; reach out to Toli with a clear scope and ask whether he can do the Navision-to-BC Vendor Catalog cost-data load | Soon | High | Bootstrap dependency for the MCP feature |
| 4 | Val Levitan | Confirm Toli's compensation expectations before scope grows | When Toli responds | High | Avoid the terminated-employee pricing trap |
| 5 | Anatoly (Toli) | Extract cost data from Navision and populate the BC Vendor Card / Vendor Catalog for parts where current 2026 paid-invoice and open-PO data are absent | After engagement is confirmed | High | Bootstraps the entire material-requirements report |
| 6 | Nathan ("Nate") | Implement the Material Requirements MCP with the three-source priority logic (paid invoice → open PO → vendor catalog) | After requirements finalised | High | Core deliverable; depends on the requirement document |
| 7 | Lev Rudky | Review drafted requirements; surface any missing nuance (vendor selection, quantity-tier pricing, etc.) | When draft arrives | High | Domain validation |

## Engineering Signals

### Confirmed Signals

- **ADR — Three-source cost-data hierarchy for MSBC parts.** Paid invoice (1) → open PO (2) → vendor catalog (3) → "no data" with human flag if none of the three.
- **ADR — Source priority logic lives in the MCP layer, not in BC.** BC standard reports cannot integrate sources 2 and 3 — the MCP wraps the priority logic externally.
- **CAP — Vendor Catalog (Item Vendor Catalog) as a third independent cost-data input.** Manually populated; not dependent on transactional activity (PO or invoice). Enables bootstrap of cost data when transactional volume is low.
- **REQ — All historical Navision-era cost data is bulk-loadable into BC Vendor Catalog.** Mechanism not yet pinned; Toli will design / execute.
- **REQ — Zero-cost rows in the Material Requirements report are flagged for human analysis** — not silently treated as missing.
- **Engineering Solution — Transcript-as-input pattern (repeated).** Val explicitly cited the meeting transcript itself as raw material for drafting requirements — Claude consumes the transcript + supporting docs to produce the first-draft requirement record. Same pattern as the May 11 meeting and the May 15 Flex-Recycler session.

### Suspected Signals

- **Possible REQ — Quantity-tier price modelling.** Lev raised that paid invoice prices can be inflated for small-quantity buys. The MCP may need to model price-by-quantity tier per vendor per part. — *Val, is this in scope for Nathan's first delivery, or a phase-2 enhancement?*
- **Possible CAP — Cost-confidence scoring per row.** The three-source hierarchy implies different confidence levels per source. Worth surfacing a confidence indicator alongside the price so users can spot low-confidence rows even without the source notation.
- **Possible ADR — Re-engagement model for former JVL employees as contractors.** Toli's case will set a precedent. *"Don't ask them to work for free; don't accept inflated terminated-employee rates either."* Worth formalising as a JVL policy for past-employee contractor engagements.

## Open Questions

- **Will Toli accept the engagement?** Open until Val reaches out. Lev believes he likely will if the scope is small.
- **What is Toli's rate?** Unknown. Val's hard floor: not free; soft ceiling: not the punitive-terminated-employee rate.
- **What is the exact list of parts requiring Vendor Catalog bootstrap?** Not enumerated in this call — Toli (or someone) will need to walk the BOM and identify which parts lack 2026 paid-invoice / open-PO coverage.
- **Quantity-tier pricing scope.** Open (see Suspected Signals).
- **Stale-price boundary:** Val and Lev agreed prices "haven't really shifted" in JVL's case — but the report should ideally surface any cost row drawn from Vendor Catalog that's older than some threshold (e.g., 12 months). Not explicitly required, but worth raising in requirement drafting.

---
*Processed from Teams transcript on May 22, 2026*
*Source meeting: Extract_BOM_MSBC-May-21-2026 (20260521_093218)*
