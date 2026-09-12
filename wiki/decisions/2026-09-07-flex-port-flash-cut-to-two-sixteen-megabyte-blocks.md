---
type: decision
title: Flex-Port memory is cut from two 64 MB blocks to two 16 MB blocks — on-the-fly firmware change is kept, about 10 MB is used today, and the cut is driven by the chip now quoting $148
date: 2026-09-07
aliases: [two by sixteen megabytes, was two by sixty-four, memory cut on Flex-Port, 10 MB used, 60 percent used, $148 chip, memory price spike, A and B slots, boot and storage block]
source-count: 2
status: active
open-commitments: 0
open-questions: 0
---

# Flex-Port flash drops to two 16 MB blocks

Checked and agreed at the [[wiki/meetings/2026-09-07-sas-aft-on-flex-port-and-remote-update.md|Sept 7 2026 10:02 AM engineers' alignment]] (Russian). [[wiki/people/val-levitan.md|Val]] raised it as a risk to something he needs: "вы сейчас урезаете память, но мне нужно иметь возможность на лету менять форм[вар]" — you are cutting the memory, but I need to be able to change firmware on the fly [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].

It continues the board-flash thread opened with [[wiki/people/genadi-peari.md|Genadi Peari]] on Sept 2 2026 (see [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]]'s page) and connects directly to [[wiki/decisions/2026-09-07-remote-firmware-update-mandatory-and-taken-off-yavorsky.md]].

## The numbers, as reconciled on the call

- **The capability survives the cut.** Alekseev: "это всё останется — то есть эта функциональность есть, и она останется" [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].
- **Usage today is about 10 MB.** "у нас сейчас в сумме где-то около 10 мегабайт занимают программы, графика и всё, и я оставляю 16 мегабайт." Val misread it as additive — "10 плюс 16?" — and Alekseev corrected him: "Нет… 16 всего будет… фактически мы используем… процентов 60" — about 60 % used [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].
- **Two blocks, not one split in half.** [[wiki/people/pavel.md|Pavel Frolov]] checked: "там 2 слота, а и б… у нас 16 мегабайт[,] он делится пополам, да?" Alekseev: "не, **2 по 16**" — one block for loading and storage, the other the running one: "один, который для загрузки и хранение, а 2[-й] уже работающий." Pavel's summary, unchallenged: "**было 2 по 64… станет 2 по 16**" [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].
- **Val accepted it.** "Это разумн[о]." Alekseev's justification: "мы сильно графики добавлять не будем же ж"; Val: "на порты нет, не будем" [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].

## Why — the component price

Alekseev volunteered the reason unprompted: "по ценам нынешним… мне прислали последний прайс на этот чип, который у нас заложен — **$148**. Я там вообще охренел просто. Как это возможно?" *(the source says only "this chip, the one we have designed in"; no part number or vendor is named and none is asserted here)* [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].

He attributed the memory price spike to the AI data-centre build-out rather than to any one person — "это вот эти стройки… это не он, я так понимаю, это вот эти [OpenAI,] Amazon, Google" — after Val blamed Musk. Val then said for the record that it was a joke: "но для транскрипта это просто шутка" [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]. The wider cost pressure sits on [[wiki/topics/jvl-machine-pricing-strategy.md]].

**§15.8:** clear — component pricing only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
