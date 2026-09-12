---
type: decision
title: The terminal's operating mode is set at build time in the warehouse, not switched remotely — and nothing is deleted: the MudaGoose build is tagged and frozen as a separate product version
date: 2026-09-07
aliases: [build-time mode, no runtime mode switch, flash the build in the warehouse, nothing is deleted, tag the August 2026 show build, frozen product version, main goes its own way]
source-count: 2
status: active
open-commitments: 1
open-questions: 0
---

# Operating mode is set at build time — and nothing is deleted

Two linked rulings from the [[wiki/meetings/2026-09-07-gacs-show-setup-flex-iq-flex-ports-and-the-e-wallet.md|Sept 7 2026 8:00 AM call]] (Russian), answering [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]]'s proposal and then his real worry underneath it. Both follow directly from [[wiki/decisions/2026-09-07-flex-iq-cannibalises-mudagoose-no-parallel-operation.md]].

## What Chudinov proposed

A remote runtime mode switch: pick a terminal in the management screen, say which configuration it should run in, press apply, and the terminal changes mode on the fly — "у нас сейчас получается 2 варианта. Это либо [Муда]гус[ь], либо… флекспорт… и терминал автоматически на лету меняет режим и, соответственно, переключается на необходимые экраны и необходимое наличие дев[ай]сов," including which peripherals are required (barcode scanner in one mode, TITO printer in the other) and the communication protocols [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].

## What was decided

- **Not worth the effort — set it in the build, in the warehouse.** [[wiki/people/andrei-klimovich.md|Andrei Klimovich]]: "вот это вот[,] он[о] оффлайн[,] поддержка с переключениями[,] нам точно не нужна, и я бы не тратил туда время. Это можно на уровне билда прошивать. То есть вот мы в офисе[,] в [warehouse] в нашем[,] ставим билд какой-то изначально. И вот этот билд определяет поддержка [Муда]г[уса] или поддержка порта" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].
- **And from the show date, MudaGoose builds simply stop being installed.** "начиная с условного октября 21 [билды] для поддержки [Муда]гуз вообще ставится не должны будут" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].
- **[[wiki/people/pavel.md|Pavel Frolov]] backed it on operability**, not architecture: "Ну так проще оперировать на самом деле[.]" Chudinov conceded the point while noting it is the same thing one layer down — "на уровне сборки мы говорим[:] собирай в таком режиме… оперировать проще" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].
- **Nothing is deleted.** Chudinov's actual concern was losing functionality they might want back: "не получится так, что мы сейчас… сделаем… задачу на удаление функционала, а потом оказывается зря удалили[.] Вот кто-то хочет посмотреть." Klimovich was emphatic: "Удалять точно ничего не надо, боже упаси, ничего не удаляем. Это отдельная версия продукта, она останется в замороженном состоянии" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].
- **Pavel supplied the mechanism: tag it.** "текущую реализацию надо просто пометить каким-то тагом… Чтобы все понимали, что это вот был[а] выставка 26 года в августе. Всё[,] она заморожена, и дальше [main] идёт развиваться своим путём" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]. The derived notes record the same three points — build-time mode, nothing deleted, tag it as the August 2026 show build [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].

## The case Pavel left standing

Pavel pointed out that two operating modes will remain distinguishable regardless of MudaGoose — the e-wallet mode JVL is building now, and a possible TITO mode: "в том же Техасе… там же возможность на каждой машине будет стоять б[ил]л[ак]септоры, принтер. И мы захотим точно так же с помощью тикета переходить от машины к машине, но при этом не сканируя [баркод]." Asked by Klimovich what Flex-IQ would even be for in that arrangement, Pavel answered that it would not be: "в этой схеме… IQ не нужен[;] нам нужен селф[-]сервис киоск какой-то[,] вроде… флекспей слим." Val stopped the thread — "Вы зря прыгаете из Техаса на Джорджи[ю]… Вам будет тяжело так сориентироваться" — so **the Texas/TITO mode was raised and parked, not decided** [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]. The Texas-on-wallets ruling it sits against is [[wiki/decisions/2026-09-02-priorities-iq-ports-flex-pay-recycler-texas-on-wallets.md]].

## Open commitments

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — tag the current MudaGoose Flex-IQ implementation as the frozen **August 2026 show** version, so everyone knows main has moved down the new path — due unspecified — [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]] [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]

**§15.8:** clear — build and release process only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
