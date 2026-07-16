---
type: decision
title: TITO locations use FlexSMIB in modern machines and FlexPort in legacy machines
date: 2025-04-07
aliases: [FlexSMIB decision, FlexSMIB naming, two-device TITO architecture, SMIB vs port ruling, standalone TITO server]
source-count: 5
status: active
---

# TITO locations use FlexSMIB in modern machines and FlexPort in legacy machines

On the Apr 7 2025 meeting ([[wiki/meetings/2025-04-07-flexpay-tito-smib-port.md]]) the open "where and when to use a SMIB board" question from the Mar 27–28 scope-gap thread was settled. [[raw/flex_pay_tito_smib_port-april7-2025.md]]

## The decision

- A TITO location with a **mix of legacy and modern machines needs two machine-dedicated hardware products**: a screenless SMIB board — named **"FlexSMIB"** on this call ("do we agree we are going to call it FlexSMIB… Yes") — goes into **modern machines** (dual SAS ports), and **FlexPort** (with its screen) goes into **legacy machines**. Either device connects to a **router**, and the router to **FlexPay**. [[raw/flex_pay_tito_smib_port-april7-2025.md]]
- **Why legacy machines can't take a hidden SMIB board:** legacy machines "were never designed to supply" player-facing error messages (e.g. a failed printer), so "a board somewhere hidden inside of the machine" gives no player interface — a frontal display is mandatory there, "and I think that's the definition of port." Modern machines report their tilts through SAS, so no screen is needed. Val explicitly revised his Mar-28 takeaway: "I left last meeting thinking that you need SMIB board for the legacy machines. I'm now revising my understanding… You need a flex port." [[raw/flex_pay_tito_smib_port-april7-2025.md]]
- **The barcode/optical scanner stays in the FlexPort design** even though TITO itself needs no scanner — kept for future card-scanning uses InComm described (a card scannable at the machine/kiosk could save ~3% per transaction); Gennady's next hardware revision places the scanner higher on the bracket for focus distance; a mirror/90-degree idea was raised with a laser-eye-safety caution. [[raw/flex_pay_tito_smib_port-april7-2025.md]]
- **Future replacement path recorded:** FlexPay could later be replaced by **Flex cloud**, plus a **mobile application for the cage** (cashier) to process redemptions — the router + FlexSMIB/FlexPort layer stays either way. [[raw/flex_pay_tito_smib_port-april7-2025.md]]

## Schedule and shipment rulings on the same call

- **TITO beta from ~April 30:** "Tito solution will come within 30 days from last week… I'm expecting it April 30th" — roughly 2 weeks hard coding + 1–2 weeks testing/interoperability, four weeks total started the prior week. Pavel's earlier three-month estimate came down to 30 days ("Pavel is a miracle worker"). The TITO solution will **not** be presented at the upcoming Georgia exhibition. [[raw/flex_pay_tito_smib_port-april7-2025.md]]
- **Ship order (Val):** **4 FlexPays + 16 FlexPorts to Georgia** and **1 FlexPay + 2 FlexPorts to the Florida office** — "tomorrow we must ship"; Pavel to assume command (Serge Novitskiy, Arkady, Gennady loading terminals; hardware-team meeting 7:30 am, FlexPay recap 9 am). Georgia demo on **the 17th**: one JVL machine with FlexPort (hotel space limits), bracket adaptable to Flex S, router on hand. [[raw/flex_pay_tito_smib_port-april7-2025.md]]
- **Shipment-timing evolution (Apr 8):** on the next day's recap the plan became "**Thursday**" shipping ("This week we're shipping two devices, two FlexPay devices to Georgia and one FlexPay device to Miami office"), arriving **Monday** — in time for the demo. (Device counts as stated on each call; the Apr-7 order and the Apr-8 "two + one" phrasing differ — recorded as said.) [[raw/flex_port_recap_felipe_juan_pavel-april-8-2025.md]] [[raw/flex_pay_evolution-april-8-2025.md]]
- **Ship-split revised down (Apr 8 engineering standup):** because only ~**12 FlexPorts** exist (plus ~14–15 FlexPays), the Apr-7 "16 FlexPort to Georgia" figure came down. The concrete split ruled on the engineering standup ([[wiki/meetings/2025-04-08-flex-port-device-testing-exhibition.md]]): **8 FlexPorts + 2 FlexPays to Georgia, 2 FlexPorts + 1 FlexPay to Miami/Florida**, [[wiki/people/arkady-batson.md|Arkady]] shipping Thursday. Same-period refinement of the Apr-7 order. [[raw/flex_port_update-april-8-2025.md]]

## Apr 23 2025 — SMIB scope narrowed + a standalone TITO-server product (current state)

The Apr-23 architecture meeting ([[wiki/meetings/2025-04-23-flexport-smib-tito-architecture-evolution.md]]) refined this ruling without contradicting it: [[raw/evolution_flex_port-apr-23-2025.md]]

- **SMIB is needed only for dual-SAS machines running TITO.** "We will 100% preserve the use of the word SMIB when it is SAS and through TITO. Otherwise, SMIB is not needed" — and "only in the cases where it has two SAS ports." For a **digital/temporary-wallet** location, every machine gets a **FlexPort** (with screen + scanner) and no SMIB is used at all — "do we actually need a SMIB or is it just a flex port that does it all? Just a flex port." (Consistent with the Apr-7 rule that single-SAS legacy machines need FlexPort's screen; this adds that the *business model* also decides — a digital-wallet location is FlexPort-only regardless.) [[raw/evolution_flex_port-apr-23-2025.md]]
- **Legacy single-SAS TITO wiring confirmed:** FlexPort keeps the printer + bill acceptor (on the **ID003** protocol, transcribed "ID03"), interprets the machine's payout **pulses/coin-out**, then validates with the local TITO server and prints the ticket over an **RS232** printer port (USB reserved for logs/firmware). GLC's exclusive primary SAS port is not ridden on. [[raw/evolution_flex_port-apr-23-2025.md]]
- **New ruling — the local TITO server becomes its own standalone product.** After debating STM32/embedded vs Linux and where to house the server, the meeting ruled to **move the TITO server onto its own standalone industrial-Linux hardware, presented as a separate device called "TITO server"** — used the same way in every location (not embedded into FlexPay, not on an STM board). Pavel's reasoning: Linux is more reliable and modular than the monolithic STM firmware, the Java/Linux code is reusable, and more Linux specialists are available. Because the server is the **single point of failure for the entire location** (up to **9 FlexPort devices**), it carries a **99.5%-uptime + auto-recover** requirement on a reliable **fanless industrial board** (reject the cheap "Kopini/Kardini" amusement board; e.g. **Tatang**, NVMe + memory, ~$120) with a wired connection. Design detail on [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/evolution_flex_port-apr-23-2025.md]]

## Relation to earlier decisions

- Evolves (does not contradict) [[wiki/decisions/2025-03-28-flexpay-support-tito-non-jvl-locations.md]]: the FlexPort-as-SMIB idea splits into two products — the screenless FlexSMIB for modern machines (preserving Val's "the screen is 60% of the cost" economics) while legacy machines keep the full screened FlexPort. WSS protocol changes between SMIB and FlexPay assumed done by "Dima" (context: [[wiki/people/dmitri-chudinov.md|Chudinov]], inference). [[raw/flex_pay_tito_smib_port-april7-2025.md]]
- The Apr 2 working meeting had left display/hardware scenarios open — see [[wiki/meetings/2025-04-02-smib-flexpay-integration.md]].

## Sources

- [[raw/flex_pay_tito_smib_port-april7-2025.md]]
- [[raw/flex_port_recap_felipe_juan_pavel-april-8-2025.md]]
- [[raw/flex_pay_evolution-april-8-2025.md]]
- [[raw/flex_port_update-april-8-2025.md]]
- [[raw/evolution_flex_port-apr-23-2025.md]]
