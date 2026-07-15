---
type: decision
title: License software per operator by count (per-seat / concurrent-install model), not per machine — enforced via the RIS manager fed by Business Central invoice data
date: 2025-04-03
aliases: [software licensing model, per-seat licensing, RIS license enforcement, RIS manager, InChat, software warranty, license not machine, concurrent installations]
source-count: 1
status: active
open-questions: 2
---

# License software per operator by count, not per machine

**Decision (Val, with [[wiki/people/pavel.md|Pavel]], [[wiki/people/dmitri-chudinov.md|Dima Chudinov]] and [[wiki/people/lev-rudky.md|Lev Rudky]], Apr 3 2025):** JVL will license machine **software to an operator by a count of installations** — a per-seat / concurrent-installation model — **not tie a licence to a specific machine or its hardware**. Enforcement lives in the **RIS manager** (the tool that authorises putting software on a machine), fed by **invoice data exported from Business Central**. The problem was framed in the meeting's chat under the label **"InChat"**; scope is deliberately narrowed to the **Georgia** market for the first implementation. [[raw/ris_business_central_integration-april-3-2025.md]]

The meeting is Russian and internally duplicates its own content (the same discussion is transcribed twice); facts recorded once. **RIS** here = the mechanism/file that lets JVL change/install software on a machine; each issued RIS carries its own **unique number** (distinct from the software version). See also [[wiki/people/pavel.md]] (the remote-initial-setup architect) and [[wiki/topics/business-central-erp-implementation.md]]. [[raw/ris_business_central_integration-april-3-2025.md]]

## The problem

- The existing "Software Manager" in the new RIS interface can already allow a software version **per operator**, but that doesn't limit *how many* machines an operator installs it on (an operator may have 200 machines). The goal is to stop software reaching the wrong hands / being installed beyond what was paid for. [[raw/ris_business_central_integration-april-3-2025.md]]

## The model chosen

- **The licence attaches to software, not to the machine.** Software installs on the **CPU board**, not the machine; machines change hands freely, so binding to hardware is the wrong control point. Val: "мы дали разрешение на софт, не на машину." Pavel initially argued it should be per-machine; Val and Dima ruled per-software. [[raw/ris_business_central_integration-april-3-2025.md]]
- Track **concurrent operational installations** — like a per-seat software licence (Val's analogy: Microsoft / Navision / Business Central are all "per seat," concurrent-user counts, "весь софтвер-мир идет в направлении одновременной работы"). Sell e.g. a licence for **10 installations**; the first 10 machines run, the 11th is blocked. A **de-installation** process moves a machine to a virtual **Warehouse** (non-operational), freeing its licence. [[raw/ris_business_central_integration-april-3-2025.md]]
- **Invoice = the tie between software and a specific operator.** Put the RIS number on the invoice and the invoice number on the RIS; can be done **manually** at first. Goal is to **remove human intervention** (a bad actor could favour an operator with extra installs). [[raw/ris_business_central_integration-april-3-2025.md]]

## Who does what

- **Lev Rudky** — after an invoice is issued in Business Central (a standard BC function he doesn't alter), export the invoice information — **invoice number, software version, operator name, quantity** — in a form the RIS manager can consume. Easiest path is **Excel export** (BC integrates tightly with Excel); a **BC API** would be better but is deferred ("давайте до решения дойдем потом"). BC does **not** manage where software is installed — that lives in the RIS manager. [[raw/ris_business_central_integration-april-3-2025.md]]
- **Dima Chudinov** — the RIS-manager side (consume the invoice data, enforce the count). Val named the two responsible parties explicitly: "Лёва Рудки… с одной стороны… Дима Чудинов… с другой стороны." [[raw/ris_business_central_integration-april-3-2025.md]]
- Process to follow: Val turns the recorded discussion into a **business requirement**, breaks it into **atomic/singular requirements**, assigns them, and **Pavel folds them into a sprint**. [[raw/ris_business_central_integration-april-3-2025.md]]

## Supporting business rules captured

- **Invoice = final sale; until an invoice is paid to zero, the sale is a lease and the machines are collateral JVL can repossess** (US law: ownership doesn't transfer until fully paid). When the invoice zeroes, the lease converts to a term of "some decades." A machine's dating anchor is always the **date of invoice** — there is no other legal date to monitor. [[raw/ris_business_central_integration-april-3-2025.md]]
- **Software warranty:** buying a new machine grants ~**3 months** (from invoice date) to install any software from the library; **one software warranty per machine** (10 machines = 10 warranties); the salesperson fills it in and can extend it. Example economics stated: a software version sold at ~**$3,000 each**, 10 = **$30,000**. [[raw/ris_business_central_integration-april-3-2025.md]]
- **Customer vs operator mismatch (needs a mapping):** JVL's records use "customer," not "operator"; one customer (e.g. **"Lucky Box"** in Georgia) can have many casinos, each a location/operator. Operator name and software version must match one-to-one between BC and the RIS manager; a mapping key is needed. [[raw/ris_business_central_integration-april-3-2025.md]]
- **Georgia-only for now:** Georgia is the one jurisdiction where JVL is barred from *operating*, so all Georgia COAM machines can be bound hard to invoices; the change is **moving-forward only** — no retroactive fixing of past installs. [[raw/ris_business_central_integration-april-3-2025.md]]

## Open questions

- Whether **participation** machines (Florida, Colombia) fit this invoice model — no worked-out system yet for how a participation charge/invoice is issued; in Georgia participation is impossible (operating banned). [[raw/ris_business_central_integration-april-3-2025.md]]
- Transferring machines between operators: mechanics of decrementing the old operator's licences and creating the new operator are discussed but not fully settled (the software "flash" could be copied; a new operator isn't in the system until they prove ownership via the invoice). [[raw/ris_business_central_integration-april-3-2025.md]]

## Sources

- [[raw/ris_business_central_integration-april-3-2025.md]]
