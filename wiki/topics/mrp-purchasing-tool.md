---
type: topic
title: MRP purchasing-planning tool (Nathan Carver's MSBC purchasing tool)
date: 2026-06-10
aliases: [MRP, purchasing tool, Nathan MRP, MSBC MRP, material requirements planning tool, purchasing dashboard]
source-count: 3
open-questions: 3
---

# MRP purchasing-planning tool (Nathan Carver's MSBC purchasing tool)

The **MRP tool** ("material requirements planning" / purchasing-planning tool) is a purchasing-decision helper [[wiki/people/nathan-carver.md|Nathan Carver]] is building for [[wiki/people/mikhail-perelman.md|Mikhail Perelman]] (Misha), JVL's procurement manager. It connects to **Microsoft Business Central (MSBC)** through the BC API, takes **plain-language commands** (an item number and a quantity), reads what BC knows, works out what's short, and recommends what to buy — a talk-to-it dashboard/report that replaces the old Excel purchasing sheet Misha used to run. This page is the dedicated home for the *tool* itself; the broader BC/ERP context sits on [[wiki/topics/business-central-erp-implementation.md]]. [[raw/Meeting_Notes_MRP_Dashboard_Demo-June-10-2026.md]]

## What it is (architecture)

- **Built on the MSBC API.** The tool reaches into Business Central directly rather than pulling data out to Excel and pushing it back. [[wiki/people/val-levitan.md|Val]]'s rule throughout: MSBC is the single source of truth for vendors, prices, inventory and purchase orders — no Excel master file. [[raw/Meeting_Notes_MRP_Dashboard_Demo-June-10-2026.md]]
- **Plain-language / agentic interface.** You give it an item number and a quantity in ordinary language; it reads BC, sees what is on hand, computes the shortage, and recommends a purchase-order quantity. It is close to being able to **create the purchase order directly in MSBC**. [[raw/Meeting_Notes_MRP_Dashboard_Demo-June-10-2026.md]]
- **No data store of its own — it is an MCP server.** Because the tool holds no database, everything stays in MSBC, which is exactly the single-source-of-truth setup Val wants. This is the same **BC-API MCP layer** the material-requirements work rode on from May-11/May-21 (see [[wiki/topics/business-central-erp-implementation.md]]). [[raw/Meeting_Notes_MRP_Dashboard_Demo-June-10-2026.md]]
- **Dashboard first, Excel later.** Misha originally asked for the old Excel tool he was used to; Val directed Nathan to build the plain-language dashboard first and treat Excel only as a later view-only export. [[raw/Meeting_Notes_MRP_Excel_Workbook_Refinement-June-1-2026.md]] [[raw/Meeting_Notes_MRP_Dashboard_Demo-June-10-2026.md]]

## What it computes

- **Shortages and recommended POs** — for a planned quantity of an item, what is on hand, what is short, and how much to order. [[raw/Meeting_Notes_MRP_Dashboard_Demo-June-10-2026.md]]
- **Multi-level BOM explosion** — it must drill every bill of material all the way down to the **purchasable items**, not stop at an intermediate sub-assembly that shows stock on hand. In the demo a 5-level sub-assembly came back too short because the tool treated "buttons and counters" as a finished part; the fix is to keep exploding down to purchasable parts (Nathan to set it up to ~20 levels deep, though nothing at JVL goes near that — ~5 max). [[raw/Meeting_Notes_MRP_Dashboard_Demo-June-10-2026.md]]
- **Vendor pricing (program economics).** To recommend *who* to buy from and *at what cost*, the tool needs vendor names and unit prices in MSBC. In the demo, planning 10,000 units of a test item, it found the shortage but had no vendor or unit price. Vendors *are* loaded in MSBC; **pricing is missing** — roughly 800–1,000 items still need vendor prices. Some prices exist in the old **Navision** system and can be exported but need validating (nobody knows which are still current); the rest must be keyed by hand, and some items carry tiered pricing (samples, 100/300/500 units), so it is not one clean list. Once real POs are placed, their prices become history the tool can use to estimate future costs. [[raw/Meeting_Notes_MRP_Dashboard_Demo-June-10-2026.md]] [[raw/Meeting_Notes_MSBC_MRP_Report_Vendor_Pricing-June-10-2026.md]]
- **Core report columns now, more later.** The demo showed only the core columns; even that already helps with inventory (a current pain point). More columns can be added on request cheaply; computed columns — payables and Misha's PO-status/comment fields — are deferred to a later phase. The bigger value comes when Nathan builds the BOM breakdown to the lowest level. [[raw/Meeting_Notes_MSBC_MRP_Report_Vendor_Pricing-June-10-2026.md]]

## Evolution (dated thread)

- **June 1 2026 — MRP Excel workbook / dashboard pivot.** Review of the tool as a BC-API-fed Excel workbook (phased: forecast/BOM/open-POs/lead-times first, posted invoices + vendor ledger later); a June-2 follow-up pivoted the plan to **build the dashboard first and defer the Excel export**. See [[wiki/meetings/2026-06-01-mrp-excel-workbook-refinement.md]]. [[raw/Meeting_Notes_MRP_Excel_Workbook_Refinement-June-1-2026.md]]
- **June 10 2026 (AM) — dashboard demo + vendor-pricing gap.** Nathan demoed the plain-language MSBC-connected dashboard; two gaps surfaced (missing vendor/price data; multi-level BOMs not fully exploding). Compromise on the Excel question: keep MSBC as the source of truth and add a cheap **export-only** Excel view for quick sorting/filtering/printing, with all actual changes going through the tool. See [[wiki/meetings/2026-06-10-mrp-dashboard-demo.md]]. [[raw/Meeting_Notes_MRP_Dashboard_Demo-June-10-2026.md]]
- **June 10 2026 (PM) — getting the report usable for purchasing.** A follow-on (Val, Misha, Lev — Nathan not present) on getting the MRP report to the point Misha can run purchasing from it. Two things missing: vendor prices on many parts, and Misha's trust in the system. Agreed: **un-priced items get $0** (correct prices fill in organically as POs are issued, ~6-month target) rather than a guessed price; **Business Central becomes the single source of truth** with Misha moving his PO-status/comment tracking out of a parallel Excel sheet into BC; **Erica** to be onboarded on a spare BC seat for manual price entry. See [[wiki/meetings/2026-06-10-msbc-mrp-report-vendor-pricing.md]]. [[raw/Meeting_Notes_MSBC_MRP_Report_Vendor_Pricing-June-10-2026.md]]
- **Still to come:** a June-12 purchasing-workflow / RFQ session and a June-25 create-PO agent demo continue this thread. (Noted from the June-10 meetings' scheduling; those meetings not yet ingested.) [[raw/Meeting_Notes_MRP_Dashboard_Demo-June-10-2026.md]]

## Open questions

- Can MSBC hold a live vendor price list, or will prices come from purchase-order history? Nathan was unsure and noted a stored list would go stale. [[raw/Meeting_Notes_MRP_Dashboard_Demo-June-10-2026.md]]
- How Misha's per-part status tracking (PO issued, PO signed or not, shipped or not) gets represented in BC — shipping status in particular is not entered today. [[raw/Meeting_Notes_MSBC_MRP_Report_Vendor_Pricing-June-10-2026.md]]
- Whether BC will genuinely beat what Misha can do in Excel — his stated real question; he stayed skeptical (never used BC hands-on) but agreed to try. [[raw/Meeting_Notes_MSBC_MRP_Report_Vendor_Pricing-June-10-2026.md]]

## Sources
- [[raw/Meeting_Notes_MRP_Excel_Workbook_Refinement-June-1-2026.md]]
- [[raw/Meeting_Notes_MRP_Dashboard_Demo-June-10-2026.md]]
- [[raw/Meeting_Notes_MSBC_MRP_Report_Vendor_Pricing-June-10-2026.md]]
