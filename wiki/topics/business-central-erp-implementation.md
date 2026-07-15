---
type: topic
title: Business Central ERP implementation (JVL's Dynamics 365 rollout)
date: 2025-04-17
aliases: [Business Central, BC, Dynamics 365 Business Central, D365 BC, Navision, ERP rollout, MRP, material requirements generation]
source-count: 1
open-questions: 1
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

## Open questions

- Is it possible to run the US tax add-on on a shared two-company database so it applies **only** to the American company and not the Canadian one? Lev: "Maybe it's possible but I cannot guarantee it without checking." Blocks the single-database license-saving option. [[raw/business_central_implementation_update-apr-17-2025.md]]

## Sources

- [[raw/business_central_implementation_update-apr-17-2025.md]]
