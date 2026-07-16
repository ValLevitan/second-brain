---
type: topic
title: Business Central ERP implementation (JVL's Dynamics 365 rollout)
date: 2025-04-17
aliases: [Business Central, BC, Dynamics 365 Business Central, D365 BC, Navision, ERP rollout, MRP, material requirements generation]
source-count: 3
open-questions: 2
---

# Business Central ERP implementation (JVL's Dynamics 365 rollout)

Microsoft **Dynamics 365 Business Central (BC)** is JVL's ERP/accounting system, rolled out company-by-company to replace the legacy **Navision** installation. Worked through in depth on an Apr 17 2025 status call between [[wiki/people/val-levitan.md|Val]] and [[wiki/people/lev-rudky.md|Lev]] (Rudky, JVL's Sr. MS Business Central MIS specialist) so Val could "put a picture together" from Lev's messages. This is the *system* side; how the finance *people* and tasks are organized sits on [[wiki/topics/jvl-finance-back-office.md]]. [[raw/business_central_implementation_update-apr-17-2025.md]]

## Status by company (Apr 17 2025)

- **JVL Mexico** — being closed ([[wiki/decisions/2025-03-24-close-jvl-mexico-operation.md]]), so it "is going to stop being an issue" and stop using BC. [[raw/business_central_implementation_update-apr-17-2025.md]]
- **JVL Systems (the US company)** — running BC in production: day-to-day accounting and **accounts receivable** work correctly, the **installment-payment "scheduler" add-on** works, and the tax program works. The company can **manufacture, sell, purchase and manage inventory** in BC — though manufacturing is set up only for **select items** so far (each item takes a large number of parameters to configure; "it's a time-consuming process… but it's not a showstopper"), and any production request can still be executed by prioritizing the missing item's setup. [[raw/business_central_implementation_update-apr-17-2025.md]]
- **JVL Labs (the Canadian company; where manufacturing currently is)** — BC implementation **on hold**; Labs still runs on **Navision**. Val's decision: **stay on Navision in Labs until it is certain where manufacturing lands** (Canada vs Georgia). [[raw/business_central_implementation_update-apr-17-2025.md]]

## The one thing not yet working in Systems

- The **purchasing scheduler** add-on is broken (a service ticket was opened). The vendor replied it would be **fixed, updated and published "this week"**; JVL then has to download and test it. The A/R (sales) scheduler already works. There are **two add-ons — one for purchasing, one for sales**. Otherwise "everything seems to be working." [[raw/business_central_implementation_update-apr-17-2025.md]]

## What implementing Labs in BC would take

- **Copy from two sources** — the BC Systems setup **plus** Navision-Labs (items/inventory are copied from Navision Labs, not Systems) — then **adapt to Canada** (taxes are "not the only thing"), and implement the **full production module including the financial side**. [[raw/business_central_implementation_update-apr-17-2025.md]]
- Separately, **reporting**, which includes **material requirements generation (MRP)**: start from a forecast ("we need to manufacture that many machines for such-and-such configurations"), then generate a report of what's required, what's in stock, what's in the pipe, and what must be ordered. This would **replace the Excel forecasting sheet [[wiki/people/mikhail-perelman.md|Michael Perelman]] uses today** (Val feeds him a forecast; he inputs part/machine numbers; it measures current stock and lists components to order). [[raw/business_central_implementation_update-apr-17-2025.md]]
- It's a large man-hour job mainly because of **bill-of-materials redundancies** — many small items across BOM levels. In Navision JVL built **exception lists** ("what not to take into account"); engineering changes / in-development parts add further complication. [[raw/business_central_implementation_update-apr-17-2025.md]]

## The licensing / single-database question (the crux)

- **Where manufacturing lands drives the design.** If manufacturing stays in Canada, Labs needs a fully-blown (expensive) manufacturing BC license; if it moves to **Georgia**, Labs "can be implemented in BC without fully-blown manufacturing" and could sit on the **same database as Systems**, cutting license count. Committing to full Canadian manufacturing and then finding it irrelevant would be "a major waste of resources." [[raw/business_central_implementation_update-apr-17-2025.md]]
- **License rule (Lev):** a company **without** manufacturing can be put on the same database as one **with** manufacturing, **but not the other way around** — the manufacturing license is "wider… with more capabilities" and a cheaper-license company won't carry it. So you can add a **cheap-license** company onto an **expensive (manufacturing) license** database, not vice versa. [[raw/business_central_implementation_update-apr-17-2025.md]]
- **The US-tax obstacle to merging:** Systems has **complex US taxation** via an add-on Lev called **"Alara"** (as transcribed) that pulls **external American data sources** state-by-state / zip-code-by-zip-code; Canadian taxation "doesn't require any add-ons." Lev's worry: putting the American tax add-on on a shared database with a Canadian company could trigger compatibility problems on Canadian sales transactions (the add-on processes only American jurisdictions). Unresolved without testing/consulting. [[raw/business_central_implementation_update-apr-17-2025.md]]
- **License cost of splitting:** each user on each system needs a license; Systems has ~**7 users** in the States, so keeping two separate license types would be roughly a **$10,000/year difference** (Canadian manufacturing licenses are pricier and carry more users) — Val's initial "couple of thousand dollars" guess was corrected upward by Lev. [[raw/business_central_implementation_update-apr-17-2025.md]]

## BC's three entity levels (Lev's explainer)

- **Tenant** — what you buy a license for (top level).
- **Environment** — one live + three test environments allowed.
- **Company** — multiple companies can live within one environment.

Two companies can share a tenant, and can be put into the **same environment** — which is where Lev has "concerns regarding finances." He believes he can find a solution but "need[s] to test… and consult." [[raw/business_central_implementation_update-apr-17-2025.md]]

## Year-end

- JVL Systems **year close is in process**; Lev hasn't reached it yet but reports "I don't think there is anything terrible." [[raw/business_central_implementation_update-apr-17-2025.md]]

## Feeding software-licensing enforcement (Apr 3 2025)

An earlier Apr-3 use of BC: it is the intended data source for **software-licensing enforcement**. After an invoice is issued in BC, [[wiki/people/lev-rudky.md|Lev]] exports the **invoice number, software version, operator name and quantity** in a form the **RIS manager** can consume (Excel export easiest given BC's tight Excel integration; a BC API preferred but deferred). BC does *not* track where software is installed — that lives in the RIS manager. See [[wiki/decisions/2025-04-03-license-software-per-operator-not-machine.md]]. [[raw/ris_business_central_integration-april-3-2025.md]]

## Open questions

- Is it possible to run the US tax add-on on a shared two-company database so it applies **only** to the American company and not the Canadian one? Lev: "Maybe it's possible but I cannot guarantee it without checking." Blocks the single-database license-saving option. [[raw/business_central_implementation_update-apr-17-2025.md]]
- How to model a software sale so the accounting-system record (item/version/MSRP/customer) is **married to the RIS config file** from the JVL system in one sale — unresolved, needs Pavel + Dima Chudinov. [[raw/business_central_update-apr-28-2025.md]]

## Apr 28 2025 — deeper status: Systems solid, Labs plan, tariffs, software sales, PO roles

A ~3-hour [[wiki/people/val-levitan.md|Val]]–[[wiki/people/lev-rudky.md|Lev]] call ([[wiki/meetings/2025-04-28-business-central-labs-tariffs-status.md]]) that ended with six named "undertakings" but "none… grew into any objectives" yet. [[raw/business_central_update-apr-28-2025.md]]

- **JVL Systems (US):** fully functioning — "we buy, we sell, we ship, we pay," even small assemblies. The one lingering bug (a payment-scheduling add-on with inconsistent number lengths) got a fix "last night," untested. Systems has only **minor customizations** (e.g. serial numbers on invoices) with **no source code and no written requirements** — Val's undertaking: **reconstruct a requirements doc from the vendor invoices/emails**, and going forward issue requirements before any customization. [[raw/business_central_update-apr-28-2025.md]]
- **JVL Mexico:** closing — licenses will not be renewed; the BC instance collapses in ~3 months. Cautionary tale: Mexico had **major customizations with no source code**, and some (multi-currency year-end reports) never worked outside local currency. [[raw/business_central_update-apr-28-2025.md]]
- **JVL Labs (Canada):** plan is to implement **without a full manufacturing module** (light/simplified), with a **normal purchasing module** (same as Systems), and to put **Labs and Systems on the same tenant**. Financial data can't be copy-pasted between companies (GL + customer/vendor/item/resource ledgers carry per-entity financial parameters); rough estimate ~1 month to get operational + ~1 month for the financial core, then loose ends/training. Manufacturing in Canada would run through [[wiki/people/arkady-batson.md|Arkady]] (as [[wiki/people/lev-rudky.md|Lev]] noted "Alec" did it in the old Navision). [[raw/business_central_update-apr-28-2025.md]]
- **Tariffs / HS codes:** the most pressing action — track HS code + country of origin per item on the vendor card; intercompany transfer at BOM+30%. Full detail on [[wiki/topics/tariffs-and-customs-compliance.md]]. [[raw/business_central_update-apr-28-2025.md]]
- **Software sales (Georgia):** JVL is setting up to sell ~**2,000 software items over ~8 months to ~50 customers** (4–6 distinct softwares, e.g. "pitch"/"DLKG"). Each software sale needs an **item number + version/approval-letter number + customer + MSRP + discount**, and must be **married to a RIS (Remote Initial Setup) config file** that comes from the JVL system while the invoice/price/customer come from the accounting system — an unsolved data-marriage problem needing [[wiki/people/pavel.md|Pavel]] and [[wiki/people/dmitri-chudinov.md|Dima Chudinov]]. [[raw/business_central_update-apr-28-2025.md]]
- **Purchase-order / sales-order role model (segregation of duties):** Val wants **[[wiki/people/hector.md|Hector]] removed from creating purchase orders** (he is the controlling arm — a PO creates a liability); **[[wiki/people/mary.md|Mary]]** creates POs for non-BOM items (e.g. GLI); **[[wiki/people/mikhail-perelman.md|Michael]]** focuses on purchasing BOM. **Sales orders** (customer-facing) → [[wiki/people/felipe-miranda.md|Felipe]], the Florida "Andrei," or [[wiki/people/juan-martinez.md|Juan Martinez]]; **purchase orders** (internal) → [[wiki/people/sebastian.md|Sebastian]], [[wiki/people/elizabeth.md|Elizabeth]]. Arkady only picks and ships; the invoice is triggered (posted, irrevocable) at shipment. Each BC user costs ~**$1,000–1,200/year**. [[raw/business_central_update-apr-28-2025.md]]

## Sources

- [[raw/business_central_implementation_update-apr-17-2025.md]]
- [[raw/ris_business_central_integration-april-3-2025.md]]
- [[raw/business_central_update-apr-28-2025.md]]
