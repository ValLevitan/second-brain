---
type: decision
title: MudaGoose is removed from the code entirely — screens, mode, tests and the old Payment Hub parts — and git history is the way back if it is ever needed
date: 2026-10-06
aliases: [MudaGoose removal, Mutagus removal, мутагусь, мотогусь, remove MudaGoose from code, activation protocol removed, PORT-82, git history is the fallback]
source-count: 6
status: active — Nov 18 2026: the removal stands; the new Flex IQ interface boards still need Flex IQ to set a line-switch signal at boot so plain printers work (see the Nov-18 update)
open-commitments: 1
open-questions: 0
---

# MudaGoose is removed from the code entirely

Taken by [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] at the [[wiki/meetings/2026-10-06-daily-standup-ris-georgia-branch-and-critical-error-text.md|Oct-6 Minsk stand-up]] (Russian), with the team agreeing. It carries out Val's earlier ruling that JVL does not support MudaGoose — [[wiki/decisions/2026-09-09-jvl-supports-both-dual-sas-and-single-sas-and-not-mudagoose.md]].

## What was said

- **The work.** Chudinov took PORT-82, "2 подключения с а с" (two SAS connections) and their effect on the logic. Then: "решил, я сделаю себе capolity и удаляю полностью. Экраны весь весь режим тесты, скорее всего, зацепит там пэймен хоп старый. Этот протокол активации… везде, где он упоминается. Буду вычищать." (I'll make a capability and remove it fully: screens, the whole mode, tests, probably the old Payment Hub, this activation protocol, everywhere it is mentioned.) [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- **The ruling behind it.** Pavel: "у нас уже есть решение о том, что нам не нужен он вообще да." Chudinov: "Овал же говорил, что всё нет" (Val said it is gone). [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- **It still leaks into requirements.** Irina: "У нас даже в требованиях мутагусь встречается и приходится к ладо тормозить" (it still appears in requirements and Claude has to be stopped). [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- **What if it comes back.** Pavel asked: what if in two weeks someone says some locations need it? Chudinov: then tell Claude there was MudaGoose and bring it back. Seregin suggested a backup branch. Pavel: a tag at the point where it still worked would be logical, but the server side would need work anyway. Tsymanov and Chudinov: the git history is there. [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- **Jira.** Kovalchuk offered to search Jira and remove the tasks. Pavel: Jira is not the problem; the code in GitHub is. Chudinov: in code it does not bother developers; it bothers in requirements. [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]

**Name.** The transcript says "мутагусь" / "мотогусь"; the notes write "Mutagus" and call it "the activation protocol" [[raw/Meeting_Notes_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]. The wiki's name for it is MudaGoose (the legacy payment mode), per the Sept-9 decision.

## Update, Oct 7 2026 — PORT-82 closed; the removal goes to dev and stage

At the [[wiki/meetings/2026-10-07-daily-standup-test-coverage-first-and-ai-task-numbers.md|Oct-7 Minsk stand-up]] (Russian) Chudinov: "я за вчера закрыл… порт 80 82 это что подол сас" (PORT-82, the two SAS connections). "Сейчас… уже разворачиваю на дэф на с т г. Всё, что связано с удалением матогусь. Если тепло и все пройдут закрываю" — he is deploying the MudaGoose removal to dev and stage and closes it if the tests pass ("тепло" read as "тесты" — the notes' reading). Pavel had looked at his pull requests, "у меня замечаний не было"; the Claude review was done and fixed [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]].

## Update, Nov 18 2026 — a scope gap: on the new Flex IQ interface boards the printer gets no signal, so Flex IQ must set one signal at boot; MudaGoose itself stays out

At the [[wiki/meetings/2026-11-18-daily-standup-printer-signal-gap-and-cap-142-merge.md|Nov-18 Minsk stand-up]] (Russian; Val absent) [[wiki/people/pavel.md|Pavel]] raised it after the round [[raw/Meeting_Transcript_Daily_Standup_Printer_Signal_Gap_and_CAP-142_Merge-November-18-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Printer_Signal_Gap_and_CAP-142_Merge-November-18-2026.md]]:

- **What happened.** "Вчера… В Джордж была проблема, что у них принтер не заработал на новых платах." A scope gap was found on the new interface boards for Flex IQ: the board was once redrawn for the MudaGoose mode, so that when the device is off the printer hangs straight on MudaGoose [[raw/Meeting_Transcript_Daily_Standup_Printer_Signal_Gap_and_CAP-142_Merge-November-18-2026.md]].
- **How the board works.** Wired in parallel with the printer, Flex IQ has no control over the data flow to the printer and cannot print its own receipts; wired in the break, the printer prints nothing when Flex IQ is off. So a new board revision "в выключенном состоянии просто закрачивает линии. Вход на выход" (passes input to output); when Flex IQ boots it switches the lines and drives the printer itself — tickets and receipts. "вот этого функционала у нас на… лекса ай" (Flex IQ) is missing [[raw/Meeting_Transcript_Daily_Standup_Printer_Signal_Gap_and_CAP-142_Merge-November-18-2026.md]].
- **The objection.** [[wiki/people/dmitri-chudinov.md|Chudinov]]: "у нас на него требований уже нет… А вот а гусь и всю реализацию с ним спринтерами выпили. У нас нету ни требований, ни колице. Почему оно должно работать?"; [[wiki/people/vladimir-samusenko.md|Samusenko]] said the same; [[wiki/people/irina-shishko.md|Irina]]: "Какой мутагусь вообще, откуда он вырос?" [[raw/Meeting_Transcript_Daily_Standup_Printer_Signal_Gap_and_CAP-142_Merge-November-18-2026.md]].
- **Pavel's ruling.** "забудем про мутагусь, у нас есть выпущенный интерфейсные платы в большом количестве, которые нам надо поддержать в работе с обычным принтером безмутась. Он сейчас не работает." Which MVP? "Сейчас." Nothing new to support: "нам надо просто сейчас сигнал на старте флекса IQ один сигнал выставить там в единичку. У нас порт переключится и наш принтер, который ген 2 или там эпик начнёт работать" — today the signals do not reach it "На новых платах". "Ну задача на час работы на самом деле, но придётся её вот сейчас создать и сделать" [[raw/Meeting_Transcript_Daily_Standup_Printer_Signal_Gap_and_CAP-142_Merge-November-18-2026.md]].

So the MudaGoose removal stands; the new board's line switch, made for MudaGoose, is now needed for a plain printer (Gen 2 or Epic) — **evolution**: a side effect found, not a reversal. Whether the board revision is the one the Georgia units carry is implied ("на новых платах"), not stated by name.

## Open commitments

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — create and do the task: Flex IQ sets the line-switch signal at boot so Gen 2 / Epic printers work on the new interface boards — due Nov 18 2026 ("вот сейчас создать и сделать") — [[raw/Meeting_Transcript_Daily_Standup_Printer_Signal_Gap_and_CAP-142_Merge-November-18-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Printer_Signal_Gap_and_CAP-142_Merge-November-18-2026.md]]

## History

- [x] Dmitri Chudinov — PORT-82 (two SAS connections) and remove MudaGoose from the code — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]] — *Oct 7 2026: PORT-82 closed; the removal is being deployed to dev and stage, to close if the tests pass* — [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]] — *treated as done by Nov 18 2026: Chudinov, "А вот а гусь и всю реализацию с ним спринтерами выпили" (the goose and all its printer implementation were cut out) — read as complete (**inference**; no closing date said)* — [[raw/Meeting_Transcript_Daily_Standup_Printer_Signal_Gap_and_CAP-142_Merge-November-18-2026.md]]

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Printer_Signal_Gap_and_CAP-142_Merge-November-18-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Printer_Signal_Gap_and_CAP-142_Merge-November-18-2026.md]]
