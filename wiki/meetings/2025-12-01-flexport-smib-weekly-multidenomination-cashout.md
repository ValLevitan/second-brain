---
type: meeting
title: FlexPort / FlexSMIB weekly — the multi-denomination cashout / bill-return deep-dive; board ordering; test-rig tasks (Dec 1 2025)
date: 2025-12-01
aliases: [Flex-Port Flex-Smib Weekly December 1, FlexPort SMIB weekly Dec 1, multi-denomination cashout, bill-return chain, HFM 339, HFM 255, HFM 346, protocol 1003]
source-count: 1
open-commitments: 4
---

# FlexPort / FlexSMIB weekly — the multi-denomination cashout / bill-return deep-dive; board ordering; test-rig tasks (Dec 1 2025)

**Date:** 2025-12-01 (recording header 12:01PM; base name `Flex-Port Flex-Smib Weekly Planning Meeting-20251201_070139`) · **Duration:** 59m 49s · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/eugine-yavorski.md|Eugine Yavorski]] ("Евгения яворского"), [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] ("Евгений Алексеев"), [[wiki/people/genadi-peari.md|Genadi Peari]]. Russian.

Weekly FlexPort/FlexSMIB planning sync — recap the prior week and set priorities to the next Monday. Continues the [[wiki/meetings/2025-11-28-flexport-smib-sync-jira-review.md|Nov-28 sync]] (and the Nov-11/12/20 arc). Substance folds into [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Dec-1).

**§12 corpus-wide cross-check — distinct meeting.** Ran `qmd update` and grepped/read the whole wiki: `raw/Flex-Port_Flex-Smib_Weekly-December-1-2025.md` is cited on no content page. It is the **Dec-1 12:01PM** Val/Pavel/Yavorski/Alekseev/Genadi weekly — separate in date and content from the Nov-28 sync (that one resolved the bill-return in principle; this one is the detailed *how* — the per-bill multi-denomination emulation — plus board-ordering and test-rig task-setting). Confirmed new.

Durable points (single source):

- **The multi-denomination cashout / bill-return problem, worked in depth (HFM-339).** FlexPort **emulates a bill acceptor** to load a ticket's value into a gaming machine, splitting the amount into individual bills (e.g. $95 → $50 + $20 + $20 + $5) and sending them one at a time over **protocol 1003** (the DCC3 bill-acceptor protocol; FlexPort talks to the machine directly, there is no machine-level maximum-accept command). When the machine hits its credit cap it **returns** the next bill, and the emulation cannot then "un-split" a partly-loaded transaction. Resolution reached on the call: because FlexPort is emulating a bill acceptor, it must behave like one — **load bill-by-bill and confirm each bill via the 1003 status before deducting it on FlexPay**; whatever the machine rejects simply **stays on the ticket**; the screen shows a neutral "**$70 of $90 credited**" message (not an error, not "limit reached" as a hard claim). Val: this improves transparency and he likes it; the cost is one transaction becomes 5–6, and FlexPay's reporting shows a row per bill. Split into the **highest denominations** the acceptor's 1003 note-table allows (fastest). [[raw/Flex-Port_Flex-Smib_Weekly-December-1-2025.md]]
- **Process ruling — AI-generate the subtasks from the transcript.** Rather than have Yavorski hand-decompose HFM-339 and argue estimates (he floated "a week" for new screens, Val stretched the room to "4–6 weeks"), Val stopped the estimating: JVL will **feed this recording to the AI to break the feature into subtasks**, then **Pavel meets Yavorski one-on-one** to agree scope and timing. [[raw/Flex-Port_Flex-Smib_Weekly-December-1-2025.md]]
- **More cashout bugs/tasks captured.** A **double-click bug** (pressing a cash-out amount button twice fires the withdrawal twice → error) → fix by **locking the buttons / a semaphore** on the event (~1–2 days). **Box-full** simulation to verify (HFM-344 area). **HFM-344** = a spurious "**cash out $0**" screen that also mis-handles a scanned ticket — investigate why it appears (probably not needed). **HFM-345** = if the validator restarts after the gaming machine (e.g. after a software reload) the machine won't re-attach it — investigate waking the machine and re-initialising the handshake (optional/desirable). [[raw/Flex-Port_Flex-Smib_Weekly-December-1-2025.md]]
- **Long-run stability testing (HFM-346).** Yavorski to run the assembled production-floor machines **continuously** to watch for hangs — a low-effort "start it and check back" task spanning ~2–3 weeks; kept **inside the FM-191 parent** so it doesn't stretch the schedule chart. [[raw/Flex-Port_Flex-Smib_Weekly-December-1-2025.md]]
- **Board work (Alekseev, HFM-270/274/275).** Alekseev tested the cable/interface boards, found and fixed faults, sent Genadi the cable changes (3 cables need the first 4 pins reordered). Genadi to send the **Minsk shipping address and the board quantity** to order; the assembled interface boards + all sets ship to **Minsk**. Alekseev closed a stray **HFM-301** (a duplicate of HFM-271 that Val had opened Oct-29 and whose status change re-surfaced it). Next week Alekseev takes **HFM-258** (validator) and the arriving **Flex Sport** production boards — new "test production board" task created to check/connect/verify them; **HFM-268** (a Windows tool) put on **hold**. [[raw/Flex-Port_Flex-Smib_Weekly-December-1-2025.md]]
- **Dima's protocol/firmware work deferred to January.** The firmware-update and negative-scenario protocol changes that need **[[wiki/people/dmitri-chudinov.md|Dima Chudinov]]**'s FlexPay side are **pushed to January** — Dima is prioritised on **Flex-POS and the payment hub**, and Pavel does not want to pull him off for a few days on the lower-priority Flex-cabinet work; Val agreed. [[raw/Flex-Port_Flex-Smib_Weekly-December-1-2025.md]]
- **Val's "no more than 3–4 tasks" discipline.** Val insists everything planned for **next year** go to the backlog and the engineers focus only on tasks that must finish this year — "after 3 tasks you start to get confused"; keep 3–4 in progress, never more. Pavel to circulate the transcript and AI-generate the follow-up subtasks. [[raw/Flex-Port_Flex-Smib_Weekly-December-1-2025.md]]

## Open commitments

- [ ] Eugine Yavorski — rework cashout to the bill-by-bill multi-denomination model (load each denomination, confirm via 1003, deduct on FlexPay, leftover stays on the ticket, neutral "$X of $Y credited" screen); close HFM-255 docking; fix the double-click double-withdrawal (button lock/semaphore) — due ~next few days / into next week — [[raw/Flex-Port_Flex-Smib_Weekly-December-1-2025.md]]
- [ ] Pavel Frolov — AI-generate the HFM-339 subtasks from this transcript, then meet Yavorski one-on-one to agree scope and timing — due this week — [[raw/Flex-Port_Flex-Smib_Weekly-December-1-2025.md]]
- [ ] Genadi Peari — send Alekseev the Minsk shipping address and the board quantity to order (HFM-270/274/275); ship the assembled interface boards + sets to Minsk — due this week — [[raw/Flex-Port_Flex-Smib_Weekly-December-1-2025.md]]
- [ ] Evgeniy Alekseev — check/connect/verify the arriving Flex Sport production boards (new test-board task) and take HFM-258 (validator) next week — due next week — [[raw/Flex-Port_Flex-Smib_Weekly-December-1-2025.md]]

**§15.8:** clear — only device/board and machine-config content. The $95/$70/$50/$20 figures are ticket values and bill denominations; the ~$200 machine credit cap is a machine configuration; the "4–6 weeks" is a task-effort estimate — none are named-person compensation.

**Same-name note (§4).** "Евгений Алексеев / Алексеев" = [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] (embedded + board work, Genadi orbit); "Евгений яворский / борский" = [[wiki/people/eugine-yavorski.md|Eugine Yavorski]] (FlexPort/FlexPay integration software); "Дима / Дмитрий" (busy on Flex-POS + payment hub; FlexPay-side protocol) = [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (FlexPay back-end/Java). [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/genadi-peari.md|Genadi Peari]] as usual. Garbled fragments ("белый цептер"=bill acceptor, "андрейкин"=underwriting, "джанг"/"джасмин") left unresolved, not force-matched.

## Sources

- [[raw/Flex-Port_Flex-Smib_Weekly-December-1-2025.md]]
