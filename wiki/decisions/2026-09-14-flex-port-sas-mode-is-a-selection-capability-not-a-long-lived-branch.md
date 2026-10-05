---
type: decision
title: The Flex-Port SAS / no-SAS split is a selection capability inside main, not a long-lived branch — Val names the missing selection screen as his own specification gap, and a branch may promise less than main until it merges
date: 2026-09-14
aliases: [SAS no-SAS selection capability, long-lived development branch, branch becomes mainstream, a branch may promise less, capability that holds the filter, selection screen, scope gap, FlexPort operating mode, build-time or device parameter, one code base, 10 capabilities for the port, 30 capabilities October 1]
source-count: 4
status: active
open-commitments: 1
open-questions: 1
---

# The Flex-Port SAS / no-SAS split is a capability, not a branch

The engineering argument inside the [[wiki/meetings/2026-09-14-code-standards-main-branch-rule-and-alekseev-coaching.md|September 14 2026, 7:37 AM code-standards call]] (Russian, ~21 minutes). It begins as [[wiki/people/pavel.md|Pavel Frolov]]'s single objection to the main-branch rule ([[wiki/decisions/2026-09-14-main-branch-must-always-build-and-the-code-belongs-to-the-project.md]]) and ends with [[wiki/people/val-levitan.md|Val Levitan]] re-classifying Pavel's branch as a missing product capability — and taking the blame for it.

## Pavel's objection: a development branch that becomes the mainstream

> "**Должно, за исключением тех случаев, где мы хотим от мэйна держать ещё какойто девелопмент бранч. Который… на какое то время становится мейнстримом.**"

— main *should* always build, except where we want to hold a development branch off main that for a period becomes the mainstream [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

His live example is his own: "**я сейчас взял как раз проект платформ[а] флекс flexport. Я от его ответвился, чтобы добавить всю работу, связанную там с с а с AFT вот эту часть**" — he branched off the **Flex-Port** platform project to add the **SAS / AFT** work [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. That is the work assigned on [[wiki/decisions/2026-09-07-flex-port-goes-sas-and-jvl-drops-the-old-machine-segment.md]].

## Val's answer: the rule bites at the merge point

- "**как только вы затянете его в мей[н]. То хамин может взяться вот этот кусок в мэй[н], и он должен работать. Он же не ваш бранч проверяет**" — the moment you pull it into main, [[wiki/people/alexei-khamin.md|Khamin]] may take that piece from main and it has to work; he is not checking *your* branch [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].
- **Khamin corrected the premise from the QA side**: "**Да, есть возможность собрать из ветки и проверить**" — yes, it is possible to build from a branch and check it [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].
- **Pavel keeps his branch under his own checking until main is ready to build both variants**: "**Мой бранч буд[у] проверять. До тех пор, пока мы не скажем, что окей, мы готовы к тому, что теперь у нас мэйн будет иметь возможность собираться как для… старого варианта no s[as] и новый вариант с. А. С.**" — until we say main can now build both the old **no-SAS** variant and the new **SAS** one [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].
- **Val conceded the narrower promise.** "**В принципе, да, потому что мы можем сказать, что в бра[н]че должно работать, только вот это и вот это**" — in principle yes, because we can say that in the branch only this and this has to work [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. That is the accepted exception: **a branch may carry a narrower, explicitly stated promise; main's full promise applies from the merge.**

## Where Val refused: a branch is not a container for capabilities

Pavel extended the pattern — a big branch containing "**там 20 копбилити, каждый отдельно ответвление уже от этого бранча**" (twenty capabilities, each branching again off that branch, so specific features can be checked separately). Val: "**20 таки[е] [кейпа]билит[и] это уже не [брать]… это вы уже по-моему утрируется**" — twenty capabilities is too far; you are exaggerating [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

Pavel then swapped the hypothetical for the real release: "**делаем версию флек[с] все [кейпа]билити, которые мы обсуждали в пятницу, которые надо сделать к 1 октября. Сколько их там штук? 30**" — the capabilities discussed on the Friday, due by **October 1**: thirty of them. [[wiki/people/andrey-bosik.md|Andrey Bosik]] corrected the scope: "**это по всем системам, там же по порту конкретно меньше**" — that is across all systems; for the port specifically it is fewer. Pavel: "**по порту будет меньше. Ну 10**" [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]

*(Recorded as spoken. **20** is Pavel's hypothetical, **30** is his figure for all systems, **10** is an unchecked figure he offers for the port after Bosik's correction — the derived notes flag the same count as worth confirming with Val before being treated as fact [[raw/Meeting_Notes_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. The "**в пятницу**" meeting is Friday **Sept 11 2026**; the October 1 date is stated in the call.)*

**Val challenged the need for one branch at all**: "**И вы все 10 делаете в одном бранче, а зачем вы это делаете?**" Bosik answered for the engineering: "**Они все взаимосвязаны**" — they are all interrelated. Pavel added the isolation reason: "**Чтобы не миксовать с той версией, [над] которой работает… [Я]ворский[,] Алексеев, чтото в той ветке делал, ну, в мейне**" — so as not to mix with the version being worked on in main [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

**Val's counter was tags**: "**а разве вы это не в тагах сортируете?**" — don't you sort this with tags? Pavel and Bosik both answered that a tag and a release are effectively the same thing ("**это почти одно и то же**" / "**Релиз это и есть тоже так**"), and Pavel proposed the concrete manoeuvre: tag the working no-SAS version as **release number one**, then declare his own branch the new main — "**а на ту ветку, с которой я работаю, сказать это теперь [мейн]. И это пойдёт уже как мейн[ов]ка со всеми новыми фичами**" [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

**Val did not accept it**: "**Чтото я так не вижу**" — I just don't see it that way [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

## The ruling: what is missing is a capability that holds the filter

> "**Если мы говорим о том, что вы сделали какието разработки… которые опционально включаются и выключаются. То, скорее всего, что не хватает кейпо билети, который имеет вот этот вот фильтр. Который в мэйн может сортировать, что включается, что не включается.**"

— if the work is a set of pieces that switch on and off optionally, then what is probably missing is a **capability that holds the filter** — the thing that in main decides what is switched on and what is not [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

**Pavel accepted it and immediately produced the case that proves it:**

> "**в таком случае можно оставаться в рамках м[эйна], но ещё недавно говорилось о том, что нам надо флекс порт, который работает по сас. Это как… отдельный чуть ли не проект. Вот от него пошла бранч[;] вчера вы написали, что нам надо, чтобы флекспорт мог работать и на машинах без сас. Это как бы немножко ломает то, что я уже сделал. И то есть надо обратно возвращаться в мэйн и иметь возможность переключать, либо мы работаем так, либо так, но кодовая база одна.**"

— we can stay inside main; but recently it was said we need a Flex-Port that works over SAS, almost a separate project, and the branch came off that — and then **yesterday you wrote that Flex-Port must also work on machines without SAS**, which somewhat breaks what I have already built. So we go back into main and have a way to switch between the two modes, with **one code base** [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. *("Yesterday" = **Sept 13 2026**; the email itself is not in `raw/` and is known only from Pavel's report of it here.)*

**Val took the example and turned it on himself:**

> "**вы, кстати[,] правы, это хороший пример. Но это значит, что вы скажете, я нашел ско[уп гэп]… нужно сделать фильтр сортировку какойто экран, который выбирает или так или так… тогда вал недосказал, что должен быть сортировочный экран… Это является ско[уп гэп].**"

— you are right, this is a good example. But it means you say *I found a [scope gap]*: a filter, a sorting, some **screen** that selects one way or the other. If the build has to work with this as well, then **Val under-specified** — he should have said there must be a selection screen. That is a [scope gap] [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

*(The term is rendered "**скобгад**" and twice "**скобка**". Read as **scope gap** — an **inference**, from the sense of the sentence and from Val using a different rendering, "**кейпо билети**", for *capability* earlier in the same passage. The derived notes read the same word as "capability" [[raw/Meeting_Notes_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. Neither reading is asserted; the word itself is recorded as rendered. JVL has a standing "scope gap" practice — see [[wiki/meetings/2025-03-27-flexpay-scope-gap-discovery.md]].)*

**Pavel restated it in his own words, and that restatement is the requirement:**

> "**у нас должна быть возможность задавать режим работы для флекспорта, каким[-]то образом либо на этапе сборки либо… на собранном девайсе каким то параметр[ом].**"

— there must be a way to set Flex-Port's **operating mode**, either at build time or by a parameter on an assembled device [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. Which of the two was **not chosen**.

## Update, Sept 26 2026 — the branch still carries the SAS work, and a debug command switches the mode

At the [[wiki/meetings/2026-09-26-flex-port-telnet-console-and-gui-harness.md|Sept-26 Flex-Port development sync]], [[wiki/people/pavel.md|Pavel]] described the "порт 9" branch: SAS support "перетянутая из Того проекта, который был с сасом", AFT commands, and part of the Wi-Fi work, with pull requests 51 and 68 to follow into it. So as of Sept 26 the SAS work still sits in a branch. The board's Telnet debug console can "включить режим сас или включите режим ноу сас" — a mode switch on an assembled device. Whether that debug command is the product's mode setting is not said. [[raw/Meeting_Transcript_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]]

## Update, Oct 1 2026 — the mode is a per-port parameter, set on the Flex IQ set-up screen and sent at registration

At the [[wiki/meetings/2026-10-01-daily-standup-sas-mode-flag-and-feature-status-rules.md|Oct-1 Minsk stand-up]] (Russian) [[wiki/people/pavel.md|Pavel]] raised the two-mode requirement with [[wiki/people/dmitri-chudinov.md|Chudinov]]: "надо портам говорить, в каком режиме они сейчас работают. Сас или не сас?" — and the "build time or a parameter" question was answered the second way: a per-port toggle on the Flex IQ set-up screen ("на вот этом вот окошке, где подключенные девайсы… выбрать напротив девайса… какой режим"), sent to the port at terminal registration as the parameter after the PIN code, server-side control deferred to MVP 2 or 3, switching only on an idle port, modes named "sas AFT" and "no sas". Chudinov's objection — "у нас в требованиях нет ничего про 2 режим… на конец релиза" — and Pavel's "эта задача на 5 минут" are there too. Full ruling on [[wiki/decisions/2026-10-01-sas-or-no-sas-is-set-per-flex-port-on-the-flex-iq-set-up-screen-and-sent-at-registration-with-the-pin-code.md]] [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]. Whether Pavel's "порт 9" branch has merged into main is still not said.

## Open commitments

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — treat the Flex-Port SAS / no-SAS split as a selection capability inside main, with one code base and a way to set the operating mode, instead of a long-lived branch — due unspecified; no Jira item named in the call — [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]

## Open questions

- ~~**Whether the Flex-Port operating mode is set at build time or by a parameter on an assembled device.**~~ Pavel named both; neither was chosen — [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. **Answered Oct 1 2026:** a parameter — chosen per port on the Flex IQ set-up screen and sent at registration with the PIN code (see the Oct-1 update) — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
- **How many capabilities the October 1 Flex release actually carries, and how many of them are Flex-Port.** "30" across all systems and "well, 10" for the port are both unchecked figures spoken in the call — [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]] [[raw/Meeting_Notes_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]

**§15.8:** clear — engineering scope and branching practice only; no named-person compensation.

## Sources

- [[raw/Meeting_Notes_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]
- [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]
- [[raw/Meeting_Transcript_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
