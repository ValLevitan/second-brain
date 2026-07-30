---
type: meeting
title: BOM Cost Extraction from MSBC via MCP (May 21 2026)
date: 2026-05-21
aliases: [BOM cost extraction MSBC MCP, MSBC BOM cost MCP, cost-source priority MCP, Navision cost bootstrap, Extract BOM MSBC, Item Vendor Catalog cost source]
source-count: 2
---

# BOM Cost Extraction from MSBC via MCP (May 21 2026)

**Date:** 21 May 2026, 1:32pm ET (~14m) (§11 recording header time; the `_093218` filename stamp is UTC, 4h behind — not the meeting time).
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/lev-rudky.md|Lev Rudky]].

The follow-up working call to the [[wiki/meetings/2026-05-11-bc-material-requirements-mcp.md|May-11 BC Material Requirements MCP session]] — same MCP target system, this time pinning **where per-part cost data comes from** for the material-requirements report and **how to bootstrap it** given JVL's Jan-1-2026 Navision→Microsoft Business Central (MSBC) migration. Lev clarified that MSBC exposes **three distinct cost sources** and that only the MCP path (not BC's standard reports) can use all three; Val fixed the priority order (last paid invoice → open purchase order → Vendor/Item Vendor Catalog → explicit zero + human flag if none). Because JVL bought little in 2026, paid-invoice and open-PO data are sparse, so the Vendor Catalog must be **bootstrapped with historical Navision cost data** — Val proposed re-engaging former JVL engineer **Anatoly ("Toli")**, who built the legacy Navision reports, as a paid contractor to extract and load it (explicitly not for free, and mindful of a past terminated-employee over-quoting). Next-step chain: this transcript + the May-11 transcript feed a Claude-drafted requirements/use-cases document → Lev reviews → **Nathan** builds the MCP with the priority logic, in parallel with Toli's Navision→Vendor-Catalog load.

Substance and citations live on [[wiki/topics/business-central-erp-implementation.md]] (May-21 2026 — three-source cost hierarchy + Navision bootstrap) and [[wiki/topics/ai-assisted-development.md]] (May-21 2026 — transcript→requirements→MCP pattern reused). §15.8: BOM/MSBC/cost-extraction/tooling economics only; no named-person compensation (Toli's rate was discussed as unknown/to-be-confirmed — no figure stated or recorded). Recorded, not resolved: "Anatoly (Toli)" the former Navision-report builder is not force-matched to a page — possibly the same Anatoly referenced elsewhere (e.g. the departed Anatoly / [[wiki/people/anatol-strekalov.md|Anatol Strekalov]], Sr. Excel/SQL programmer) but left unlinked per the May-11 treatment.

## Sources
- [[raw/Meeting_Transcript_bom_cost_extraction_msbc_mcp-May-21-2026.md]]
- [[raw/Meeting_Notes_bom_cost_extraction_msbc_mcp-May-21-2026.md]]
