---
type: person
title: Lev Rudky
date: 2024-01-01
aliases: [Lev Rudky, Lev, Lev Rudki, Лёва Рудки]
source-count: 16
---

# Lev Rudky

Lev Rudky appears in the **JVL Insights** knowledge-base proposal (~2023–24) as a JVL **employee**, titled **Sr. Microsoft Business Central MIS Specialist** — scoped to integrate JVL Insights with Business Central, implement its reporting/analytics, and oversee data synchronization. (Consistent with JVL running its accounting on MS Business Central — see [[wiki/organizations/jvl.md]].) Compensation details in the source are withheld (§15.8). See [[wiki/projects/jvl-insights-knowledge-base.md]]. [[raw/jvl_insights_the_aidriven_knowledge_base_draft_2_2025-03-29.md]]

- **Feb 2025 (date inferred):** he is the gatekeeper for finance-system access — [[wiki/people/alka-sood.md|Alka Sood]] asked Val to "accelerate him to get me access to things on the system so I can get the sales tax done," and Val agreed to communicate Chris's access needs to "Lev" (context match to this Lev: system access at JVL; recorded as an inference). [[raw/Finance - Alka.md]]

- **Apr 3 2025 — the Business Central export side of software licensing:** on the RIS ↔ Business Central licensing meeting ([[wiki/meetings/2025-04-03-ris-business-central-licensing.md]]) Val named Lev ("Лёва Рудки") as one of the two responsible parties (with [[wiki/people/dmitri-chudinov.md|Dima Chudinov]] on the RIS side). Lev's function: after an invoice is issued in BC (a standard function he doesn't alter), **export the invoice number, software version, operator name and quantity** in a form the RIS manager can consume — Excel export easiest given BC's tight Excel integration; a BC API would be better but is deferred. See [[wiki/decisions/2025-04-03-license-software-per-operator-not-machine.md]]. [[raw/ris_business_central_integration-april-3-2025.md]]
- **Apr 17 2025 — Business Central owner:** Lev is JVL's day-to-day owner of the **Business Central** ERP rollout. On a ~38-min status call he walked Val through the state of BC across the companies, the broken purchasing scheduler, what implementing JVL Labs would take, and the single-database license question (the manufacturing-vs-cheap-license rule, the US "Alara" tax add-on obstacle, tenant/environment/company levels). Full detail on [[wiki/topics/business-central-erp-implementation.md]]. [[raw/business_central_implementation_update-apr-17-2025.md]]
- **Apr 18 2025 — US-sale invoicing:** in the invoice pipeline [[wiki/people/andrei-klimovich.md|Klimovich]] set up, **US-origin** machine sales go to Lev (he creates the invoice, calculating per-state sales tax) until BC is fully installed and Klimovich can enter invoices directly — a matter of "months." Canada-origin sales route to [[wiki/people/arkady-batson.md|Arkady]] instead. [[raw/andrei_klimovich_update-apr-18-2025.md]]

## Apr 28 2025 — deeper Business Central status (Systems / Labs / tariffs)

On a ~3-hour BC status call ([[wiki/meetings/2025-04-28-business-central-labs-tariffs-status.md]]) Lev walked Val through Systems (fully functioning, minor undocumented customizations), the Mexico shutdown, the plan to implement **JVL Labs with a light manufacturing module on a shared tenant**, the **HS-code/tariff tracking** to add to the vendor card (made his #1 priority), the software-sale/RIS data-marriage problem, and the purchase-order/sales-order role model. Detail on [[wiki/topics/business-central-erp-implementation.md]] and [[wiki/topics/tariffs-and-customs-compliance.md]]. [[raw/business_central_update-apr-28-2025.md]]

## May 1 2025 — action-list review (HS codes, software sales, Val's BC license)

On the [[wiki/meetings/2025-05-01-action-list-review-lev-rudky.md|May-1 review]] of the 6-point action list he had emailed Val, Lev reported HS codes now assigned to every purchased component in Navision (country-of-origin the missing field), owed an **Excel HS report (by vendor/part/HS code) for China & Korea imports by the evening of May 2**, and took the setup of Val's own **full Business Central license** (demo booked May 15, 1 pm). Point #3 (software sales) goes to a **May 8, 7 am** meeting with Pavel + Dima Chudinov; point #4 (segregation of duties) to a series with Alka; and Val told him to start preparing an **accelerated JVL Labs → BC conversion**. Detail on [[wiki/topics/tariffs-and-customs-compliance.md]] and [[wiki/topics/business-central-erp-implementation.md]]. [[raw/action_list_review_lev_rudky-may-1-2025.md]]

## June 26 2025 — Business Central for the Georgia manufacturing move

On the [[wiki/meetings/2025-06-26-procurement-manufacturing-transfer-alignment.md|manufacturing-transfer alignment]] Lev owns the BC side of moving assembly to Georgia ([[wiki/decisions/2025-06-24-move-manufacturing-from-canada-to-georgia.md]]): **no manufacturing module**, assembly **from purchase-level components** on the JVL Systems BC, redefining purchase items as assembly/BOM items and porting the BOM from Navision (flagging the zero-quantity-placeholder migration wrinkle). He needs the **GL/chart of accounts** done first (meeting with [[wiki/people/alka-sood.md|Alka]] this week), then the **general posting setup** — JVL's call, not the subcontractor's. He sized it **"medium"/~3 weeks–1 month**; JVL Labs stays on Navision. Detail on [[wiki/topics/business-central-erp-implementation.md]]. [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]

## Nov 25 2025 — the Labs BC sandbox before January go-live

On the [[wiki/meetings/2025-11-25-business-central-migration-update.md|Nov-25 BC migration call]] Lev walked Val through the state of the **JVL Labs sandbox company** in Business Central and the tasks left before a **January go-live**: the Canadian-dollar currency conversion (assigned to [[wiki/people/anatol-strekalov.md|Anatoly]]), which customers/vendors carry over, standing up the **bank accounts first** (and a possible direct RBC↔BC integration), the Canadian **tax setup** (must be built while [[wiki/people/alka-sood.md|Alka]] is still engaged), and the **December physical inventory count** ([[wiki/people/elizabeth.md|Elizabeth]] + Filippe). Lev's principle: test as much as possible in the sandbox so fewer post-cutover error messages land on him. Detail on [[wiki/topics/business-central-erp-implementation.md]] (Nov-25). [[raw/Business Central Migration Update.md]]

## Nov 28 2025 — transaction classification, Global dimensions, January-start config

On the [[wiki/meetings/2025-11-28-business-central-financial-classification-dimensions.md|Nov-28 BC session]] (source is an AI summary, not a transcript) Lev diagnosed the BC dashboard's wrong figures as **intercompany/open-document translation errors + incorrect-or-missing Global dimensions**, and set the division of labour: **Lev teaches [[wiki/people/igor-donis.md|Igor]]** how to correct transactions and verify them (a recurring finance task Igor owns), **tests the settings in the sandbox first**, and owes the **tax + bank-account config** and **chart-of-accounts formatting** before the January start. [[wiki/people/alka-sood.md|Alka]] is to do report-based QC only (no edit rights). Detail on [[wiki/topics/business-central-erp-implementation.md]] (Nov-28). [[raw/BC-JVL_Labs-November-28-2025.md]]

## Apr 14 2026 — native AR statements out of Business Central

On the brief [[wiki/meetings/2026-04-14-accounts-receivables-ga-coam.md|Accounts Receivables GA-COAM]] wrap-up ([[wiki/people/val-levitan.md|Val]], [[wiki/people/felipe-miranda.md|Felipe]], [[wiki/people/laura.md|Laura]]) Val assigned Lev two things: work hand-in-hand with Laura to extract **native statements of account directly from Business Central** for the GA-COAM customers, and ensure those native BC statements can be **emailed directly to customers from within BC itself** (no manual export/attach step). Substance on [[wiki/topics/jvl-finance-back-office.md]] (Apr 14 2026). [[raw/Meeting_Transcript_accounts_receivables_GA-COAM-April-14-2026.md]] [[raw/Meeting_Notes_accounts_receivables_GA-COAM-April-14-2026.md]]

## Apr 15 2026 — progress payments live; payment-terms cleanup; sales-rep access

On the two-segment [[wiki/meetings/2026-04-15-bc-progress-payments-payment-terms.md|Apr-15 progress-payments call]] with [[wiki/people/val-levitan.md|Val]], Lev confirmed the AP Commerce **Progress Payment** add-on has been working since ~mid-March (an unsubscribe/resubscribe fixed it) — clarifying and apologizing for the Apr-14 impression that it still didn't work. Lev is to **clean up the old/inconsistently-named payment terms** (keeping only the new correctly-configured ones), **fix the 60-vs-90-day grace-period calc error**, and continue working the (still-broken) **sales-rep data-segregation** via permission sets + security filters. He explained the progress- (event-driven, A/P) vs installment- (time-driven, A/R) payment distinction and that each purchase-payment event posts a purchase invoice to the vendor/GL ledgers. Detail on [[wiki/topics/business-central-erp-implementation.md]] (Apr-15). **§15.8:** clear. [[raw/Meeting_Transcript_Lev_Rudky_BC_progress_payments_payment_terms-1-April-15-2026.md]] [[raw/Meeting_Transcript_Lev_Rudky_BC_progress_payments_payment_terms-2-April-15-2026.md]] [[raw/Meeting_Notes_Lev_Rudky_BC_progress_payments_payment_terms-April-15-2026.md]]

## Sept 30 2026 — the GitHub-to-MSBC meeting: a part number in BC needs more than engineering data

On the [[wiki/meetings/2026-09-30-github-to-msbc-bom-flat-list-bridge.md|Sept-30 10:00 AM GitHub_to_MSBC_BOM_Integration meeting]] (English; with [[wiki/people/val-levitan.md|Val]], [[wiki/people/genadi-peari.md|Genadi]] and [[wiki/people/nathan-carver.md|Nathan Carver]]) Lev spoke once, late, and made the one accounting point of the meeting [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]]:

- "If the source of a new part number. He is in Github. And it automatically gets created in BC afterwards. So you need to populate there more than engineering parameters in order to create a part number. in BC. It's all kinds of BC classifications associated with the part number, which has nothing to do with engineering. It's various posting groups, things like that, dimensions." Hence "Two sources of input. for a specific new part number" — engineers and somebody else.
- He kept it to the item itself, not vendors: "talking strictly about part number as a stand-alone entity… when Genadi creates… a new part number in Msbc, he enters additional information that is not strictly engineering information. Things like Dimensions. Type of inventory in simple language… if there is, for example, a new unit of measure for some part, it has to be initialized in the system and has to be accommodated during transfer as well."
- His verdict: "it's probably a good idea to experiment with to see how this concept works, because there are… some unanswered questions there. I understand it on high level, but in terms of getting into practical implementation. There might be issues."

Val released him and Nathan before the end ("I'm just burning their hours"). Recorded on [[wiki/decisions/2026-09-30-a-new-part-number-is-assigned-by-claude-from-the-standard-in-github-and-pushed-to-msbc-once.md]] and [[wiki/topics/business-central-erp-implementation.md]] (Sept 30). **§15.8:** clear.

## Sources

- [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]]
- [[raw/Meeting_Transcript_Lev_Rudky_BC_progress_payments_payment_terms-1-April-15-2026.md]]
- [[raw/Meeting_Transcript_Lev_Rudky_BC_progress_payments_payment_terms-2-April-15-2026.md]]
- [[raw/Meeting_Notes_Lev_Rudky_BC_progress_payments_payment_terms-April-15-2026.md]]
- [[raw/Meeting_Transcript_accounts_receivables_GA-COAM-April-14-2026.md]]
- [[raw/Meeting_Notes_accounts_receivables_GA-COAM-April-14-2026.md]]
- [[raw/jvl_insights_the_aidriven_knowledge_base_draft_2_2025-03-29.md]]
- [[raw/Finance - Alka.md]]
- [[raw/ris_business_central_integration-april-3-2025.md]]
- [[raw/business_central_implementation_update-apr-17-2025.md]]
- [[raw/andrei_klimovich_update-apr-18-2025.md]]
- [[raw/business_central_update-apr-28-2025.md]]
- [[raw/action_list_review_lev_rudky-may-1-2025.md]]
- [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]
- [[raw/Business Central Migration Update.md]]
- [[raw/BC-JVL_Labs-November-28-2025.md]]
