---
type: decision
title: At cashout the Flex-Port offers a second button that prints a new wallet ticket on the cashier's Flex-IQ printer over SAS — so a player never has to leave a machine holding a win
date: 2026-09-07
aliases: [print at the cashier, second button at cashout, scan existing or print new, SAS print command, do not leave the machine with a win, six machines per location]
source-count: 2
status: active
open-commitments: 0
open-questions: 1
---

# Print the winnings ticket at the cashier, over SAS

Proposed by [[wiki/people/genadi-peari.md|Genadi Peari]], shaped by [[wiki/people/pavel.md|Pavel Frolov]] and approved by [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] at the [[wiki/meetings/2026-09-07-gacs-show-setup-flex-iq-flex-ports-and-the-e-wallet.md|Sept 7 2026 8:00 AM call]] (Russian). It is the mechanism that makes the zero-balance wallet of [[wiki/decisions/2026-09-07-the-e-wallet-must-exist-with-a-zero-balance.md]] workable in a room with no printer on the machines.

## The question Genadi asked

"Каким образом [и]гро[к] получает [и]волет, если нету на машине принтера?" Klimovich's answer depended on the gateway: with Flex-IQ a printer is attached to it and the cashier prints the ticket and hands it over by hand; with a self-service kiosk such as the Slim, the kiosk prints it [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].

## The improvement

- **Genadi's proposal:** "А может [Флекс-порт] по [SAS] передать, чтобы… принтер распечатал тикет, который стоит возле каш[и]ра, и каш[и]р просто отдаёт этот билет игроку[?] Чтобы игроку не бегать к каш[и]ру." The objection he was answering was his own observation of the alternative: "Так он оставляет машину с выигрышем" — the player walks away from a machine still holding a win. He restated it as a button: "почему он не может нажать кнопку[:] распечатай мне мой билет[?] Он [по SAS] передаёт команду IQ, которому подключен тито[-]принтер. Билет печатается[;] всё, что ему надо[ —] подойти, забрать свой билет. Машина уже… на машине ноль кредит[ов]" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- **Val's reaction to the alternative was the same as Genadi's:** "Ну вот это мне тоже не нравится" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- **[[wiki/people/irina-shishko.md|Irina Shishko]] turned it into a choice:** either the player cashes out onto the wallet he already has, "либо у него его нет[ —] он говорит[:] пускай это печатает… создать новый, который у… кассира[.] Тогда нужен выбор" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- **Klimovich's worry — an extra step for every cashout — was answered by Pavel.** Klimovich: "мы добавляем игроку плюс один степ каждый раз, когда он будет делать коллек[т]." Pavel: "нет, этот степ всё равно я считаю обязательн[ым], то есть игрок, даже если у него есть [и]воле[т], когда он делает кэшаут, у него будет степ ожидани[я]: поднесите ваш [и]воле[т] для зачисления выигрыша. **Просто на этом степе мы можем показать ещё дополнительную кнопку — отпечатать тикет с выигрышем**" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- **Chudinov framed the two buttons** — "либо на выбор[:] отсканировать существующий, либо распечатать… новый" — and Klimovich approved: "Ну хорошо[,] класс, мне нравится. Идея хорошая" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]] [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]

## Val's caveat, and why the cashier version is acceptable anyway

"Безопаснее всего, когда на самой машине стоит принтер" — the safest arrangement is still a printer on the machine itself. The cashier-print option works because Georgia rooms are small: "лак[ейшн]ы очень маленькие, там **в среднем стоит 6 машин**, и сам флекспей будет стоять рядом с машинами, то в принципе это небольшая проблема — встать и подойти к киоску и взять билет. Это… будет работать" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]. *(The ~6-machine figure sits with the 5.9-machines-per-location market arithmetic on [[wiki/projects/georgia-market-rollout.md]].)*

Klimovich noted the consequence for hardware — "она нас ещё больше углубляет в флекспорт[ со] ста[ч]скрином, или флекспорт хотя бы с какими-то кнопками для выбора опции" — and Val said it was already settled: "Мы в принципе уже решили, что флекспор[т] должен быть ста[ч]скрином… Сделаем такой же флекспорт, как у нас сегодня, только удешевляем дизайн… за счёт уменьшения мемор[и]," with the caveat that this is for now, "пока мы не установили полностью весь процесс[;] в дальнейшем может что-то поменяться." That restates [[wiki/decisions/2026-09-04-flex-port-keeps-its-screen.md]] and adds the memory reduction as the cost lever [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].

## Open questions

- **The kiosk version of the same flow has a hole nobody closed.** Klimovich asked Genadi how it works with a self-service kiosk and answered himself: "с киоском тоже[ —] киоск просто распечатает. Ну там его кто-то перехватить может" — someone else could take the ticket off the kiosk. The discussion moved on — [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]

**§15.8:** clear — product flow only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
