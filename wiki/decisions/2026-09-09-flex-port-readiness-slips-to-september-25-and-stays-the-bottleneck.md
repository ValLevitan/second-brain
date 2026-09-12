---
type: decision
title: Flex-Port is the bottleneck for the whole transactional programme — not ready for a location on September 11, most likely not September 18, best case September 25
date: 2026-09-09
aliases: [Flex-Port is the bottleneck, best case the twenty-fifth, not September 11, not September 18, when can I put it at a location, one stand by the middle of next week, bottleneck estimate]
source-count: 2
status: active
open-commitments: 3
open-questions: 1
---

# Flex-Port is the bottleneck, and readiness slips to a best case of September 25

The question [[wiki/people/val-levitan.md|Val]] called the [[wiki/meetings/2026-09-09-september-resource-plan-and-flex-port-readiness.md|Sept 9 2026 7:02 AM resource-plan call]] to answer: "флегспорт… должен заработать, когда? Когда могу я его поставить на лаке[йшн]?" — when will Flex-Port work, and when can he put it at a location [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].

## The estimate

- **Val had already asked about Friday September 11 and been told no.** "[Е]сли я планирую здесь время, я у вас спросил, 11 сентября это пятницу, вы сказали, наверняка нет" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].
- **September 18 goes too.** Val: "Окей, мы знаем, что это не 11 сентября, так как так, когда?… 18." [[wiki/people/pavel.md|Pavel Frolov]]: "Скорее всего, нет. По моим ощущениям" — most likely not, by his feel [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].
- **Best case is the 25th.** Pavel: "я думаю, что гдето ну в лучшем случае… в лучшем случае это 25" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]. Irina checked what the date covers — "и 25 число я так поняла, ты сказал это для… [MVP]… всего[,] не для копобилиц[ы] данной" — and Pavel confirmed it is the **MVP**, the set of capabilities judged minimally necessary to launch, not the single capability under discussion: "да[,] это MVP с набором каких[-]то [капа]билити котор[ые] мы… считаем, что минимально до[ста]точно необходимы для запуска" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].
- **Pavel would not commit further than that without testing.** Asked to be more precise, his answer was that it only becomes clear once testing starts and shows how many gaps surface along the way: "[Ко]гда начнем тестировать[,] станет понятнее, насколько много недоработок возникает по ходу" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].

## Why it is the bottleneck

Irina asked Pavel to say plainly whether Flex-Port holds everything else up, and he did: "ботлнек[,] значит он да будет задерживать, то есть пока не сделается какой[-]то функционал в[о] флекспорте[,] дальше проверить на flexpay какой[-]то функционал будет невозможно" — until a piece of Flex-Port functionality exists, the matching FlexPay function cannot be checked at all [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]. He had first hesitated between Flex-Port and the Flex-IQ services rework before settling on Flex-Port: "наверное, это в меньшей степени… флекспорт сейчас будет [бо]ттлнек[,] всё[-]таки наверное флекспорт" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].

This is the schedule consequence of the engineering direction already ruled on [[wiki/decisions/2026-09-07-flex-port-goes-sas-and-jvl-drops-the-old-machine-segment.md]] and [[wiki/decisions/2026-09-04-port-the-smib-sas-module-into-the-flex-port-main-branch.md]].

## What Pavel committed to instead

Rather than a location date, Pavel gave a **bench** date: "у нас по факту неделя… я бы наверное всё[-]таки и 15 число сказал[,] 16[,] середина недели… [с]ередина следующей недели мы должны подготовить хотя бы один стенд. Либо флекс[-]пэй[,] либо флекс[-]айкью[,] с [флекс-]портами с новой прошивкой, которые умеют работать по сассу" — at least one stand, FlexPay or Flex-IQ with Flex-Ports on the new firmware working over SAS, by the middle of the following week. He expected it to be FlexPay: "Скорее всего, это будет флекспей" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]. Val had asked for the 15th; Pavel's own number is the 16th — **a slip of one day inside the same week, recorded beside the ask, not replacing it** [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].

Separately he expected a Flex-IQ able to run in the e-wallet variant **by the end of the following week**: "к концу следующей недели я ожидаю, что уже будет вариант [ф]лекс[-]ай[-]кю[,] который в состоянии будет работать в варианте… [е-]волет" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].

## How the work is split

- **Pavel took the SAS work himself.** His stated reasons: partly interest — "мне это интересно" — but mainly resources. "Смогу сделать лучше, чем Алексеев хотя бы по той причине, что у меня больше для этого ресурсов… у меня есть там Лёша под боком[,] у меня есть Ира. У меня есть много машин, у меня есть возможность это всё в разных кейсах гонять" — [[wiki/people/alexei-khamin.md|Khamin]] and [[wiki/people/irina-shishko.md|Irina]] beside him and several machines to run cases on, whereas [[wiki/people/evgeniy-alekseev.md|Alekseev]] "будет всё равно нас дёргать[,] но с задержкой в сутки" — a roughly one-day delay on almost every request [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]. Val pushed back on the framing of that delay: "некоторые смотрят [на это] как [на] задержк[у], а некоторые на это смотрят[: ]вот я ему дал работу, я пошёл спать, а он работает" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].
- **Alekseev is booked for at least a week already** — current Wi-Fi tasks plus finishing the firmware update: "у Алексеева пока есть актуальные задачи по вайфаю. Это раз[;] во[-]2[,] доделать обновление прошивок… этих задач хватит? Ну на неделю точно" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]. The firmware-update work is the one ruled on [[wiki/decisions/2026-09-07-remote-firmware-update-mandatory-and-taken-off-yavorsky.md]].
- **Pavel wants the remote-log work given to Alekseev if he can carry it** — "какой[-]нибудь вот… lo[g]s transferring это можно Алексееву, если он сможет это взять и вести… [е]сли он не только в выходные будет работать" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].
- **The Flex-Port code is all in git.** Irina: "[по] флекс[-]пор[ту] тоже[,] этот Яворский уже всё должен был в ги[т] выложить[,] у него ничего не должно было нигде ж остаться"; Pavel confirmed: "Вся работа в [гите]" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]. This closes the loose end left on [[wiki/decisions/2026-09-04-port-the-smib-sas-module-into-the-flex-port-main-branch.md]] about [[wiki/people/eugine-yavorski.md|Eugine Yavorski]]'s material.

## Open commitments

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — have at least one working stand ready (FlexPay or Flex-IQ with Flex-Ports on the new firmware, working over SAS; most likely FlexPay) — due mid-week of Sept 14 2026, his own number being Sept 16 against Val's ask of Sept 15 — [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — get the full setup working in the office, however roughly, at least two weeks before the October 1 installation, so [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] can start testing — due week of Sept 14 2026 — [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]] [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [ ] [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] — take the remote log-transfer work over WS/SAS if he can carry it alongside the Wi-Fi tasks and the firmware update — due unspecified — [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

## Open questions

- Can Alekseev be moved to full time, or take this work on at his current job? Val raised it — "я могу, например, Алексееву попросить взять [эту работу] на своей работе или взять его на фултайм работу" — and Pavel said he is workable with ("долго его убеждаешь в том, что надо другим путём идти, но в целом он адекватный"). Not resolved. — [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

**§15.8:** clear — assignment, capacity and scheduling only; no named-person compensation recorded.

## Sources
- [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
