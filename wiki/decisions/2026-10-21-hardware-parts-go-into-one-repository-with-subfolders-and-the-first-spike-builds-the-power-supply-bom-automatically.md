---
type: decision
title: Hardware parts go into one GitHub repository with subfolders, not many repositories; the first spike builds the power-supply sub-assembly BOM automatically from data contracts and GitHub Actions for Nathan to load into Business Central; Genadi does not build the BOM by hand and only discusses the logic (Val, on Andrei Bosik's proposal, Oct 21 2026)
date: 2026-10-21
aliases: [one hardware repository, one repo with subfolders, single repo for hardware parts, no separate hardware repositories, подпапки в одном репозитории, power supply BOM spike, power supply sub-assembly spike, блок питания spike, BOM instead of an ISO image, Genadi does not build the BOM by hand, no fake milestone, audit agent for parts, this transcript is the spec]
source-count: 2
status: active
open-commitments: 2
open-questions: 1
---

# Hardware parts go into one repository with subfolders; the first spike builds the power-supply BOM automatically (Oct 21 2026)

Decided by [[wiki/people/val-levitan.md|Val Levitan]] with [[wiki/people/andrey-bosik.md|Andrei Bosik]] at the [[wiki/meetings/2026-10-21-hardware-parts-single-repo-and-bom-spike.md|Oct 21 2026 call]], 10:01–10:20 AM Eastern, in Russian (only the two of them). Quotations are from the transcript [[raw/Meeting_Transcript_Hardware_Parts_Single_Repo_and_BOM_Spike-October-21-2026.md]] unless marked.

## How it came up

- **Val's question.** Val wanted to learn how a bill of materials is assembled "Из индивидуальных… Чертежей или покупных деталей". Every part — purchased-part data sheets, JVL drawings and specs — gets a data contract that lists "всех возможностей" of the part.
- **Why Val wanted many repositories.** He was copying the developers' set-up, where GitHub Actions build the ISO image ("За счёт гидакшнс у нас собирается iso имидж"). His picture: all harnesses in one repository, all monitors in another, all the metal parts Genadi designs in a third, each described properly, and a GitHub Action that assembles finished sub-assemblies.
- **Andrei's answer.** He had replied to the email only on the point "зачем нам создавать множество репозиториев" when one repository with subfolders would do. A repository is "просто абстракция уровня"; an Action can read a subfolder as easily as a separate repository. Repositories are split for things another product can reuse; here "это же одна информация". Many repositories would be hard for Genadi to work with, and parts overlap: "материнская плата блок питания и… кабеля. И это уже 3 категория". Splitting later is easy, joining is hard: "Мы можем всегда разделить гораздо сложнее соединять".
- **Tags.** Val recalled that tags were rejected for development, and "ирон был категорически против таков", but he did not remember why. Andrei: tags are "вообще другая тема" — a tag is only a pointer to a commit.

## What was decided

- **One repository with subfolders.** Val: "Я тогда считаю этот вопрос закрытым, он решённый, мы мы не делим это на на разные репозитории. Мы идём 100 архитектуры, которые вы предложили."
- **The first spike: the power supply.** Val wants "сырую такую штуку" built first — the power-supply sub-assembly from purchased parts, the metal Genadi designs, and a purchased harness with connectors, "Использую… Дельта, контракты и акшены". The output is a BOM in place of an ISO image: "вместо iso имиджа… выйдет билов материал. Этот билов материал нейтан потом берёт и… Закладывает его в бизнес централ." ("нейтан" = [[wiki/people/nathan-carver.md|Nathan Carver]]; "гена" / "Геннадий" = [[wiki/people/genadi-peari.md|Genadi Peari]].) Andrei: "Ну я уверен, что это можно будет сделать."
- **The contract also explains the function.** For example, the power supply takes incoming power and gives out 12 V and 5 V; a harness exists to carry the 5 V and 12 V out — "Иначе харнес там не нужен." That logic is part of the data contract.
- **No hand-built BOM.** Today Genadi builds it by hand in an Excel table. Val does not want that, for two reasons: to save Genadi's time, and because an automatic BOM is a key checkpoint — "Если б биоматериал правильно соберётся… значит, все… контракты правильно составлены… все детащит правильно положены". "Для меня это очень важный маилстон, который я не хочу, чтобы мы его профейкали руками." Genadi should discuss only the logic ("чтобы гена обсудил только логику"). Andrei may ask Genadi how he works today, but only to learn what not to do.
- **Claude writes the contracts.** Val: "Я считаю, что клод может сам составить", on the basis of the data sheets.
- **Val stays in.** "пожалуйста, вникайте только меня от этой темы не отодвигайте", because he does not want Andrei and Genadi to settle things without him: "Генадий сделает посвоему, он сделает хорошо, но не сделает так я хочу."
- **The spec is this transcript.** Andrei asked for a technical spec; Val: "Я веду этот транскрипт… Может даст вам техническое задание?" Andrei: "давайте попробуем из него вывести".

The notes record the same three decisions and say the one-repository ruling replaces the Oct-20 plan to settle repositories or tags by email [[raw/Meeting_Notes_Hardware_Parts_Single_Repo_and_BOM_Spike-October-21-2026.md]].

## How it sits against earlier rulings

- **Reverses the "no monorepo" ruling.** On Oct 5 Val turned down Nathan's mono-repo idea ("if we have one monorepo, then JIRA doesn't work"), and on Oct 19 he restated "Each repository is… Equal to a Project" and asked for three repositories first — [[wiki/decisions/2026-10-05-hardware-follows-the-developer-repo-model-one-jira-project-one-repo-zero-trust-data-contracts-no-monorepo.md]], [[wiki/decisions/2026-10-19-hardware-repositories-start-with-harness-display-and-sheet-metal-and-the-agent-generates-data-contracts-from-vetted-data-sheets.md]]. **Evolution:** the newer ruling is current; Nathan's folder list, the readme / Prose / data-contract set, and agent-written contracts carry over as subfolders of one repository. What this means for the matching Jira projects was not discussed.
- **Settles the Oct-20 challenge.** On Oct 20 "Andrei" objected to about fifteen repositories and suggested tags; Val said tags are bad. Here the speaker label is **Andrei Bosik** and he says he wrote the reply on repositories — so the Oct-20 "Andrei" is Bosik (by the speaker label and his own words; the Oct-20 notes had written "Andrei Klimovich").
- **Fits the BOM control gate.** It applies [[wiki/decisions/2026-10-13-the-agent-builds-the-bom-as-a-control-gate-taught-by-data-contracts-not-cad-and-genadi-finds-why-it-is-wrong.md]]: the agent's BOM is the test that the contracts and data are right.

## Open commitments

- [ ] [[wiki/people/andrey-bosik.md|Andrei Bosik]] — study the topic, take the spec from this transcript, and prepare the power-supply BOM spike — due Tue Oct 27 2026 (the next meeting; he is busy Thu–Fri with the PM agent and with autotests, helping "Женя") — [[raw/Meeting_Transcript_Hardware_Parts_Single_Repo_and_BOM_Spike-October-21-2026.md]] [[raw/Meeting_Notes_Hardware_Parts_Single_Repo_and_BOM_Spike-October-21-2026.md]]
- [ ] [[wiki/people/val-levitan.md|Val Levitan]] — book a meeting with Andrei for Tuesday at 7:00 ("Договорились на вторник на тогда на 07:00 я назначу митинг"; Andrei asked for Tuesday, not Friday) — due before Oct 27 2026 — [[raw/Meeting_Transcript_Hardware_Parts_Single_Repo_and_BOM_Spike-October-21-2026.md]] [[raw/Meeting_Notes_Hardware_Parts_Single_Repo_and_BOM_Spike-October-21-2026.md]]

## Open questions

- Who reads the data contracts Claude writes before a BOM fails? Andrei: someone must check them, "мне так кажется, что это гена"; an early error "пойдёт дальше и дальше". Val: "я бы это не читал. Я бы читал только тогда, когда у меня не собирается беломатирую"; a failed build or an audit agent that finds parts left out of every sub-assembly will show the error — [[raw/Meeting_Transcript_Hardware_Parts_Single_Repo_and_BOM_Spike-October-21-2026.md]] [[raw/Meeting_Notes_Hardware_Parts_Single_Repo_and_BOM_Spike-October-21-2026.md]]

**§15.8:** clear. **§15 #9:** clear.

## Sources

- [[raw/Meeting_Transcript_Hardware_Parts_Single_Repo_and_BOM_Spike-October-21-2026.md]]
- [[raw/Meeting_Notes_Hardware_Parts_Single_Repo_and_BOM_Spike-October-21-2026.md]]
