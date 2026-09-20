---
type: decision
title: InComm returns no daily-cap error, so JVL cannot detect one — requirement 1533 is removed and the location's call comes to JVL first, to be read out of the logs
date: 2026-09-16
aliases: [requirement 1533, daily cap, velocity, InComm limits, no daily cap error, unofficial number, support web interface, running daily total, hotline number, дейли кап, велосити, fraud velocity]
source-count: 2
status: active
open-commitments: 1
open-questions: 1
---

# InComm returns no daily-cap error, so the call comes to JVL first

Requirement **1533** — handling [[wiki/organizations/incom.md|InComm]]'s per-location daily cap and velocity limits — was removed at the [[wiki/meetings/2026-09-16-transactional-mvp1-open-questions-and-offline-operation.md|Sept 16 2026 8:01 AM call]] (Russian), on a fact checked live in the middle of the meeting [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. *([[wiki/people/irina-shishko.md|Irina Shishko]] noted that [[wiki/people/pavel.md|Pavel Frolov]] had already edited 1533 before the meeting reached it.)*

## What the two InComm limits are

[[wiki/people/andrei-klimovich.md|Klimovich]] explained both, as the only person on the call who had them [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]:

- **Daily cap** — "сколько денег может быть загружено [ИН]КОМ[ом] в пределах этой локации в течение дня" — how much money InComm will load onto cards at one location in a day. Each location starts from a default and the figure is then held individually per location and changes over time. *(Klimovich's estimate of the default was hedged — "там дефолтное значение типа 3000 или $5000" — and is recorded as his approximation, not as a stated figure.)*
- **Velocity** — "калькулируемый ими сами[ми] параметр[:] интенсивность выпуска карт за единицу времени. Это для борьбы с фродом" — a parameter InComm computes themselves, the rate of card issuance per unit of time, used against fraud. Klimovich's illustration: a hundred cards in an hour and "они такие[:] ой, что[-]то явно здесь не то". **What InComm then does he does not know** — flag the next activation and block it, or follow some internal procedure and try to telephone the location — and he said so rather than guess.

## The fact that decided it

Klimovich put the deciding question to [[wiki/people/dmitri-chudinov.md|Chudinov]] — do we get an explicit error from InComm saying the card cannot be issued because the daily cap is reached — and Chudinov went and read the API documentation during the call. He came back with nothing: "я посмотрел [доку]ментаци[ю]… [про] дейли кап нет. Соответственно и ошибок никаких не будет", and again a minute later, "я в документацию не нашёл ничего" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

Klimovich's conclusion was immediate: "раз нет ошибок, то её нам здесь делать нечего" — with no error to catch, the requirement has nothing to do [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. It was deleted.

## The consequence the room accepted with its eyes open

Chudinov walked the support path that follows from having no error code [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]:

> **[Б]удет ошибка от [ИН]КОМ[а,] скорее всего[:] операция невозможна[,] и мы будем писать на экране, что мы не можем активировать карту по неизвестной причине. Звонить уже будут не банк[у], а сначала нам[:] почему не работает? Где мы будем сидеть, смотреть [л]оги, и мы увидим, что мы целый день выпускали карты, а… в какой[-]то момент… раз[ —] и перестал[о] выдавать.**
>
> *(There will probably be an error from InComm — operation impossible — and we will write on the screen that we cannot activate the card for an unknown reason. They will then call not the bank but us first: why is it not working? And we will sit and look at the logs and see that we issued cards all day and then at some point it simply stopped.)*

Irina supplied the diagnosis the logs will suggest — "потому что превысили лимит" — and Chudinov refused to call it certain: "неизвестно[;] мы будем только догадываться потом" (we will only be guessing afterwards) [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. Irina's summary of the new support chain, confirmed by Klimovich: "сначала он должен связаться с нами, чтоб потом мы его отправили в ИНКОМ" — the location contacts JVL first and JVL forwards them to InComm [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

The one thing that can be done up front is a warning: Klimovich would tell each location that this can happen, hand them InComm's hotline number, and have them ask for the cap to be raised — "вот вам хотлайн намбер [ИН]КОМ[а,] звоните им[,] просите поднять" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## Where the running total should live — settled against the operator menu

Pavel wanted the day's card total visible in a menu, because the first thing InComm will ask a cashier is how many cards and for what value went out today, "и он скажет[:] не знаю. Сейчас я возьму калькулятор, посчитаю" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

Klimovich was against putting it in front of the operator — "не очень поддерживаю, потому что это не очень [о]фиши[а]л намбер" — JVL's own tally is not InComm's official number, and the cap it would be read against is per-location and moves. His counter-proposal was to put it in JVL's own support tooling instead [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]:

> **удобн[ый] веб[-]интерфейс, где в течение дня прямо вся калькуляция будет видна… и глядя на эту сумму ты можешь сказать[:] вот так[,] ребята[,] у вас там $5000 за сегодняшний день[;] судя по всему, может быть[,] де[йли] кап. Позвоните в [ИН]КОМ, уточните, какой у вас дейли кап стоит для вашей локации.**

Chudinov's addition, contingent on InComm ever exposing the limit: "если б нам давали информацию о каком[-]то дейли кап[е], мы могли бы… сами вести сумму и подсказывать на будущее, что вы уже приближаетесь к ограничениям" — JVL could then run its own count and warn a location as it approached the ceiling. That remains impossible today [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — provide the day's running card-issuance total to support in JVL's own reporting/web interface, so a suspected daily cap can be spotted from the logs ("это уже наша задача[:] в репорт[е] я это сделаю") — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]

## Open questions

- **Whether the running daily total should also be shown in the operator menu.** Pavel wants it where the cashier can read it; Klimovich refuses to show an unofficial number to an operator and wants it in JVL's support interface only. Not resolved on the call — [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]

**§15.8:** clear — processor limits, API behaviour and support process only. The dollar figures here are InComm's per-location card-loading limits — platform economics, not any person's compensation; no named person's pay, rate or performance judgement appears in either source, and nothing was excluded on that ground. **§15.9:** no licence, registration, tax or account number appears in this material; the InComm hotline number referred to on the call is not stated in either source.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
