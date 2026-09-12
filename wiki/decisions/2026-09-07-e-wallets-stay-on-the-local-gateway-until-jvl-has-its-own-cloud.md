---
type: decision
title: E-wallets stay on the local gateway for now — Val defers the cloud move to JVL's own cloud server, expected within about six months, and accepts the limit that a wallet made at location A will never work at location B
date: 2026-09-07
aliases: [wallets stay local, cloud deferred six months, own cloud server, location A location B, ticket collision, do not load your head with it before the show]
source-count: 2
status: active
open-commitments: 0
open-questions: 0
---

# E-wallets stay on the local gateway until JVL has its own cloud

Ruled by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-09-07-gacs-show-setup-flex-iq-flex-ports-and-the-e-wallet.md|Sept 7 2026 8:00 AM call]] (Russian), over [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]]'s cloud-first preference. **It re-times, rather than cancels, [[wiki/decisions/2026-09-02-e-wallets-move-to-the-cloud.md|the Sept-2 ruling that e-wallets move to the cloud]]** — the cloud is still the destination; what changes is when, and on whose server.

## How it came up

Chudinov re-opened the question he had raised five days earlier: "Это создание [и]волет[ов]… [в] клауд[е]… Внешнее хранилище[,] внешнее создание, уникальное, которое потом распространяется на всю систему[,] и дальше в будущем мы уже решаем, можно ли этот [и]волет использовать только в рамках одного лок[ейшна], либо в рамках одного кастомера." He confirmed the present state: "Текущий [Флекс] был реализован так[,] всё локально, у него своя база, и он никуда ничего не раздаёт" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].

[[wiki/people/andrei-klimovich.md|Andrei Klimovich]] pressed on what actually changes for security — "Если мы создаём эти [и]волиты локально на [gateway] или создаём их в клауде… Как работает система безопасности в этом случае? Вот копирования[,] дубликата, попытки взломать этот [и]волет[,] создать его искусственно" — and Chudinov's answer was a preference plus a design principle, not a threat model: "с точки зрения безопасности, лучше вынести всё это в серверный вариант. К тому же будет единый принцип ответственности" (a single point of responsibility). Asked whether "server" meant cloud, he confirmed: "Облако" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].

[[wiki/people/pavel.md|Pavel Frolov]] supplied the one concrete risk on the table: "сейчас, наверное, сгенерированные локально тикеты… с очень маленькой вероятностью, очень маленькой, но на… чужом лак[ейшне], наверное, может быть коллизия" — a small chance that a locally generated ticket number collides with one issued elsewhere [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].

## What was decided

- **Stay local, and move everything when JVL's own cloud server exists.** Val: "Это в течение полугода мы выпустим свой облачный сервер. До этого мы, в общем-то[,] совсем безопасны. Загружать сейчас свой мозг этим — это мне кажется[,] просто выставка… Шансы очень, очень маленькие… И инсталляций будет не очень много. Поэтому я бы просто… пошёл бы этим путём[,] за это время сделал бы свой облачный сервер, и [пере]м[естил] всё в облачный сервер" — about six months to JVL's own cloud server; the risk is very small; installations will be few; and it is not worth loading anyone's head with it before the show [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]. The derived notes record the same ruling [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].
- **Klimovich confirmed the state that follows:** "Тогда мы едем пока на локальном сервере[,] на [gateway], [где] хранится" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].
- **The accepted limit, stated and agreed on the spot:** "Давай тогда [про]говорим один лимит, что пока мы на локальном сервере[,] [и]воля, созданн[ая] на локации [а,] никогда не будет поддерживаться на локации б." Pavel: "Ага… Хорошо" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]] [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].

## What this settles, and what it does not

- **It answers the Sept-2 open question about wallet scope — but only for the local period.** On Sept 2 whether a wallet stays tied to the location that created it was left explicitly unresolved, with Val "не уверен, что мы хотим делать такой дизайн" and Pavel's server-side "friendly locations" flag offered as the later mechanism. Here the same limit is **accepted as a stated constraint of running locally**, with no claim about what happens after the cloud move. The Sept-2 question therefore stands for the post-cloud design [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].
- **It does not answer the operator-scope half** of Chudinov's original Sept-2 question, which he restated here ("в рамках одного лок[ейшна], либо в рамках одного кастомера") and which again went unanswered [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].
- **The security question Klimovich asked was never actually answered.** No one described what copying, duplication or forgery looks like in either architecture; the decision was made on time-to-ship and installation volume [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].

**§15.8:** clear — architecture and timing only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
