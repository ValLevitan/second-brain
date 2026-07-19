---
type: person
title: Lev Rudky
date: 2024-01-01
aliases: [Lev Rudky, Lev, Lev Rudki, Лёва Рудки]
source-count: 8
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

## Sources

- [[raw/jvl_insights_the_aidriven_knowledge_base_draft_2_2025-03-29.md]]
- [[raw/Finance - Alka.md]]
- [[raw/ris_business_central_integration-april-3-2025.md]]
- [[raw/business_central_implementation_update-apr-17-2025.md]]
- [[raw/andrei_klimovich_update-apr-18-2025.md]]
- [[raw/business_central_update-apr-28-2025.md]]
- [[raw/action_list_review_lev_rudky-may-1-2025.md]]
- [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]
