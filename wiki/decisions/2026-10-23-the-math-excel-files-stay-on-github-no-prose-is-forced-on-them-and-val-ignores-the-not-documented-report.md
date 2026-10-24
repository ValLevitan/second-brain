---
type: decision
title: Efim's maths Excel files stay on GitHub (not SharePoint); no prose is forced on them while Efim works in Excel by hand; Val ignores Claude's "not documented" report for them, and excluding the folders from the scan waits (Oct 23 2026)
date: 2026-10-23
aliases: [math Excel files stay on GitHub, maths Excel workbooks, platform-math_engine-assets, math engine assets repo, асадса, Асос, RTP Excel files, reels in Excel, macro export to the game config, no forced prose for Excel, not documented report, exclude folders from the repo scan, GitHub vs SharePoint for math files]
source-count: 2
status: active
open-commitments: 0
open-questions: 3
---

# The maths Excel files stay on GitHub, and no prose is forced on them

Settled on an [[wiki/meetings/2026-10-23-math-excel-files-stay-on-github.md|18-minute call on Oct 23 2026]] (Russian) between [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/efim-podvoiski.md|Efim Podvoiski]] and [[wiki/people/andrey-bosik.md|Andrey Bosik]] [[raw/Meeting_Transcript_Math_Excel_Files_Stay_on_GitHub-October-23-2026.md]]. The Teams title names the repository as "platform-math_engine-assets"; in the speech it is "асадса" / "Асос" (read as "assets" — **inference**) [[raw/Meeting_Notes_Math_Excel_Files_Stay_on_GitHub-October-23-2026.md]].

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## The problem (Val)

- "когда мой клод смотрит на репозиторию, он видит эти большие файлы с и говорят, что они не документированы." Efim: "Они не документированы никогда." [[raw/Meeting_Transcript_Math_Excel_Files_Stay_on_GitHub-October-23-2026.md]]

## What the files are (Efim)

- **RTP workbooks.** Files "в которых рассчитывается RTP при математике"; they hold the reels and other maths settings, in Excel [[raw/Meeting_Transcript_Math_Excel_Files_Stay_on_GitHub-October-23-2026.md]].
- **A manual chain.** He changes the reels and their layout, runs a macro that exports them, puts the result into the right file, and it goes into the game config; "И вот конфига игры уже попадает в продакшн." "То есть этот процесс пока вручную." Bosik restated it — the files describe a game's reels; a macro exports a config that goes into the maths engine so it works by that game's rules — and Efim agreed [[raw/Meeting_Transcript_Math_Excel_Files_Stay_on_GitHub-October-23-2026.md]].
- **Not in the build.** The game configs already live in the maths-engine repository. This repository was kept apart "потому что он очень большой, и он непосредственно автоматически не попадает… не участвует в процессе строительства" [[raw/Meeting_Transcript_Math_Excel_Files_Stay_on_GitHub-October-23-2026.md]].
- **Loosely sorted.** Some classification was tried, "но она не не обязательно правильная"; look in the games folder, sorted by product and category [[raw/Meeting_Transcript_Math_Excel_Files_Stay_on_GitHub-October-23-2026.md]].

## Why not document them now (Efim)

- "Я не вижу простого… пути к документировать. Я не думаю, что клод сейчас справится с документацией xl файлов. Их очень много, они многие похожи." Unlike code, where linked subsystems make prose useful, he asked who would use such documentation [[raw/Meeting_Transcript_Math_Excel_Files_Stay_on_GitHub-October-23-2026.md]].
- He builds a game by changing a previous one; small changes pile up, or he combines games. Moving all of it to Python or a tool "это малореалистично. Это очень много работы." He will document when, and if, he automates this part [[raw/Meeting_Transcript_Math_Excel_Files_Stay_on_GitHub-October-23-2026.md]].

## What was decided

- **Keep the files, on GitHub.** Bosik asked whether they need keeping at all. Efim: "Нужно нужно… если она пропадет, а потом не нужно вернуться к похожей игре." Bosik weighed Microsoft SharePoint, which suits Excel files well, and chose GitHub, because it is far easier if the files are automated later. Efim agreed that this will need automating some day [[raw/Meeting_Transcript_Math_Excel_Files_Stay_on_GitHub-October-23-2026.md]]. The notes list it as Bosik's and Efim's, with Val not objecting [[raw/Meeting_Notes_Math_Excel_Files_Stay_on_GitHub-October-23-2026.md]].
- **No forced prose.** Val: prose is needed so that end-to-end tests can be built on the acceptance criteria in the requirements; later, game mechanics will be described in requirements with acceptance criteria "которые помогут делать нам тестирование математики." Bosik: this repository is part of no tests today. Val: "Я совсем не хочу быть… Дураком, который думает, что давайте через силу как то напишем прозу." [[raw/Meeting_Transcript_Math_Excel_Files_Stay_on_GitHub-October-23-2026.md]]
- **Wait for the tools.** Val: "Мы подождём, когда за нас сделает этот клод или грок, или… Опытный ай… а мы применим это потом как инструмент. Сейчас нам удобно с экселем пользоваться и всё." Efim hopes "клод просто научится работать с ним" [[raw/Meeting_Transcript_Math_Excel_Files_Stay_on_GitHub-October-23-2026.md]].
- **Ignore the report; exclusion later.** Efim asked whether these folders could be excluded from the scan. Val: "Я понимаю, что этот репорт я должен проигнорировать… А потом, когда будет время, мы наладим это." [[raw/Meeting_Transcript_Math_Excel_Files_Stay_on_GitHub-October-23-2026.md]]

## How it sits against earlier items

- **The prose standard** asks every repository for prose — [[wiki/decisions/2026-09-03-prose-standard-into-knowledge-repository.md]]. This is a named exception for one non-code repository, not a change to the standard (**inference** from the wording "через силу").
- **The maths server** was to get its own data contract on Sept 4 — [[wiki/decisions/2026-09-04-data-contracts-closed-every-repository-by-september-11.md]]. That covers the engine; these files sit outside the build.

## Open questions

- Should the Excel files move into the maths-engine repository, so its prose covers both? Bosik proposed it; Efim pointed to size and the build; not settled — [[raw/Meeting_Transcript_Math_Excel_Files_Stay_on_GitHub-October-23-2026.md]] [[raw/Meeting_Notes_Math_Excel_Files_Stay_on_GitHub-October-23-2026.md]]
- What would prose or a README for this repository contain, if anything? Bosik: "Может быть достаточно грамотного ритми… Или кладым файлы?" — [[raw/Meeting_Transcript_Math_Excel_Files_Stay_on_GitHub-October-23-2026.md]]
- When automated, will the work still be in Excel or in a new tool? Efim: "Я пока не знаю" — [[raw/Meeting_Transcript_Math_Excel_Files_Stay_on_GitHub-October-23-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_Math_Excel_Files_Stay_on_GitHub-October-23-2026.md]]
- [[raw/Meeting_Notes_Math_Excel_Files_Stay_on_GitHub-October-23-2026.md]]
