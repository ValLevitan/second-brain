---
type: decision
title: Val's MVP 2 — no Flex Pay; Flex IQ, Wi-Fi configuration, remote update for the Flexports and Flex IQ, diagnostics, Galaxy transactional brought up to reporting and dashboards, and the location's bank shortfall paid by card with the operator as guarantor — Flex Pay is retagged MVP 3, and each MVP takes two to three weeks with testing alongside development
date: 2026-10-15
aliases: [MVP 2 scope Oct 15, no Flex Pay in MVP 2, Flex Pay to MVP 3, retag Flex Pay MVP 3, гвоздь программы это вай фай, Wi-Fi is the centrepiece of MVP 2, remote update of Flexports moves to MVP 2, Galaxy transactional reporting and dashboards, location shortfall paid by card, Stripe on the location page, operator as guarantor, two to three weeks per MVP, desirably two weeks, development in parallel with testing, Andrei writes only functional requirements]
source-count: 2
status: active — Val's view, subject to the final MVP 2 list he is polishing with Andrei (Klimovich, by context — inference)
open-commitments: 4
open-questions: 2
---

# Val's MVP 2: Flex IQ, Wi-Fi, remote update, diagnostics, Galaxy reporting — Flex Pay moves to MVP 3

Set out by [[wiki/people/val-levitan.md|Val]] at the [[wiki/meetings/2026-10-15-wi-fi-router-switch-power-loss-battery-and-mvp2-scope.md|Oct-15 11:04 AM Wi-Fi meeting]] (Russian), with [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/irina-shishko.md|Irina Shishko]] [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

## The question Irina put

Val: "Теперь [MVP] 2. Гвоздь программы это вай фай." Irina: is MVP 2 Flex IQ or Flex Pay? "у нас сейчас там это на самом деле flex pay идёт как [MVP] 2." [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]

## Val's answer

- **Not Flex Pay.** "Мы с Андреем говорили… Андрей считал, что нужно делать [F]lex pay. Но я считаю, что нужно больше отполировать" Flex IQ and Wi-Fi; "я бы хотел, чтоб [MVP] 2 зашёл в игру быстрее чем ковыряться сейчас с флекспей." [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]] *(This "Андрей" is [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] by context — on Oct 14 he framed MVP 2 around the slim dispensers with Flex IQ — **inference**; the notes flag it unconfirmed.)*
- **The list.** "Я бы не включал флекс пей, я бы включал бы только флекс IQ. Вай фай конфигур[ация]. [Remote update], включая flex порты. И включая ай кю. И Galaxy [transactional] довёл бы до такого порядка, что мы можем делать репортин… даш борды" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]. Diagnostics were put into MVP 2 earlier in the meeting — [[wiki/decisions/2026-10-15-service-diagnostics-go-to-the-cloud-with-role-based-access-not-to-the-local-screen.md]].
- **Remote update of the Flexports moves here.** MVP 1 keeps only the USB-stick update; Val: "в MVP 2 мы включим уже [remote] апдейт [на] flex порты." Pavel: "Да." — [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Oct-15, 11:04 AM update) [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **Wi-Fi starts with the switch and an external router** — [[wiki/decisions/2026-10-15-flex-iq-gets-a-switch-between-its-own-access-point-and-an-external-router-and-mvp2-starts-on-the-router.md]].

## The location's bank shortfall

- **Val.** "Там важный момент для [Nathan] нужно доделать": if a location has too little money on its account for JVL to draw, "чтобы можно было снять с кредитной карточки" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **Pavel's way.** Nathan is not needed for this part: show it on the location's own dashboard page, so the operator, logging in to the location, "увидел это и нажал кнопочку оплатить… используя сервис там страйп" with his own card, then send a notification to [[wiki/people/nathan-carver.md|Nathan]]'s module "чтобы он отразил это в инвойсах" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]. Stripe was his example ("например"), not a choice.
- **Val adds the guarantor.** "мы хотим самого оператора сделать гарантёром за этот перевод" — if the location does not pay and the card fails, JVL draws automatically from the operator, "подкрепить бухгалтерскими репортами". Pavel: reports "[с]вязанные с [MSBC]" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- This builds on the Oct-14 guarantor-account-and-card chain — [[wiki/decisions/2026-10-14-jvl-sets-the-location-daily-cap-backs-it-with-a-guarantor-account-and-a-card-and-the-automatic-location-block-is-mvp-1-5.md]] (Oct-15 update).

## Pace

- Val: "каждый промежуток между каждым [MVP] это гдето от 2 до трёх недель… Желательно 2 недели не больше." Irina: two weeks of development — and what about requirements and capabilities? Val: "Мне очень важно, чтобы разработка шла параллельно с тестированием." [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- **Requirements first (Irina).** In MVP 1 the requirements were rewritten "в такойто гонке"; for MVP 2 there are one or two capabilities so far. "Требования [capabilities] без них мы ничего не сделаем"; the sooner they start, the better, since the team knows where it stumbled [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **Who writes what (Val).** "Андрей может написать только [функциональные] [requirements]. [Requirements] мы должны [получить] от инженеры." [[wiki/people/andrey-bosik.md|Bosik]]: for Wi-Fi "львиная доля написана уже их просто надо пройтись проверить. Актуализировать" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

## People away

Pavel: for at least the next two weeks [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] and [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] are on vacation, so fewer people. Irina: "Лёша" must also work on the RIS re-issue ("перевыпуск… рис", garbled); "я остаюсь я одна". Pavel: start looking at the tasks and estimating [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

## Where it sits

- **Evolution of the MVP 2 frame.** On Sept 30 Pavel said MVP 2 is "исключительно добавление [FlexPay]" plus Wi-Fi ([[wiki/decisions/2026-09-09-one-transactional-unit-per-location-until-the-wi-fi-iteration.md]], Sept-30 update); on Oct 1 Biratka began porting Flex IQ's capabilities to Flex Pay for MVP 2, and on Oct 14 Klimovich framed MVP 2 around the slim dispensers ([[wiki/decisions/2026-10-01-mvp2-capabilities-biratka-ports-flex-iqs-to-flexpay-and-writes-no-new-ones-until-klimovich-defines-the-flows.md]]). Val now takes Flex Pay out. It is Val's view; the final list waits on his session with Andrei.
- Val's Oct-14 MVP 2 priority list (Wi-Fi, diagnostics, inspector report, nine cash-out categories, remote update, configurable options, SMS low-funds notices, contract signing) is on the Oct-1 page. Oct 15 restates its core and adds Galaxy reporting and the shortfall payment; the other Oct-14 items were not mentioned and are not dropped in words.

## Open commitments

- [ ] [[wiki/people/val-levitan.md|Val Levitan]] and [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (by context — inference) — finish the MVP 2 list; then Andrei starts work with the team — due unspecified — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]] [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — go through the MVP 1 / MVP 2 items tomorrow; take the MVP 2 mark off Flex Pay and relabel it MVP 3 (he said "из flexпорта"; Irina: "С флекс пэя ты ими хотел сказать") — due Oct 16 2026 — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] / [[wiki/people/irina-shishko.md|Irina Shishko]] — tell Andrei (Klimovich, by context — inference) the MVP 1 release date; he asked Val the day before and Val did not know what to say — due Oct 16 2026 (Irina: "наверное, мы завтра сможем") — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrei Bosik]] — review and update the Wi-Fi requirements already written, for MVP 2 — due unspecified (the notes mark the assignment "implied") — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]] [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]

## Open questions

- Who plans the next two weeks with fewer people (vacations, Lyosha on the RIS re-issue)? Pavel and Irina to look at the tasks — [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- What exactly goes into MVP 2 after Val's session with Andrei — the transcript's "все экспресс экс п email" (Pavel, on what gets the MVP 2 mark) is garbled — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]

**§15.8:** clear — scope, dates and staffing only; vacations are availability facts. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
