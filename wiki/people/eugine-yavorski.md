---
type: person
title: Eugine Yavorski
date: 2025-02-18
aliases: [Eugine Yavorski, Evgeny Yavorsky, Yavorski, Yavorsky, Яворский, Evgeny Egorsky, Egorsky, Егорский, Evgeny Nevorsky, Nevorsky, Неворский, Evgeny, Yevgeny, Zhenya, Женя, Евгений]
disambiguation: "FlexPort/FlexPay integration engineer (alias Egorsky), this page. Evgeny/Zhenya cluster — EXHAUSTIVE at THREE per owner (2026-07-20; Zhenya = Evgeniy = Evgeny = Eugine, one name): [[wiki/people/eugine-yavorski.md|Eugine Yavorski]] = FlexPort/FlexPay integration software (alias Egorsky); [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] = embedded code + hardware-adjacent work (boards/redesigns/electronics, esp. Genadi Peari's projects); [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] = LGS/Omni backend (payroll "Kharetski Yauheni"; garble-aliases Koretski/Khorvatsky). Resolve by context: FlexPort/FlexPay integration software → Yavorski; embedded/hardware-adjacent & Genadi's projects → Alekseev; LGS/Omni backend → Kharetski. NO fourth Zhenya exists — a mention fitting none clearly is a mis-heard non-Zhenya (cf. Ethan/Efim), so treat as garble/mishearing and queue; NEVER create a new Zhenya."
source-count: 25
open-commitments: 3
---

# Eugine Yavorski

Eugine Yavorski (surname confirmed by Val; called "Zhenya" / "Женя" in the transcripts) is a JVL field/deployment engineer who is bringing up the **FlexPay/FlexPort** payment integration on real machines ahead of placing them at the first locations. He is based in Ontario, Canada (the transcript places him "up north," dealing with snow around Barrie/Bradford). [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]] Role somewhat unclear — he could be a JVL field engineer or an operator running the first installs; flagged.

## Role

- On the Feb 18 embedded-group standup, Evgeny is the person running FlexPay on the machine at the first-location site; work stalled because he could not start FlexPay until "Dima" delivered a new FlexPay build that ignores the card dispenser (this embedded build-delivery "Dima" is a developer — not the 3D designer, and not clearly the IT Dima; left UNRESOLVED per the owner ruling). He worked closely and near-continuously with the Minsk team last week, giving Pavel remote access to his machine. [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]
- His encoding tests matched the samples he was sent; he had assembled the pieces individually and needed at least another week to integrate everything. He is targeting placing machines at the first locations, but Val pushed him to allow two weeks (~March 5) rather than one. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]

## Embedded group — cash-out edge case (Feb 25)

- On the Feb 25 standup Evgeny ("Женя") raised the **abandoned-cash-out** case: a player presses cash-out and walks away without scanning a ticket / entering a PIN. He had put 5-minute timeouts on the start/scan/PIN steps and asked what to do about a cash-out that removes credits but is never claimed. Val's ruling: cancel the ticket as **"not claimed,"** pull the credits, report to FlexPay, and restore the money on paper via FlexPay during audit if the player returns. He is also verifying he can read a FlexPay-issued ticket and credit it, but a sensor on his device wasn't working. See [[wiki/meetings/2025-02-25-embedded-group-flexport-flexpay.md]] and [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/Embedded_Group_alignment_and_update_2025-02-25.md]]

## Embedded group — integration near-complete (Mar 4, Mar 11)

- **Mar 4:** Evgeny got the FlexPort↔FlexPay **data exchange working at a minimal level**, traced the earlier disconnect to needing to **ping with text messages**, can read a **barcode ticket**, and is adding a **watchdog** and **log file** plus **event-based** state reporting to FlexPay (all-clear / error / recovery / unclaimed-money). Still needs a validator to confirm credits land on the machine. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/Embedded_Group_alignment_and_update_2025-03-04.md]]
- **Mar 11:** He reported the integration **nearly feature-complete**, finishing **cash-out** (EGM→FlexPay), with the **firmware update** protocol still to do (~1 week; USB-stick update already works). He is merging his branch into the **main branch owned by [[wiki/people/evgeniy-alekseev.md|Zhenya Alekseev]]** (commit ~175), and planned to bring FlexPorts to the **Toronto office** to test two machines on one bus before shipping. [[raw/Embedded_Group_alignment_and_update_2025-03-11.md]]

Name confirmed by Val as **Eugine Yavorski** (the Mar 11 transcript renders it "Evgeny Yavorsky" / Евгений Яворский). He is a **distinct person** from **[[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]]**, the main-branch owner — both are colloquially "Женя"/"Zhenya," and the owner has confirmed they are two different people.

## Embedded standup (Mar 17)

- On the Mar 17 standup (reporting as "Евгений"/Zhenya), Yavorski reported one game machine passing almost all functionality **except cash-out**, with **FlexPay working** at both stations and a new printer printing tickets. He needs to cooperate with [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] on the cash-out work, and flagged that the money-transfer protocol currently runs in **one phase** but must be reworked to the **two-phase** request/confirm (reject/commit) model — he is to verify whether funds are debited at phase one. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/Flex-port-update-March-17-2025.md]] [[raw/Embedded_Group_alignment_and_update_2025-03-18.md]]

## Embedded standup (Mar 25)

- Now working **full-time** for JVL (Val: "Женя сейчас фулл-тайм работает"), which Val treats as removing the timezone excuse — he wants Yavorski to pair with the back-end "Dima" ([[wiki/people/dmitri-chudinov.md|Chudinov]]) on FlexPort **daily** (Yavorski can work 7–10am while Dima is available). The remaining FlexPort issue: **cash-out succeeds only once** per ticket (credits leave the gaming machine but don't get credited back to the ticket on repeat). Yavorski is to reproduce it right after the meeting and hand fresh logs to Dima. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/Embedded_Group_alignment_and_update_2025-03-25.md]]

## Named for the SAS mini-server (Mar 27)

- On the English scope-gap meeting Val named the staffing for the "make-do" local primitive SAS mini-server: "**Evgeniy Alexeev plus Evgeniy Yavorsky. Nobody else.**" See [[wiki/meetings/2025-03-27-flexpay-scope-gap-discovery.md]]. [[raw/flex_pay_scope_gap-mach-27-2025.md]]

## FlexPay TITO scope-gap (Mar 28)

- On the Mar-28 TITO meeting Yavorski (Евгений) was assigned the **WSS-protocol implementation** for the new TITO/SAS-server work: he agreed to read the WSS protocol over the weekend and report Monday on how long it would take, estimating **~two weeks**. He asked for a **test machine** to develop against; the plan is for Pavel to instruct the setup remotely and send him the IGT SAS-emulator utility (with "Ira" or "Vlad" helping find the RS-232 port). See [[wiki/decisions/2025-03-28-flexpay-support-tito-non-jvl-locations.md]] and [[wiki/meetings/2025-03-28-flexpay-tito-scope-gap.md]]. [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]

## SAS/TITO kickoff week (Apr 1)

- On the Apr 1 standup ([[wiki/meetings/2025-04-01-flexport-flexpay-dev-update.md]]) his plate: test **multiple devices simultaneously on the FlexPay bus** in the office ("у нас пока на шине было только один девайс"), then implement **log/system-state transfer to FlexPay on a button press**. A planned office session had slipped (the office was closed the day before); he arranged to go the same day (Gennady in the office) and asked to be shown how to do a **cash-out** on the gaming machine. His SAS/TITO test bed is an **ECHO countertop machine** that must run in **production (not demo) mode** ("иначе не будет работать"); he needs a **printer and a replacement bill validator** from Gennady (his stopped working) and identified the machine's **DB9** connector as the SAS port. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex-port_pay_dev_update-april-1-2025.md]]

## Embedded weeklies (Apr 15, Apr 22)

- **Apr 15:** on the SMIB/SAS weekly ([[wiki/meetings/2025-04-15-embedded-group-smib-sas-printer.md]]) Yavorski ("Яворский") reported finishing the **Georgia/Florida program build (version 0.15, `update.bin`)** and clarified the flashing sequence (bootloader once for production, after which the flash-drive update stops working); firmware-update-via-FlexPay targeted for end of April. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/weekly_embedded_group_flex_port_progress-apr-15-2025.md]]
- **Apr 22:** on the follow-up standup ([[wiki/meetings/2025-04-22-flexport-tito-machine-setup-debug.md]]) Yavorski (rendered "**Егорский**" this time — already established on this page as him) had joined the **PWS/WebSocket** exchange project, was porting settings from the with-screen project to run the FlexPay exchange, and had the **firmware update ~40% done** (paused to prioritise the SAS work, which "must родить something by end of April"). His test machine is a small **red countertop** with no printer (so not TITO-enabled) — he must connect a printer, Factory-Reset, scan the passport and apply an RIS file to enable TITO; Alexei Khamin/Vlad to walk him through it. [[raw/flex_port_update-apr-22-2025.md]]

## Open commitments

- [ ] Eugine Yavorski — read the FlexPay↔FlexPort **WSS protocol** over the weekend, report the effort estimate Monday, then implement the TITO extension — due Monday (report) — [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]
- [ ] Eugine Yavorski — run the multi-device FlexPay bus test in the office and implement the log/state transfer-to-FlexPay command — due week of Apr 1 2025 — [[raw/flex-port_pay_dev_update-april-1-2025.md]]
- [ ] Eugine Yavorski — send the letter describing the FlexPay protocol change (new command to mark/hold Flex Sport's "stuck"/unclaimed money) — due next day (~Nov 12) — [[raw/POS_and_PORT-schedule_review.md]]

## Apr 16 2025 — dispensing tower is the next embedded stage

On the Genadi hardware call Val named the **Flex self-dispensing tower** (on the FlexPort base) as the next stage of work for "Евгений Алексеев и Евгений Егорский" (Yavorski) after the TITO-architecture pieces. [[raw/fkex_pay_evolution-apr-16-2025.md]] See [[wiki/decisions/2025-04-16-dispensing-tower-first-magnetic-stripe.md]].

## May 7 2025 — WSS side done; day-by-day TITO milestones

On the FlexPort hardware call ([[wiki/meetings/2025-05-07-flexport-two-machines-tito-milestones.md]]) Yavorski reported the **WSS protocol finished** and that he must now integrate with [[wiki/people/evgeniy-alekseev.md|Alekseev]]'s SAS→WSS part; Val pushed him to break the remaining TITO work into **daily testable milestones** (register FlexPort→FlexPay that day; coupon-out by Thu/Fri). See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex_port_hardware_update-may-7-2025.md]]

## May 8 2025 — TITO MoneyOut bring-up

On the [[wiki/meetings/2025-05-08-flexport-flexpay-tito-standup.md|May-8 standup]] Yavorski reported connecting the full FlexPort↔FlexPay↔machine hardware chain: **WSS works on version 145** but needs the update to **154** for the latest TITO commands (Sergei Novitsky to update FlexPay); he ran [[wiki/people/evgeniy-alekseev.md|Alekseev]]'s SAS ticket-out commands, **printed and read back a ticket**, and planned today's **MoneyOut** (using a software stub first) and Friday's **MoneyIn**, before two-machine testing and handing to QA Monday. He is building a home version **155** (no dispenser). Flagged an unblockable **SAS code-51** message loop after a failed print. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex_pay_hardware_update-may-8-2025.md]] [[raw/flex_pay_port_hardware_update-may-8-2025.md]]

## May 10 2025 — weekend debug update

On a short Saturday update ([[wiki/meetings/2025-05-10-flexport-flexpay-debug-update.md]]) Yavorski reported the menu-cancel path not yet working — spoofed commands return **"ticket null, code 0"** while init/registration pass; he estimates **~90% his own side** and will inspect closely before escalating to [[wiki/people/dmitri-chudinov.md|Dima]] (Chudinov). He planned to work the office over the weekend (taking the key from [[wiki/people/evgeniy-alekseev.md|Alekseev]]), with Val telling him to email [[wiki/people/arkady-batson.md|Arkady]]/[[wiki/people/genadi-peari.md|Genadi]] to protect his workshop machines. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex-port_flex-pay_update-may-10-2025.md]]

## May 15 2025 — money-in ~80%, TITO/WSS-logging/remote-update assigned

On the May-15 FlexPay/FlexPort progress meeting ([[wiki/meetings/2025-05-15-flexpay-flexport-progress.md]]) Yavorski reported **money-in ~80%** (memory-buffer overflow on long FlexPay commands being debugged) and money-out first-round done ("very raw"); he'd send the next build to Minsk **Sun May 18** after weekend work. To May-27 he owns: polish TITO both directions, add **WSS logging** (~2–3 days), and **remote update via WSS** (target Wed May 21). Detail on [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex-pay_flex-port_update-may-15-2025.md]]

## May 20 2025 — SMIB "variant 2" build to Minsk; remote-update kickoff

On the [[wiki/meetings/2025-05-20-flexport-flexpay-smib-action-review.md|May-20 SMIB action review]] Yavorski's money-in/out was stabilized; he sends the updated **FlexPort "variant 2"** build (SAS SMIB emulation with full ticket transfer/validation + fake-data logging) to Minsk that evening (login done; log-collection command in progress). He begins the **remote firmware update** work with [[wiki/people/dmitri-chudinov.md|Chudinov]] on **May 21**, starting with the challenge of receiving a **64KB package over WSS** on the constrained board (fallback: shrink to ≤16KB). See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex-port_flex-pay_smib_update-may-20-2025.md]]

## May 29 2025 — money-in/out corrections; found 8KB update workaround

On the e-Wallet/TITO review ([[wiki/meetings/2025-05-29-ewallet-tito-flexpay-implementation.md]]; rendered "Егорский") Yavorski reported money-in/out was tested and sent to Minsk ~May 20, with corrections to apply: use the **minor-units** field (not the amount field) for credits, return the **real device number from the SAS protocol** (not a stub), and implement real command logging. On the E-Wallet update path he found the **64KB transfer hangs the receive buffer "very stably" but 8KB works safely**, driving the 64KB→8KB packet-size change (Chudinov to implement). He'll add the protocol command Sunday so Minsk can test Monday; still needs help getting firmware onto a kiosk. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/e-wallet_tito_flex-pay_flex-port_implementation_update-may-29-2025.md]]

## Nov 11 2025 — Flex Sport compatibility, log transfer, firmware-OTA, and a protocol-change letter

On the Nov-11 POS + FlexPort schedule review ([[wiki/meetings/2025-11-11-pos-flexport-schedule-review-board-update.md]]; Val, [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]], [[wiki/people/genadi-peari.md|Genadi Peari]]): Yavorski (rendered "Евгений яворской") confirmed **Flex Sport ↔ new-machine money-compatibility works** at a basic level (deposit/withdraw) — HFM-255 — with continuous-run testing and the **negative-scenario** suite (HFM-256) still to finish. His other open items: **log transfer Flex Sport → FlexPay** (a dedicated command over the **WSS** protocol) and the **firmware-over-the-air update** feature (load new firmware over the high-speed connection, verify, switch), on a tight deadline he called "жестковатый." He is preparing a letter describing a **protocol change** — a new command so FlexPay can mark and hold the "stuck"/unclaimed money Flex Sport hands over — promised for the next day. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Nov-11). [[raw/POS_and_PORT-schedule_review.md]]

On the [[wiki/meetings/2025-11-28-flexport-smib-sync-jira-review.md|Nov-28 FlexPort/SMIB sync]] Yavorski worked through HFM-255 (gaming-machine docking): the low-credit-cap **bill-return** case was resolved with Pavel into a **two-phase cashout command that does not complete phase 2** (rather than a new command/field or a cash return), which Yavorski will rework and test. He moved his block-logging task to Dec-5 and agreed to break the big docking task into subtasks. **Notable relationship dynamic:** Val told him bluntly he "can't understand what you're doing" verbally and insisted all work live as properly-statused Jira subtasks — "if it isn't in Jira, it doesn't exist" — with a weekly Monday status check. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Nov-28). [[raw/Flex-Port_Smib_alignment-November-28-2025.md]]

## Feb 5 2026 — the Flex-Port / WSS protocol owner (responsibility-split briefing)

A JIRA-sourced briefing prepared for [[wiki/people/aaron.md|Aaron]] ([[wiki/meetings/2026-02-05-flexpay-flexport-wss-responsibility-briefing.md]]) mapped the FlexPay↔FlexPort WSS responsibility split. Yavorski (named "Evgeniy Yavorski") owns the **Flex-Port** end. [[raw/Aaron_Briefing_FlexPay_FlexPort_WSS-February-5-2026.md]]

- **Primary domain:** embedded firmware on the **STM32-based Flex-Port board** inside the EGM slot machine. He **designs, defines, and implements the WSS protocol on the Flex-Port side — owning the protocol specification and message formats.** [[raw/Aaron_Briefing_FlexPay_FlexPort_WSS-February-5-2026.md]]
- **Cash-in/out:** bill-validator (**ID-003**) communication, EGM cash-out forwarding, Redeemable-vs-Playable message tagging (**HFM-338, HFM-340, HFM-343**). **Firmware/updates:** flash-stick + WSS-over-Ethernet update mechanisms, bootloader, production support tools (**HFM-215, HFM-216, HFM-279**). **Logging:** on-device logging, local transaction storage (NVS/SQLite), log transfer to Flex-Pay (**HFM-209, HFM-210, HFM-278**). **Security:** encrypted WSS + TrustZone evaluation on STM32 (**HFM-211**). **TITO:** supported at the hardware/protocol layer via **Flex-SMIB handoff** (**HFM-263**). He is **not involved server-side** (embedded-only scope). [[raw/Aaron_Briefing_FlexPay_FlexPort_WSS-February-5-2026.md]]
- **Status:** **4 items In Progress** (log transfer to Flex-Pay, bill-validator "Box Full" fix, stability testing, incremental-crediting UI) and **7 To Do** — including firmware-update support (due **2/9**), double-trigger prevention (due **2/15**), and an ID-003 wake-up investigation (due **2/24**). Flagged risk: several Feb-2026 due dates cluster together. [[raw/Aaron_Briefing_FlexPay_FlexPort_WSS-February-5-2026.md]]
- **Single-point-of-knowledge risk:** the briefing's key takeaway for Aaron is that Yavorski is **the protocol architect and embedded specialist** — if only he fully understands the WSS protocol specification, [[wiki/people/dmitri-chudinov.md|Chudinov]] and the broader team are dependent on him, which is why the ongoing knowledge transfer is called critical. [[raw/Aaron_Briefing_FlexPay_FlexPort_WSS-February-5-2026.md]]

## Feb 5 2026 — status alignment (HFM ticket walk-through)

A separate same-day ~15-min status call with [[wiki/people/val-levitan.md|Val]] and [[wiki/people/pavel.md|Pavel Frolov]] ([[wiki/meetings/2026-02-05-yavorski-status-alignment.md]]) in which Yavorski walked his open HFM tickets. (Distinct from the Aaron briefing above.) [[raw/Status_alignment-Yavorski-February-5-2026.md]]

- **HFM-346 (long-time stability testing):** he updated the production-floor devices to the latest version and wants to **extend the test ~2 weeks** — it is a continuous-run check on the production floor, not a permanent task, and he wants it to keep running after the fixes land rather than closing it. [[raw/Status_alignment-Yavorski-February-5-2026.md]]
- **A self-starting-machine bug** found after the update: on at least one machine it begins playing on its own after he loads cash — the bet jumps to \$2 and auto-play activates without a button press. Pavel and Val suspect a **shorted mechanical button** on the panel (he cannot send a command that would start a game); he will re-check on a second machine and inspect the protocol logs. [[raw/Status_alignment-Yavorski-February-5-2026.md]]
- **HFM-352 (JAS reporting) is blocked on HFM-384** (screens drawn by [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]]) — the screens did not activate correctly; Alekseev is shipping updated screens over the weekend, after which Yavorski expects to **close both 352 and 384 around Tuesday**. [[raw/Status_alignment-Yavorski-February-5-2026.md]]
- **HFM-345** was planned but never started (no activity) and was moved back to To-Do; **HFM-342** (bill-validator "box full" mask) works intermittently and was reopened for review the following week; **HFM-353** (money-front implement-logic) is **done** and to be closed, with a separate task to be opened for re-verifying the bug fixes once the new Flex version arrives. **HFM-522** is not his — Yavorski said it belongs to another engineer ("Alexey," surname unclear in the transcript). [[raw/Status_alignment-Yavorski-February-5-2026.md]]
- **FlexPort stable version for the demo:** he confirmed he posted a **stable FlexPort web version 8** for the demo Pavel needs, and reported setting up repository connections and cloud access with [[wiki/people/andrey-bosik.md|Andrey Bosik]]. [[raw/Status_alignment-Yavorski-February-5-2026.md]]

## Feb 10 2026 — Claude Code onboarding → contractor knowledge transfer

On a short session ([[wiki/meetings/2026-02-10-claude-code-yavorski-knowledge-transfer.md]], ~7m, with [[wiki/people/aaron.md|Aaron]] and Val) Yavorski reported his Claude Code attempt **built successfully but was "totally wrong"** — the AI wrote logs to the console instead of the intended destination because it "totally misunderstood our concept." His lesson: don't give a task and hope the agent understands — split into smaller tasks, control it, and review the code; working from the command line is hard because he needs to see the real code. Aaron's diagnosis was the missing **specification** ("the JIRA issue became the specification"). **Val reframed the exercise as a one-time knowledge transfer:** Yavorski is a **contractor, not a JVL employee** — JVL does not want to change how he works, it wants to **pass his knowledge in an organised format so JVL becomes the owner of the project**, compressed because "we're at the end of the project." Val vouched: "I know Eugene for decades… the most honest, the most faithful guy." Accepted plan: **Aaron clones Yavorski's repos, sets up the framework himself, and writes pull requests for Yavorski to review**, starting from the JIRA issue. See [[wiki/topics/ai-assisted-development.md]] (Feb-10). [[raw/Claude_Code-Yavorski.md]]

## Sources

- [[raw/Claude_Code-Yavorski.md]]
- [[raw/Aaron_Briefing_FlexPay_FlexPort_WSS-February-5-2026.md]]
- [[raw/Status_alignment-Yavorski-February-5-2026.md]]
- [[raw/POS_and_PORT-schedule_review.md]]
- [[raw/Flex-Port_Smib_alignment-November-28-2025.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]
- [[raw/e-wallet_tito_flex-pay_flex-port_implementation_update-may-29-2025.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-02-25.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-03-04.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-03-11.md]]
- [[raw/Flex-port-update-March-17-2025.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-03-18.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-03-25.md]]
- [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]
- [[raw/flex_pay_scope_gap-mach-27-2025.md]]
- [[raw/flex-port_pay_dev_update-april-1-2025.md]]
- [[raw/fkex_pay_evolution-apr-16-2025.md]]
- [[raw/weekly_embedded_group_flex_port_progress-apr-15-2025.md]]
- [[raw/flex_port_update-apr-22-2025.md]]
- [[raw/flex_port_hardware_update-may-7-2025.md]]
- [[raw/flex_pay_hardware_update-may-8-2025.md]]
- [[raw/flex_pay_port_hardware_update-may-8-2025.md]]
- [[raw/flex-port_flex-pay_update-may-10-2025.md]]
- [[raw/flex-pay_flex-port_update-may-15-2025.md]]
- [[raw/flex-port_flex-pay_smib_update-may-20-2025.md]]
