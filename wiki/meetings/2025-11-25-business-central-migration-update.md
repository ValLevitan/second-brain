---
type: meeting
title: Business Central migration update — sandbox testing, currency conversion, inventory count, banks (Nov 25 2025)
date: 2025-11-25
aliases: [Business Central Migration Update, BC migration Nov 25, Labs BC sandbox, inventory count December, Canadian dollar conversion BC]
source-count: 1
open-commitments: 4
---

# Business Central migration update — sandbox testing, currency conversion, inventory count, banks (Nov 25 2025)

**Date:** 2025-11-25 (6:01 PM recording header) · **Duration:** 40m 28s · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/lev-rudky.md|Lev Rudky]]. Russian/English mixed.

A working call continuing the Navision → Business Central migration thread that the [[wiki/meetings/2025-11-04-finance-recurring-loans-consolidation.md|Nov-4 finance call]] made the priority and the [[wiki/meetings/2025-11-17-phasing-out-navision-continued.md|Nov-17 "Phasing out Navision" call]] began executing. Val and Lev walk the state of the **JVL Labs sandbox company in BC** and the concrete work still needed before a **January go-live**. Substance on [[wiki/topics/business-central-erp-implementation.md]] (Nov-25) and [[wiki/topics/jvl-finance-back-office.md]] (Nov-25).

**§12 corpus-wide cross-check — distinct meeting.** Ran `qmd update` and grepped the whole wiki: `raw/Business Central Migration Update.md` is cited nowhere but `log.md`, and no existing meeting page carries this Nov-25 6:01 PM Val/Lev content (sandbox testing + Canadian-dollar conversion + December inventory count + bank setup). It is separate from the Nov-4 recurring finance call, the Nov-6 "2nd path" consolidation, and the Nov-17 Navision close-out call — different date and content. Confirmed new.

Durable points (single source):

- **The BC "Labs" company is a sandbox/test company.** Lev framed the current work as building a **test company ("это как песочница")** where transactions are exercised; when the time comes to go live, JVL will **take the verified setups out of the sandbox and load them into an empty company** to start working. Val's guiding preference: **launch even if not everything is finished** ("я лучше что-то не доделаю в 1 раз"), adding anything missed in real time — "for me the most important thing is to start the system." Lev's counter-principle: **the more that is tested up front, the easier life is after the cutover**, because when error messages appear the user won't know what to do and it lands on him.
- **Customers and vendors — most stay, Canadian side is thin.** Most customers and **practically all vendors stay in the same currency**; the vendors were exported from the US company. JVL has **essentially no Canadian customers** (it will not sell to US customers directly out of Canada) and few Canadian vendors — so customers/vendors are left **open** and added **manually** if any appear. **Service-provider vendors** (utilities and the like) do need to be switched to the Canadian setup. A **"quarantine" location** is to be kept for machines arriving from Mexico, Russia or elsewhere ("this quarantine act will always exist").
- **No employee accounts, no expenses.** JVL does **not** need employee accounts in BC — employees are paid through **"DP"** (transcribed; payroll provider), not directly by the company — and there is **no "expenses" concept in Canada** and no sales people booking expansion (all of that stayed in the US operation).
- **Currency conversion is the biggest single piece of work.** The most important outcome: transactions must post in the **correct currency — Canadian dollars — not US dollars** (the sandbox currently defaults US). This is "hours, not fifteen minutes" of work: **export the data, do the conversion in a temp, load it back.** Val is allocating **[[wiki/people/anatol-strekalov.md|Anatoly]]** to do it.
- **Banks first, then test transactions; a possible direct RBC↔BC integration.** Lev wants the **bank accounts set up first** (without the AP/[ЭП] integration — just the banks), then **test bank transactions**. Val noted he is building a relationship with **RBC** ("арби с") and mentioned **"Egor Bessy"** (as transcribed) as someone with a **direct Business Central implementation** — proposing to research a **direct integration** rather than the intermediary path. (The "Egor Bessy" reference and the exact RBC integration mechanism are unclear in the transcript — recorded as stated, not resolved.)
- **Tax setup must be done now, while Alka is still engaged.** The **tax ("такс") configuration** must be built correctly and **now**, while **[[wiki/people/alka-sood.md|Alka]]** ("алко") is still working — because the new posts start in **January**, and if the bank integration, tax, or the Canadian company's accounts are set up wrong they are the hardest things to unwind and must be drawn out first.
- **December inventory count (physical) — combined with shelving.** The **physical inventory count** is a December project for **[[wiki/people/elizabeth.md|Elizabeth]]** (engineer) and **Filippe**: they receive an **Excel file listing every part**, walk the shelves, pick each part off the list and enter the counted quantity keyed to its **serial/inventory number**. Then a **back-and-forth reconciliation** against the system, analysed **by dollar and by discrepancy percentage** top-down; big discrepancies (e.g. ~100 boards) get re-counted, the rest is left as the system shows it so parts aren't lost. Inventory is at its **minimum — only ~100 machines (Flex)** — so it can go fast, though Lev warned the **reconciliation takes longer than the count**. Because parts are currently on the floor (shelving removed), JVL will **install shelves during the count** — lift from floor to shelf, **label as they go**, plan the warehouse by aisle/shelf so it can be entered into the system. The space is **~8,000 sq ft** with **low ceilings → 2 tiers instead of 3**. Track by **location (SN)**; slow-moving bulk (e.g. large plastic shipments) won't be brought into the system (handled like Barbados).
- **Role shuffle: Elizabeth loses sales, gains operations; sales successor undecided.** Elizabeth's **sales component drops off** and **operations** shift onto her (Val judged the resulting conflict "not that scary"). Who takes **sales** — **Filippe or [[wiki/people/mary.md|Mary]]** — Val has **not yet decided** ("I have to think about it").
- **Tomorrow's finance-workflow meeting.** Lev has a meeting the next day (~2 PM) with **finance people — [[wiki/people/alka-sood.md|Alka]] ("Алко") and [[wiki/people/igor-donis.md|Igor]]** — about the **workflow process**; **[[wiki/people/monica.md|Monica]]** (transcribed "Мутнея") is the one who sent the workflow tables. Val's read: Alka and Igor "don't understand any processes," so **Val wants to attend himself** and asked Lev to forward him the invite. Val also booked a **1 PM** slot with Lev to go through the migration together and wants to meet again by end of week to review results.

## Open commitments

- [ ] Anatol Strekalov — convert the sandbox company's transactions to **Canadian dollars** (export → temp → reload) — due unspecified — [[raw/Business Central Migration Update.md]]
- [ ] Lev Rudky — set up the **bank accounts** in BC (without AP integration first) and test bank transactions; research a possible **direct RBC↔BC integration** — due unspecified — [[raw/Business Central Migration Update.md]]
- [ ] Lev Rudky — build the **Canadian tax configuration** correctly before January, while Alka is still engaged — due before January go-live — [[raw/Business Central Migration Update.md]]
- [ ] Elizabeth + Filippe — run the **December physical inventory count** (Excel part list → shelf count → reconcile by dollar/percentage) while installing shelving and labelling — due December — [[raw/Business Central Migration Update.md]]

**§15.8:** clear — ERP-migration, currency-conversion, inventory-count and bank/tax-setup economics only; no per-person compensation figures.

## Sources

- [[raw/Business Central Migration Update.md]]
