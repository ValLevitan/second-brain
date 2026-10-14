---
type: decision
title: MudaGoose is removed from the code entirely — screens, mode, tests and the old Payment Hub parts — and git history is the way back if it is ever needed
date: 2026-10-06
aliases: [MudaGoose removal, Mutagus removal, мутагусь, мотогусь, remove MudaGoose from code, activation protocol removed, PORT-82, git history is the fallback]
source-count: 4
status: active
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

## Open commitments

- [ ] Dmitri Chudinov — PORT-82 (two SAS connections) and remove MudaGoose from the code — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]] — *Oct 7 2026: PORT-82 closed; the removal is being deployed to dev and stage, to close if the tests pass — still open* — [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]
