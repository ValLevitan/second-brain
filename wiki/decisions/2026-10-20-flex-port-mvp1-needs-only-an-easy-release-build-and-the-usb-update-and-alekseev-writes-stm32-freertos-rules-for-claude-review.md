---
type: decision
title: For Flex-Port MVP 1 only an easy, stable release build and the USB-stick update are needed — check it, put it in MVP 1 and open 10 locations; Val wants the build documented so a non-developer (or Claude) can make it without Alekseev; Alekseev writes STM32 / FreeRTOS coding rules for Claude review; no schedule until the work is split into tasks and estimated (Oct 20 2026)
date: 2026-10-20
aliases: [easy release build for MVP1, легко компилировать новый релиз, non-developer must be able to build, нон девелопер, not depend on one developer, document the system so we do not depend on you, STM32 FreeRTOS rules, best practice for Claude review, стандарт разработки STM32, double beep, двойной бип, beeper in its own thread, hard fault, HFM-663, version 0.0.84, update.bin with a different version, one branch not two, Flex POS emulator for Alekseev, release action blocks on prose and contract checks]
source-count: 6
status: active
open-commitments: 7
open-questions: 3
---

# Flex-Port MVP 1 needs only an easy release build and the USB update; Alekseev writes the rules for Claude review

Settled at the [[wiki/meetings/2026-10-20-flex-port-mvp1-usb-update-and-build-standards.md|Oct 20 2026, 7:01 AM Flex-Port firmware meeting]] (Russian, about 68 minutes) between [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]], [[wiki/people/irina-shishko.md|Irina Shishko]] and, at the end, [[wiki/people/alexei-khamin.md|Alexei Khamin]] [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]] [[raw/Meeting_Notes_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## What MVP 1 needs (Pavel)

- **The USB-stick update.** For the first release "Иметь возможность обновлять софт с юсбистика", so the ports already sent to the field do not have to be flashed with a programmer [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].
- **Every build through GitHub Actions.** "мы хотим все наши сборки делать через гидхап экшн, потому что на это завязано и процедура тестирования"; all developers then have one build and test environment [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].

## Who must be able to build (the argument)

- **Val: a non-developer.** Val understood that the GitHub Actions are made by [[wiki/people/andrey-bosik.md|Andrey Bosik]] ("Андреем босиком"), "специально нон девелопром". Pavel: "не обязательно". Val: "в нашей среде это обязательно" — the point is to make sure that someone who did not write the code can build it. Pavel: "Андрей не сможет это все покрыть." Val: that works only when the repository holds the right data contracts and prose; without them Andrei cannot build it [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].
- **Alekseev: only a developer can set it up.** "Ей может пользоваться любой… но создать этот… может только девелопы": wrong parameters in the automatic build give a wrong application, "А Кроме девелопера никто не может сделать правильной." Val: "Я в корне с этим не согласен… Не могут так компании работать" — a company cannot depend on one very clever developer [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].
- **Pavel: written once, then anyone starts it.** When the infrastructure is made, the developer writes the rule that starts the build "один раз… и дальше любой человек может придернуть сборку проекта"; this is how all JVL projects work, except server deployment. A release action can carry its own rules: it can refuse a release "если не прошли… юнитесты. Если не прошла проверка на прозу, если не прошла проверка на контракты"; QA then starts the build and picks release [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].
- **Val's request, in his words.** "Я хочу документировать так систему, чтобы в будущем мы от вас не зависели." He said this is not about hiding anything — he trusts Alekseev and knows he would come back to fix things. The aim: Claude can read the architecture and data contracts in the repository, so "в теории посторонний человек может собрать" — GitHub Actions makes the image, the image goes on a USB stick, and the stick does the update [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].
- **Alekseev's answer.** "Разработка такой документации может занять больше времени, чем разработка проекта." Val: not with Claude. Alekseev: "с колодом, может и быстрее" [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].
- **Pavel on what exists.** This project already has prose and data contracts committed. What is poorly covered is the update and the bootloader [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].
- **Not settled.** The notes list this as an open question: Val wants a non-developer to be able to build; Alekseev disagrees [[raw/Meeting_Notes_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].

## The release build — who did what

- **Alekseev:** nobody had ever made the release configuration, so the automatic build had errors only a developer could fix — "Вот то, чем я и занимался на выходные." Now "Параметры теперь всё работает", but in his view much in the project is done wrong and "очень ненадёжно будет работать" [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].
- **Pavel disagreed** ("давайте не говорить неправду"): he had sent a link showing a GitHub release build that "лёша" (Khamin) built and ran on hardware — the main application, flashed directly, without the prod loader. Everything about the update (USB and remote) was left to Alekseev on purpose: "апдейт мы оставили за вами"; "это уже 2 неделю с вами пытаемся переписываться". Irina: because the team did not get these changes from him, it could build and run only that piece. Alekseev: "То об этом было бы хорошо сказать. Раньше." [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]]
- **Where his work is.** Not in main — Irina: Khamin found no commits in main. It is in his branch **HFM-663**, version **0.0.84** [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]] [[raw/Meeting_Notes_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].

## Code quality, and the rules for Claude review

- **Alekseev's report.** He has not worked on this code for a year. Many later additions break the rules of multithreaded systems; "структура практически сломана". He had Claude make a table to show it; there are "штук, шестьсемь" such rules and almost all were found broken. His example: the double beep — different beeps need "отдельный потом", working by events or queues, "никак не напрямую вызываться из одного потока в другой" [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].
- **Irina:** "это неправильно" leads nowhere; go through the code and say what is wrong and how to do it, or leave it, release, and fix in MVP 2 [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].
- **Pavel: the old code has the same problems.** The team took the project Alekseev wrote, which [[wiki/people/eugine-yavorski.md|Eugine Yavorski]] then continued, and kept its style. Pavel ran the same Claude report on Yavorski's last branch: "там все те же самые замечания есть. Их меньше" [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].
- **The rules become a standard.** Pavel: write these rules into a development standard "ст м 32 проектов, которые используют… freetos", so that even when Claude programs, it follows them. Alekseev: "Да, Я согласен." Later: "Давайте сначала правило напишем." The notes record it as agreed by Pavel and Alekseev, with Val [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]] [[raw/Meeting_Notes_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].
- **Rules vs contracts.** Val asked whether these rules are data contracts. Pavel: no — "Правила, по сути построения… бест практис написания". Val: architecture? Alekseev: "в некоторой степени". Val: rules, architecture "и стандарты разработки" for this processor. Val also said much of this is already written for Claude; Pavel: Claude will produce such rules in three to five minutes; Alekseev: that would be general, not concrete [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].

## The scope call (Val)

- **No schedule yet.** Pavel expects the code-quality rework to go to "MVP 2 Как минимум". Val: nothing can be scheduled while there are no tasks — take this transcript, split it into tasks, see which standards apply, hear from Alekseev how long each task takes, "И тогда будем знать, что нам надо делать сейчас". Pavel gives Alekseev the task descriptions [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].
- **MVP 1 is the easy build only.** Alekseev wanted at least a visual pass for MVP 1 to remove obvious inconsistencies, "тем же звуком". Val: "для MP один я бы сделал только то, чтоб нам легко было компилировать новый релиз." Alekseev: "Ну это уже сделано." Val: "давайте это проверим и имплементируем и включим это в MVP"; "нам нужно открыть 10 лакейшинов и начинать их тестировать обязательно"; only after that develop further [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]]. The notes record it as Val's decision [[raw/Meeting_Notes_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].

## The test after Val left

- **The hard fault.** Alekseev: his application falls into a hard fault in the main loop, "при любом раскладе". To reach the "scan your ticket" screen for testing without a machine, his build uses a define that turns off the WS protocol and comments out the functions called in the loop. Pavel suggested letting Claude Code debug it [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].
- **How the USB update is tested.** Flash the loader file first, then insert a stick; better two sticks with different versions, to check the bootloader too. Khamin: the prod loader is the factory firmware [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].
- **Khamin's result.** He built from the branch on the spot. The first time the terminal did not react to the stick; the second time it went through to "remove flash drive". After the stick is removed the terminal goes to the main application and "тут же начинают пищать" with a warning about scanning a ticket, and keeps beeping. So he cannot go on to check the bootloader yet [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].
- **Debug vs release.** Khamin: the GitHub action always builds the loader and bootloader as release. Alekseev: they are the same in debug and release, so a debug build of the main application is enough [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].
- **Next steps.** Khamin builds a second update.bin with a different version through GitHub Actions, without code changes, and tests the update of the main application and of the bootloader. Alekseev will remove the define, and finds and fixes the hard fault. Pavel wants the define gone and the problem fixed before anything goes into main [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].
- **One branch, not two.** Irina asked whether the update could go in one branch and the beeping be left for later in another. Alekseev: "Значит всё в одной ветке" — the hard fault must be fixed and "как минимум… бипер вынести там в отдельный поток" [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].
- **A Jira ticket first.** Alekseev: "мне нужна… жира… Потому что вал требует на любой… Задачу" [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]].
- **The Flex IQ emulator.** Pavel will give Alekseev access to the Flex IQ (Flex POS) emulator. Remote update is not ready; when "дима" is back from vacation next week, the next task is remote update, with Flex IQ providing an API and a new emulator version [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]]. ("дима" = [[wiki/people/dmitri-chudinov.md|Chudinov]] — **inference**.)

## How it sits against earlier items

- **The MVP 1 gate.** The [[wiki/meetings/2026-10-20-daily-standup-io-board-firmware-via-github-and-vp9-video-decode.md|same morning's stand-up]] said MVP 1 counts as released only when the Flex-Port updates by USB stick. Val's ruling here keeps that gate and adds the easy GitHub release build to it — **consistent**. Detail: [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Oct-20 7:01 AM update).
- **The code belongs to the project.** Val's "not depend on one developer" repeats [[wiki/decisions/2026-09-14-main-branch-must-always-build-and-the-code-belongs-to-the-project.md]] (link drawn here — **inference**). On Sept 14 Bosik was to walk Alekseev through the standards — [[wiki/decisions/2026-09-14-alekseev-is-walked-through-the-standards-by-bosik-not-ordered.md]].
- **Later the same morning** Val came back to this at the [[wiki/meetings/2026-10-20-third-party-egm-bv-emulation-mode-and-sas-data.md|8:31 AM call]]: only "production-ready" release is needed; Khamin writes the story for Alekseev; release on a Wednesday — [[wiki/decisions/2026-10-20-machines-without-working-aft-connect-by-bill-validator-emulation-and-pulses-in-mvp1-and-the-port-mode-is-set-per-port.md]].

## Open commitments

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — split this meeting's transcript into tasks and give Alekseev the task descriptions — due unspecified — [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]] [[raw/Meeting_Notes_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]]
- [ ] [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] — write the STM32 / FreeRTOS coding rules as a development standard that Claude review uses — due unspecified — [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]] [[raw/Meeting_Notes_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]]
- [ ] [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] — estimate each task once the tasks exist — due after Pavel's split — [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]]
- [ ] [[wiki/people/alexei-khamin.md|Alexei Khamin]] — build a second update.bin with a different version from branch HFM-663 through GitHub Actions and test the USB update of the main application and of the bootloader — due unspecified (MVP 1 blocker) — [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]] [[raw/Meeting_Notes_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]] — *Oct 21 2026: Khamin tested a build from Alekseev's branch and replied to him; not said to be this test — left open* — [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]]
- [ ] [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] — find and fix the hard fault in the main loop, move the beeper to its own thread and remove the test define, all in the same branch — due unspecified — [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]] [[raw/Meeting_Notes_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — create the Jira ticket for Alekseev's hard-fault work — due unspecified — [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — give Alekseev access to the Flex IQ (Flex POS) emulator — due unspecified — [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]] [[raw/Meeting_Notes_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]]

## Open questions

- Can someone other than Alekseev — a non-developer, or Claude — build and release the Flex-Port firmware? Val says it must be so; Alekseev says only a developer can set the build up — [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]] [[raw/Meeting_Notes_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]]
- Where does the hard fault in the main loop come from? — [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]]
- Why does the application beep all the time after the USB update? Alekseev said he does not know — [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]]

**§15.8:** clear — no pay figure or rate recorded. **§15 #9:** none.

## Note, Oct 21 2026

At the [[wiki/meetings/2026-10-21-daily-standup-flex-port-mode-switch-and-sas-crc-fix.md|Oct-21 Minsk stand-up]] (Russian) [[wiki/people/alexei-khamin.md|Khamin]] said he tested the Flex-Port build Alekseev sent from his branch and replied to him [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]]. Whether this is the second-update.bin and bootloader test in the commitment above is not said, so it stays open. Pavel also said the kiosk-to-port mode command will not wait for Alekseev — [[wiki/decisions/2026-10-20-machines-without-working-aft-connect-by-bill-validator-emulation-and-pulses-in-mvp1-and-the-port-mode-is-set-per-port.md]] (Oct-21 update) [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]].

## Note, Oct 22 2026 — standards in a repository; not readable

At an [[wiki/meetings/2026-10-22-pavel-frolov-code-standards-and-knowledge-repo.md|Oct-22 11:03 AM call]] Val and Pavel spoke about reliable code and standards. Only terms can be read: Pavel's "Alekseev", "Kovalchuk reliable code. Standard.", "Best practices", "The repository knowledge is standards"; Val's "A repository in a cloud code" and "yes, just do it" [[raw/Meeting_Transcript_Pavel_Frolov_Code_Standards_and_Knowledge_Repo-October-22-2026.md]] [[raw/Meeting_Notes_Pavel_Frolov_Code_Standards_and_Knowledge_Repo-October-22-2026.md]]. That this continues the coding-rules item above is an **inference**; no commitment here is discharged.

## Sources

- [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]]
- [[raw/Meeting_Notes_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]]
- [[raw/Meeting_Notes_Pavel_Frolov_Code_Standards_and_Knowledge_Repo-October-22-2026.md]]
- [[raw/Meeting_Transcript_Pavel_Frolov_Code_Standards_and_Knowledge_Repo-October-22-2026.md]]
