---
type: decision
title: October 15 replaces October 1 as the working MVP 1 date — Val asks for the final state by then "if possible", while the autotest estimate runs to October 23
date: 2026-09-28
aliases: [October 15 MVP1, MVP1 moves to October 15, сдвигаем на 15 октября, 15 число это реальная дата, final state October 15, 95 percent is fine, autotests until October 23, trial batch of ten locations, пробную партию 10]
source-count: 5
status: active
open-commitments: 2
open-questions: 1
---

# October 15 replaces October 1 as the working MVP 1 date

Reached at the [[wiki/meetings/2026-09-28-transactional-mvp1-remote-updates-and-october-15-target.md|Sept-28 8:02 AM MVP 1 call]] (Russian). No one said "the date is changed" in one sentence. The three people who set the date all spoke to October 15, and no one argued for October 1 [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]].

## What was said

- **Pavel** named the new date first, while arguing for remote Flex-Port update: "Мы MVP один, например, сдвигаем на 15 октября. Да, наверное, можем постараться сделать и обновление флекспортов к этой дате" [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]].
- **[[wiki/people/andrei-klimovich.md|Klimovich]]** — who had held October 1 on Sept 24 — now said: "будем честны, что у нас 15 число. Это реальная дата[;] 1 октября… [н]ереализуемо" [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]].
- **[[wiki/people/val-levitan.md|Val]]** set the goal at the end: "просьба коллективу[:] провести авто тесты и сделать final [st]ate 15 октября, если это возможно." Then: "если 95% будет закончено[,] [н]ормально" [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]].

## The autotest estimate runs past it

- **October 23.** [[wiki/people/irina-shishko.md|Irina Shishko]]: with [[wiki/people/vladimir-samusenko.md|Vladimir]] joining the autotests from Wednesday for about 8 days, the tests finish "до 23 числа"; Val checked: "до 23 октября". She added that this is for autotests only — development "должна закончиться раньше" [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]].
- **Val's reading.** "по сути дела, мы не можем выпустить продукт до 23 числа." Pavel: "Почему нет? Мы можем" — a trial batch of about 10 locations can go out earlier, without waiting for all autotests, if remote update of Flex IQ works, because problems can then be fixed remotely [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]].
- **The first installs are Flex IQ only.** Val: "на MVP один мы начинаем только с установки IQ[,] не флекспей." Pavel and Irina: yes. This matches [[wiki/decisions/2026-09-11-mvp1-goes-with-flex-iq-alone-and-one-kiosk-per-location.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]].
- **Why Val expects it to be faster.** The tests are written with Claude (Irina: "Ну конечно"), so "цифры, которые вы нам даёте, они консервативные." Irina needs "пару дней" to judge the real speed; until then October 23 stands as her estimate [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]].

## What it changes

- The date moved, so the scope grew: remote update of the Flex-Port comes back into MVP 1. See [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Sept-28 update).
- **Plan vs actual** (owner's 2026-09-01 principle, [[wiki/decisions/2026-09-01-first-nova-product-south-dakota-vlt-2.md]]): the old plan was October 1 ([[wiki/decisions/2026-09-09-first-transactional-installation-planned-for-october-1.md]], now superseded). The new plan is October 15. No actual date is known yet.
- *(Inference:)* Klimovich's Sept-24 warning that "15 это может превратиться в 30" is not withdrawn in words; he now calls 15 the real date.

## Update, Oct 1 2026 — the slice on the old date: all MVP 1 features closed by the developers, 165–174 still open, development done by Sunday or Monday, and the Oct 22–23 dates are the autotests

On October 1 — the date this decision replaced — [[wiki/people/andrei-klimovich.md|Klimovich]] asked for "срез. Того, где мы находимся, с [MVP] один" at the [[wiki/meetings/2026-10-01-transactional-mvp1-status-slice-and-sas-command-logging.md|8:02 AM call]] (Russian) [[raw/Meeting_Transcript_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]]:

- **Development.** [[wiki/people/pavel.md|Pavel]]'s Jira view, sorted by status: MVP 1 "начинается отсюда 122"; the top capabilities "все в… реквест ревью. Это значит, что разработчики закрыли. Все фичи. И остались только задачи по тестированию и по написанию автотестов"; still In Progress or To Do "начиная с к а п 165. И заканчивая… кап 174" — not fully cleaned ("Сейчас дочищу"). [[wiki/people/dmitri-chudinov.md|Chudinov]]: reprint, records and the SAS-command logging remain; "с учётом рабочего выходных… до конца до воскресенья до понедельника всё это добьём". Klimovich: "по [IQ] и по портовому клиентам всё будет готово по разработке… к понедельнику" — Pavel: "примерно выглядит так".
- **Testing.** [[wiki/people/irina-shishko.md|Irina]]: "Тестирование моё завтра… сегодня не увидим ещё ничего." The due dates "22 октября 23" on the board: Chudinov — "там авто тесты… разработка с тестами смешанная" — so the October-23 autotest estimate above still stands.
- **Georgia.** The field check waits on a date from Elizabeth — [[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]] (Oct-1 update).

The derived notes record the slice the same way [[raw/Meeting_Notes_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]]. October 15 was not mentioned on the call; nothing here moves it.

## Open commitments

- [ ] The autotest team ([[wiki/people/alexei-khamin.md|Khamin]], [[wiki/people/ivan.md|Ivan]], Vladimir Samusenko) — finish the autotests and reach the final state by October 15 if possible; 95% done is acceptable — due Oct 15 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]]
- [ ] [[wiki/people/irina-shishko.md|Irina Shishko]] — re-judge the autotest finish date after a couple of days of real progress — due about Sept 30 2026 ("пару дней") — [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]] — *Sept 30 2026: her status was "с тестами получается, на мой взгляд, неплохо. Все подтянулись, пишут… тесты проходят"; no new date was given, so October 23 stands* — [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]] — *Oct 1 2026: "Тестирование моё завтра… по тестированию мы будем обновляться завтра" — her update is due Oct 2* — [[raw/Meeting_Transcript_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]] — *Oct 2 2026 (stand-up): no new date — she asked Vladimir, Khamin and Ivan to mark their done items in Jira "потому что нужно как бы переобновить расписание, чтобы понимать до когда это будет сделано"; the Oct-2 MVP 1 sync, if held, is not in the corpus* — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]

## Open questions

- Can the autotests move from October 23 to October 15, and does a trial batch of about 10 locations go out before they finish? — [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
