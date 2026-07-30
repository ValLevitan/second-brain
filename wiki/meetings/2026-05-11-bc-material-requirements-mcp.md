---
type: meeting
title: BC Material Requirements via MCP (May 11 2026)
date: 2026-05-11
aliases: [Materials requirement use cases, BC material requirements MCP, material requirements MCP, Misha material requirements report, MRP MCP]
source-count: 2
---

# BC Material Requirements via MCP (May 11 2026)

**Date:** 11 May 2026, 8:49pm ET (~21m) (§11 recording header time; the `_164942` filename stamp is a different zone and is not the meeting time).
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/mikhail-perelman.md|Mikhail (Misha) Perelman]], [[wiki/people/lev-rudky.md|Lev Rudky]].

Russian-language working call in which Val proposes bridging [[wiki/people/mikhail-perelman.md|Misha]]'s missing material-requirements (procurement/MRP) report — the one-click Navision report Anatoly built him — using the **Model Context Protocol (MCP) layer JVL has built on top of the Business Central API** (~95% complete; natural-language querying in Russian or English, no code required). The agreed bridge is two-step: [[wiki/people/lev-rudky.md|Lev]] produces the standard un-consolidated BC per-machine/per-subassembly parts report (Step 1, exists today), then Val, via Claude + MCP, performs the cross-subassembly **consolidation** (one row per unique part, quantity rolled up), the **vendor + last-price + minimum-order-quantity enrichment**, and the **per-vendor grouping for POs** in a single combined step (Step 2) — avoiding any modification to BC's standard reports. Auto-issuing POs is deferred to a later phase (Misha keeps the analysis-then-release step manual). Val will synthesise formal **requirements + use cases + a "procurement manager" persona** from this transcript plus Misha's example Excel file, then review the draft with Misha before handing it to the MCP developer. Misha to send the Navision-style Excel sample immediately.

Substance and citations live on [[wiki/topics/business-central-erp-implementation.md]] (May-11 2026 — Material Requirements via MCP) and [[wiki/topics/ai-assisted-development.md]] (May-11 2026 — BC MCP tooling). §15.8: BC / MCP / procurement / tooling economics only; no named-person compensation. Open item (recorded, not resolved): the MCP developer Val is assigning was referenced but not named on the call.

## Sources
- [[raw/Meeting_Transcript_bc_material_requirements_mcp-May-11-2026.md]]
- [[raw/Meeting_Notes_bc_material_requirements_mcp-May-11-2026.md]]
