---
type: meeting
title: "Dev_environments" — the two development environments and the dependency on Pavel, the RK3568 SDK's state, the AMD spike with a ten-day clock, the RK3576 branch, and a one-minute AI PM direction check (Sept 29 2026, 10:06–10:32 AM, three segments)
date: 2026-09-29
aliases: [Dev_environments, Dev Environments Sept 29 2026, Dev Environments RK3568 SDK and Pavel Bottleneck, Dev Environments AMD SDK Spike and RK3576 Plan, Dev Environments AI PM Direction Check, Sept 29 dev environments call, two development environments, AMD SDK spike, RK3576 branch, AI PM direction check, два девелопмента, баттлнек вокруг Павла]
source-count: 6
open-commitments: 0
open-questions: 0
---

# "Dev_environments" — RK3568 SDK, the AMD spike, and the AI PM direction check (Sept 29 2026)

**Date/time:** September 29 2026 (a Tuesday), **10:06 – 10:32 AM Eastern** (about 26 minutes in three recordings: 10:06–10:20, 10:20–10:31, 10:31–10:32), from the `**Date:**` header lines [[raw/Meeting_Transcript_Dev_Environments_RK3568_SDK_and_Pavel_Bottleneck-September-29-2026.md]] [[raw/Meeting_Transcript_Dev_Environments_AMD_SDK_Spike_and_RK3576_Plan-September-29-2026.md]] [[raw/Meeting_Transcript_Dev_Environments_AI_PM_Direction_Check-September-29-2026.md]]. Teams session "Dev_environments". **Language: Russian.**

**Who spoke** (speaker labels, all three segments): [[wiki/people/val-levitan.md|Val Levitan]] (organizer; ran it), [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]] [[raw/Meeting_Transcript_Dev_Environments_RK3568_SDK_and_Pavel_Bottleneck-September-29-2026.md]].

**Purpose.** Val: "Давайте обсудим проблему" — JVL now keeps two development environments (RK and AMD), both must be easy for developers, and the environment work depends on one person; what is the state of the RK3568 SDK, can it be copied as a skeleton for AMD, who does it and by when. The last minute checked whether Pavel and Irina had doubts about the AI project manager discussed at 6:02 AM [[raw/Meeting_Transcript_Dev_Environments_RK3568_SDK_and_Pavel_Bottleneck-September-29-2026.md]] [[raw/Meeting_Transcript_Dev_Environments_AI_PM_Direction_Check-September-29-2026.md]].

**§12 — one meeting, three segments, six files.** The three recording pairs carry the same Teams session title "Dev_environments", the same three speakers, and headers "Segment 1 of 3 / 2 of 3 / 3 of 3" with back-to-back times (10:20 ends segment 1 and starts segment 2; 10:31 ends 2 and starts 3). Segment 2 opens mid-answer to the question segment 1 ends on ("Все линук сборки на базе?" → "Наверное, мы можем сейчас перестроить и AMD на базе ну Того же репозитория"), so it is one conversation; segment 3 is Val's closing question in the same call. **One stub, `source-count: 6`.** A corpus-wide grep for all six filenames, "Dev_environments", "10:06", "AMD SDK", "RK3576 branch" and "скелет" found no page citing any of them and no earlier stub for this call. The same morning's [[wiki/meetings/2026-09-29-daily-standup-firmware-reissue-and-modem-gateway.md|4:49 AM stand-up]], [[wiki/meetings/2026-09-29-ai-pm-architecture-and-second-brain-plan.md|6:02 AM "Design_AI-PM" call]] and [[wiki/meetings/2026-09-29-transactional-mvp1-setup-instructions-and-mikrotik-router.md|8:06 AM MVP 1 call]] are different meetings (other times, other attendees). New meeting.

Substance lives on:

- [[wiki/decisions/2026-09-29-the-amd-environment-is-rebuilt-from-the-rk3568-sdk-pavels-ten-day-spike-and-the-rk3576-waits.md]] — the rulings: AMD rebuilt from the RK3568 skeleton; standardise first, RK3576 after; RK and AMD separate repositories; MVP 1 = kernel, root file system, installer, bootloader; Pavel takes the spike; ten days, review on the 8th
- [[wiki/topics/nova-platform-architecture.md]] (Sept 29, 10:06 AM) — the two environments, the RK3568 SDK's state and the dependency problem, the RK3576 branch
- [[wiki/decisions/2026-09-14-the-street-cabinet-board-is-the-rk3576-not-the-rk3568.md]] — Sept-29 update: the 3576 lives as a branch in the RK3568 repo, cannot boot from SD, 95 % the same, and waits for the standardisation
- [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] — Sept-29 (10:06 AM) update: an x86 emulator exists and is good, the RK3568 one is weaker; the only useful SDK test is that the image boots in an emulator
- [[wiki/topics/test-automation-strategy.md]] (Sept 29, 10:06 AM) — how a development environment is tested: through the integration repository, inside other tasks
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Jul 20 2026, Sept-29 update) — the x86 platform SDK direction from July, now a dated spike
- [[wiki/projects/ai-project-manager-and-company-second-brain.md]] and [[wiki/decisions/2026-09-29-bosik-owns-the-ai-pm-the-meeting-bot-waits-and-the-second-brain-is-built-first.md]] — the 10:31 AM direction check: Pavel and Irina have no reservations
- People: [[wiki/people/val-levitan.md]] · [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · (named, not present) [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/andrey-bosik.md]] · [[wiki/people/evgeniy-alekseev.md]]

**§4 name calls** [[raw/Meeting_Transcript_Dev_Environments_RK3568_SDK_and_Pavel_Bottleneck-September-29-2026.md]] [[raw/Meeting_Transcript_Dev_Environments_AMD_SDK_Spike_and_RK3576_Plan-September-29-2026.md]]:

- "Павел" / "Паша" = Pavel Frolov (speaker). "Ирина" = Irina Shishko (speaker).
- "дима", who "активно… работал по автоматическому обновлению" in the platform-SDK-RK3568 repository and last "причёсывал" it to make it universal = [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]], **by context** (the Flex IQ remote-update work is his — capability 122 and the update dashboard on his page) — inference, not spoken.
- "Саша", who also worked in that repository = [[wiki/people/alexander-biratka.md|Alexander Biratka]], **by context** (the Sept-1 Flex-Pay-onto-RK3568 assignment) — inference.
- "Андрей", who made the 13 prose sections "по новой структуре" = [[wiki/people/andrey-bosik.md|Andrey Bosik]], **by context** (standards and prose rollout are his) — inference; Klimovich does not fit.
- "Алексеева" (whose written reply Irina pointed Pavel to) = [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] — surname spoken.
- Garbles read, not asserted: "дега" / "девелопментами" = development environments; "инваль" / "инваймент" / "энваймент" / "инвайть" = environment; "аккумулятор" / "стимулятор" = emulator (**inference**, as on the Sept 23–29 pages); "клод" / "клот" = Claude; "с д к" = SDK; "adi russ" = ADRs; "кейпо Билла" / "capobility" = capabilities; "дэбби" = Debian (the notes' reading; **inference**); "MD" / "а м д" = AMD; "рк 35 7 76" = RK3576. "Чтобы решается Павел кондашвиц" and "Машина i mary" — **unclear**, not interpreted.

**Where the notes and the transcript diverge** (transcript followed; notes [[raw/Meeting_Notes_Dev_Environments_RK3568_SDK_and_Pavel_Bottleneck-September-29-2026.md]] [[raw/Meeting_Notes_Dev_Environments_AMD_SDK_Spike_and_RK3576_Plan-September-29-2026.md]] [[raw/Meeting_Notes_Dev_Environments_AI_PM_Direction_Check-September-29-2026.md]]):

1. **"First made for FlexPay".** The segment-1 notes say the RK3568 repository "was first made for FlexPay". Pavel said "изначально создавался для флекс пэя. Помоему Да нет для флекса флекса" — he corrected himself from FlexPay to "Flex"; which device is **unclear**.
2. **"On Debian".** The segment-2 notes state Debian; the transcript has "На базе дэбби" — kept as the notes' reading, marked inference.
3. **"October 8".** The notes give the date in full; Val said only "Какое 8 число да? 8 числа я назначу [митинг]" — the month is by context. Ten days from Sept 29 would be the 9th; the 8th is what was said.
4. **The Alekseev reply.** The segment-1 notes say "a reply from Alexeev about 8 MB SDRAM not working". The transcript: Irina "Паша видела ответ Алексеева… Он там как раз пишет"; Pavel "То, что с драм 8 мегабайт не работает. Ноль"; Irina "663 пишет, 108 дней назад было" — what does not work, what "663" and "108 дней" refer to, are **unclear**; not interpreted and not carried to any page.
5. **Omitted by the notes:** Pavel's "Ну сейчас это только на меня можно, [ассайн]" is in the notes as "only he can take it now"; Val's "вы сказали, что у вас есть время… вы хотели взять даже работу на себя" is not — recorded on the decision page without a reason (none is spoken). Irina's "Раз раз 23 пишешь?" at the end of segment 2 is **unclear**.
6. **Segment 3** — the notes match the transcript; nothing diverges.

**§15.8:** the "bottleneck around Pavel" is recorded only as a single-point-of-dependency fact — what only he could do (the RK3568 environment at the start), what has since been spread (other developers now work in the documented repository), and who takes the AMD spike. Val's remarks about Pavel himself are not recorded; nothing about pay. **§15 #9:** no corporate identifier appears; "13 секций прозы", "95 %", "80 %", "10 дней" and "8 число" are work figures.

## Sources
- [[raw/Meeting_Notes_Dev_Environments_RK3568_SDK_and_Pavel_Bottleneck-September-29-2026.md]]
- [[raw/Meeting_Transcript_Dev_Environments_RK3568_SDK_and_Pavel_Bottleneck-September-29-2026.md]]
- [[raw/Meeting_Notes_Dev_Environments_AMD_SDK_Spike_and_RK3576_Plan-September-29-2026.md]]
- [[raw/Meeting_Transcript_Dev_Environments_AMD_SDK_Spike_and_RK3576_Plan-September-29-2026.md]]
- [[raw/Meeting_Notes_Dev_Environments_AI_PM_Direction_Check-September-29-2026.md]]
- [[raw/Meeting_Transcript_Dev_Environments_AI_PM_Direction_Check-September-29-2026.md]]
