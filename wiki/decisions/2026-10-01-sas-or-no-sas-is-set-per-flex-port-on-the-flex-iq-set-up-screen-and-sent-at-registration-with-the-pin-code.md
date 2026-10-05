---
type: decision
title: A Flex-Port's SAS / no-SAS mode is set per port on the Flex IQ set-up screen, not on the server (that waits for MVP 2 or 3), and goes to the port at terminal registration with the PIN code; a port switches only when it holds no transaction and no money; the modes are called "sas AFT" and "no sas"
date: 2026-10-01
aliases: [SAS mode flag, sas AFT и no sas, SAS AFT, no SAS, тумблер переключения, mode per port, mode on the Flex IQ set-up screen, not on the server, PIN code and mode at registration, port switches when idle, эмуляция билаксептора, part of a location on SAS and part not, одном банке часть машин по сассу, flag on the fly, задача на 5 минут, server-side toggle MVP 2 or 3]
source-count: 2
status: active
open-commitments: 1
open-questions: 2
---

# SAS or no SAS is set per Flex-Port on the Flex IQ set-up screen, and sent at registration with the PIN code

Settled by [[wiki/people/pavel.md|Pavel Frolov]] with [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] at the [[wiki/meetings/2026-10-01-daily-standup-sas-mode-flag-and-feature-status-rules.md|Oct-1 Minsk stand-up]] (Russian), and restated for [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] later in the same stand-up [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]].

## What was asked

Pavel, after Chudinov's status: "**надо портам говорить, в каком режиме они сейчас работают. Сас или не сас?**" Chudinov: "Ни сас это что?" Pavel: "**Не сас этого как было раньше эмуляция билаксептора**" — not-SAS is the old bill-acceptor emulation [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]. This is the two-mode requirement that came out of Val's Sept-13 email on [[wiki/decisions/2026-09-14-flex-port-sas-mode-is-a-selection-capability-not-a-long-lived-branch.md]].

## The ruling, step by step

- **Who decides the mode — first the server, then not.** Chudinov: "А кто это решает?" Pavel: "Это надо, чтобы решалось на серверной стороне". Chudinov: "зашибись Паша ну блин я на сервере думаю уже всё закончил… куда мы это вставляем лакейшн". Pavel pulled it back: "**можем пока что это на сервер не выносить можем оставить на вот этом вот окошке, где подключенные девайсы. Флекс порты да и чтоб ты мог выбрать напротив девайса, например, какой режим у него работы.**" The gain: "**в одном банке часть машин по сассу работает, часть машин не по сассу**" — one location can mix [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]].
- **Where it lives in Jira, and how it reaches the port.** Chudinov: "Это надо в ту задачу в cappality, где про пинкоды, чтоб это пошел как отдельный такой этот флаг". Then: "давай то сейчас чтоб запомнили либо я, либо Сергей там будет задача с пинкодами. Когда регистрируются терминал, чтобы одни параметры шёл пинкод 2 параметром шёл вот этот режим" — at terminal registration the PIN code is parameter one and the mode is parameter two. Pavel: "Да да" [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]].
- **Switching on the fly.** Chudinov: "этот флаг еще на лету надо переключать… А если налито переключается от его экранах скана… деньги потеряны" — what if it flips mid-transaction. Pavel: "**порт должен этот флаг ловить, если у него в данный момент нет транзакции… на нём нет денег, то он просто переключается и всё.**" Chudinov: "Угу" [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]].
- **The names.** Pavel: "**у меня называется сас и no sas, а не один режим называется sas AFT а 2 называется no no sas. Почему sassa FT? Потому что там теоретически возможен ещё наверное один в будущем режим просто сас без af FT.**" Chudinov: "тогда для 2 придумаем, что то более нормальное на сасс както. Очень широкое понятие" — he will find a better name for the second mode [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]].
- **Not the server — restated for Tsymanov.** Tsymanov, who had heard "пробрасывать", placed it on the server: "Для меня это было сервер". Pavel: "**нет, нет, нет, это именно девайс относится к флекспорту**"; Chudinov: "на сетапе, где вкладка всех подключенных, чтоб у каждого была тумблер переключения"; Pavel: "**Мы сказали, что пока что оставляем на киоске. На MVP там 2 или 3 это можно будет добавить, что когда мы пробросим информацию о портах, ну начнём их там показывать, мониторить их состояние. На сервере ну можем туда и это тумблер тогда добавить.**" Tsymanov: "окей, хорошо" [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]].

## The objection that did not stop it

Chudinov: "**А мы точно вам в AP один будем в 2 режимах выходить.**" Pavel: "**Нет, нет.**" Chudinov: "**Ну у нас в требованиях нет ничего про 2 режим, а мы начинаем набрасывать. Блин, на конец релиза, вот и это и это.**" Pavel: "**Но как по мне, эта задача на 5 минут.**" Chudinov: "Не так я флаг сделаю. Вопрос а что будет… на порте?" — he will make the flag; the port side is the question [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]. *(So: MVP 1 does not ship in two modes, per Pavel's "Нет, нет"; the flag is added now because it is small. The derived notes call this "not fully clear" [[raw/Meeting_Notes_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]; it is recorded here as spoken.)*

Pavel then asked whether any other parameter must be given to a device at the start — "нет ли ещё какихто параметров… чтобы он нормально заработал?" — and answered himself: Wi-Fi is by default ("Если он найдёт, то он будет пытаться работать через вайфай"), and "это MVP 2" [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]].

## Where it sits

- It answers the open question on [[wiki/decisions/2026-09-14-flex-port-sas-mode-is-a-selection-capability-not-a-long-lived-branch.md]] — build time or a parameter on the assembled device: **a parameter**, chosen per port on the Flex IQ and sent at registration. The Sept-26 Telnet debug command ("включить режим сас или… ноу сас") is a developer's switch; this is the product's.
- It extends the registration exchange Chudinov already builds for the PIN code ([[wiki/topics/flexpay-business-architecture-payout-devices.md]]).
- The derived notes record the same four points — per device on the Flex IQ set-up screen, server later, idle-only switching, "SAS AFT" / "no SAS" [[raw/Meeting_Notes_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]].

## Open commitments

- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] or [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] — add the mode flag to the PIN-code capability: a per-port toggle on the Flex IQ set-up screen's connected-ports tab, sent as the second registration parameter after the PIN code — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]

## Open questions

- **What the port does with the flag beyond the idle case** — Chudinov: "Вопрос а что будет… на порте?"; Pavel gave only the idle rule — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
- **The second mode's name.** "no sas" is Pavel's; Chudinov wants something "более нормальное" — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]

**§15.8:** clear — product design only. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
