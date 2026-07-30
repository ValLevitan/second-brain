# Meeting Summary — BC Material Requirements via MCP (Misha / Val / Lev)
**Date:** May 11, 2026, 8:49 PM Eastern
**Duration:** 21m 14s
**Attendees:** Val Levitan, Mikhail (Misha) Perelman, Lev Rudky

## Summary

Russian-language working call (summary in English) covering Misha's pain point on **Material Requirements** reporting out of Microsoft Business Central (BC) and Val's proposal to bridge the gap using the **BC MCP (Model Context Protocol)** integration JVL has been building.

**The MCP context.** Val opened by explaining the MCP-to-BC integration: JVL has developed an MCP layer on top of the BC API, currently ~95% complete. MCP enables natural-language queries (Russian or English) — the protocol translates conversational input into the equivalent API calls. *"You don't need to write a program; you don't need to write modules — you can communicate in human language."* Val noted he is already pulling broad operational data through it (debtors, periods, AP/AR figures, etc.). Misha had not yet heard of MCP. Val offered to assign the MCP developer to Misha's specific material-requirements work.

**Misha's pain point: the missing Navision-style report.** Misha wants a report comparable to what he used to have in **Navision** (legacy ERP) for material requirements planning. The Navision report's key value was one-click, near-instant updates. Val drove out Misha's working model in detail:

- **Input** (any one or more of): part number, subassembly, complete machine, or a set of subassemblies, with **target quantity** ("make 30 units").
- **Output (canonical):** the system tells Misha what parts he is short of after accounting for what's in stock, what's already on order, and what's in transit, and produces a complete shortage list with quantities.
- **Consolidation rule:** when a single part appears in multiple subassemblies, the system **consolidates** — one row per unique part, with the total quantity rolled up. Today the standard BC report does NOT consolidate in a single step.
- **Per-subassembly side-list:** Misha also wants a separate sheet *per subassembly variant* alongside the consolidated view. Example: 200 Echo cabinets/year, broken down as 130 without bill validator + 70 with bill validator. Bulk of parts are shared, some parts differ — Misha needs per-subassembly visibility for cross-checking, alongside the global roll-up.
- **Vendor enrichment:** for each part, the report should include **vendor** (supplier), the **last price paid**, and the **minimum order quantity** (since price depends on quantity tier).
- **Vendor grouping for POs:** when a single vendor supplies multiple parts needed in the requirement, the report should consolidate them into one PO per vendor.
- **Stretch — auto-issue POs:** Misha said this is "probably the next stage." He still expects to do **manual analysis** before any PO is released (deciding which subassemblies to make this period vs defer), so the system should generate POs *only for the subassemblies Misha approves*, not blanket.

**Current state per Lev.** Lev clarified what Business Central does today:
- Standard BC produces the per-machine / per-subassembly parts list on request.
- That list **does NOT consolidate** when a part appears in multiple subassemblies — the same part will appear multiple times in the report.
- The consolidation step is what Misha currently does manually, building a **pivot table in Excel** on top of the BC export. Misha confirmed: "I use those reports — I pivot the Excel myself."
- Toni (Anatoly) historically built specific tweaks for Misha (vendor, last price, minimum order quantity columns) — the "nuances" Misha mentioned. Those are not in BC standard.

**Val's proposed solution path.** Val laid out a two-step bridge:
1. **Step 1 (Lev):** generate the standard BC per-machine / per-subassembly parts report — the one BC produces today, no modification.
2. **Step 2 (Val via Claude + MCP):** take the standard report and have Claude perform the cross-subassembly consolidation, the vendor enrichment (vendor + last price + min order quantity), and the per-vendor grouping in a single combined step. Val: *"today Claude does this in one step."*

This bypasses any modification of BC standard reports while delivering Misha's full functional ask.

**The longer play — synthesise requirements from this transcript.** Val proposed using the meeting recording itself as raw material for drafting formal **requirements + use cases + persona** in the JVL capability/requirement format:

- **Persona:** procurement manager (i.e., Misha himself = the user).
- **Use cases:** derived from the workflow Val walked Misha through above (input target quantity → shortage list → vendor-grouped POs).
- **Requirements draft:** Val will draft from the transcript + Misha's example Navision-style Excel file. *"If you write the requirement correctly, then essentially the code writes itself now"* (via Claude Code).
- **Iteration:** Val + Misha review the draft tomorrow. If something is missing (last price, minimum order quantity, vendor grouping nuance), Misha calls it out. Lev joins if needed. Then the requirements go to the MCP developer for implementation.

**Closing action: Misha sends Val the Excel sample immediately.** Val: send me the file right now and I'll start drafting tomorrow. Misha confirmed and committed to sending the example file in the next minute.

**Implicit point Val made repeatedly.** Whether Misha does the analysis-and-release step manually or the system does it for him *"is not so essential"* — what matters is that the system delivers the consolidated, vendor-enriched shortage list as a single artefact. The actual PO release can stay manual at first; auto-PO is a later phase.

## Decisions Made

- **Val's MCP developer will work on Misha's material-requirements automation** — i.e., the BC MCP layer is the target platform for this enhancement, not new BC reports. (Val.)
- **Two-step bridge accepted as the implementation path:** BC standard report → Claude/MCP consolidation + vendor enrichment + vendor grouping in a single combined step. (Val, accepted by Lev and Misha.)
- **Val drafts the requirements + use cases + persona from this transcript and Misha's Excel example.** (Val.)
- **Misha sends the Navision-style Excel example to Val immediately.** (Misha, in flight at meeting close.)
- **Auto-PO issuance is a later-phase stretch — not in the first pass.** Misha continues to do the analysis-then-release step manually. (Misha, accepted by Val.)
- **The standard BC report (un-consolidated) is acceptable as Step 1 input** — no modifications to BC standard needed. (Lev confirmed availability; Val accepted.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Mikhail Perelman | Send Val the Navision-style Excel example showing the pivot-table consolidation + vendor + last price + min order quantity columns | Within minutes of meeting close (May 11, 2026) | High | Required input for Val's requirement drafting |
| 2 | Val Levitan | Draft requirements + use cases + persona (procurement manager) for the material-requirements MCP feature, using the meeting transcript + Misha's Excel file as inputs | Tomorrow (May 12, 2026) | High | Val: "довольно простой консервативный, на довольно примитивном языке" — accessible language, not deep technical |
| 3 | Val Levitan | Reconvene with Misha (and possibly Lev) to walk the draft requirements and confirm completeness | Within the next few days | High | Validate before sending to the MCP developer |
| 4 | Lev Rudky | Be available to join the requirements review if invited | TBD | Normal | Lev's BC knowledge needed for any standard-report integration questions |
| 5 | Val Levitan / MCP developer | Implement Step 2 (consolidation + vendor enrichment + grouping) in MCP once requirements are approved | After requirement approval | High | Step 1 already exists in BC standard |

## Engineering Signals

### Confirmed Signals

- **CAP — Material Requirements automation via BC MCP.** Two-step pattern: standard BC report → MCP-driven Claude consolidation + enrichment + grouping. New capability under the BC MCP umbrella, owned by Val's MCP developer.
- **CAP — Natural-language-query MCP layer on Microsoft Business Central.** ~95% complete; runs on top of BC API; supports Russian and English natural-language input. Foundational JVL platform capability — many downstream features (this one included) will depend on it.
- **REQ — Cross-subassembly part consolidation: one row per unique part with rolled-up quantity.** Single-pass output, not multi-row by subassembly.
- **REQ — Per-subassembly side-list alongside consolidated view.** Misha needs both — the side-lists exist for cross-checking, not as a substitute for the consolidated view.
- **REQ — Vendor + last price + minimum order quantity columns** on every part row.
- **REQ — Vendor-level grouping for PO generation** (potentially multiple parts → one PO when same vendor).
- **REQ — Stock + on-order + in-transit accounting** before declaring shortages.
- **ADR — Bypass BC standard-report modifications.** Use the BC standard output as-is at Step 1, perform all custom logic in MCP/Claude at Step 2. Avoids touching BC's internal reporting layer.
- **Engineering Solution — Use meeting transcripts as raw material for requirement drafts.** Val's repeated working pattern: record the conversation, feed it to Claude with the example artefact, produce the first-draft requirement document. Applies beyond this feature.
- **CAP — Persona = "procurement manager"** (Misha as the canonical user) — adds to JVL's persona library alongside operator, player, JVL product manager.

### Suspected Signals

- **Possible CAP — Auto-issued purchase orders against approved subassemblies.** Misha said "probably the next stage." Worth tracking as a phase-2 capability, not in the first delivery. — *Val, should this be tracked now as a planned future capability or wait until the first pass ships?*
- **Possible REQ — Vendor-pricing-tier modelling.** Misha mentioned that price depends on quantity. Implicit requirement that the system understand tiered pricing per vendor per part. Not explicitly stated as a deliverable. — *Should this be in scope for Step 2 enrichment, or assumed handled later?*

## Open Questions

- **Who is the MCP developer Val is assigning to this?** Val referenced "the person writing this" but didn't name them on the call.
- **Where does Misha's existing pivot-table Excel live now?** Pulled from Navision originally; Misha will share it. The structure of that file is the canonical reference for the first requirement draft.
- **How are the "nuances" Anatoly built historically captured today?** Val and Misha both referenced these (vendor, last price, min order quantity) — but their source-of-truth in BC vs Misha's offline Excel isn't fully clear. May affect whether Step 1 needs supplementary BC queries.
- **How are subassembly-vs-machine BOMs structured in BC currently?** The system has to traverse subassembly hierarchies for the consolidation step — depth, recursion handling, and any quirks need to be documented during requirements drafting.

---
*Processed from Teams transcript on May 22, 2026*
*Source meeting: Materials_requirement_use_cases-May-11-2026 (20260511_164942)*
