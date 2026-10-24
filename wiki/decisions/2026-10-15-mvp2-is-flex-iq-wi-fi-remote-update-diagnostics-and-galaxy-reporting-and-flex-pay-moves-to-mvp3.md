---
type: decision
title: Val's MVP 2 — no Flex Pay; Flex IQ, Wi-Fi configuration, remote update for the Flexports and Flex IQ, diagnostics, Galaxy transactional brought up to reporting and dashboards, and the location's bank shortfall paid by card with the operator as guarantor — Flex Pay is retagged MVP 3, and each MVP takes two to three weeks with testing alongside development
date: 2026-10-15
aliases: [MVP 2 scope Oct 15, no Flex Pay in MVP 2, Flex Pay to MVP 3, retag Flex Pay MVP 3, гвоздь программы это вай фай, Wi-Fi is the centrepiece of MVP 2, remote update of Flexports moves to MVP 2, Galaxy transactional reporting and dashboards, location shortfall paid by card, Stripe on the location page, operator as guarantor, two to three weeks per MVP, desirably two weeks, development in parallel with testing, Andrei writes only functional requirements]
source-count: 6
status: active — Val's view, subject to the final MVP 2 list he is polishing with Andrei (Klimovich, by context — inference); Oct 16 2026: Pavel reported MVP 2 as only Wi-Fi and remote port update through Flex IQ, with Flex Pay renamed MVP 3 — the width of MVP 2 is an open contradiction (see the Oct-16 update)
open-commitments: 7
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

- [ ] [[wiki/people/val-levitan.md|Val Levitan]] and [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (by context — inference) — finish the MVP 2 list; then Andrei starts work with the team — due unspecified — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]] [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]] — *Oct 16 2026: Pavel reported a two-task MVP 2 from "yesterday's coordination meeting"; whether that was the finished list is not said* — [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — go through the MVP 1 / MVP 2 items tomorrow; take the MVP 2 mark off Flex Pay and relabel it MVP 3 (he said "из flexпорта"; Irina: "С флекс пэя ты ими хотел сказать") — due Oct 16 2026 — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]] — *Oct 16 2026: Pavel told the stand-up that Flex Pay, until now MVP 2, "Переименован в 3"; whether the Jira marks were changed is not said, so left open* — [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]] — *Oct 19 2026: Irina said Flex Pay still sits in MVP 2 in Jira; she takes the move over herself (see the Oct-19 update)* — [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] / [[wiki/people/irina-shishko.md|Irina Shishko]] — tell Andrei (Klimovich, by context — inference) the MVP 1 release date; he asked Val the day before and Val did not know what to say — due Oct 16 2026 (Irina: "наверное, мы завтра сможем") — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrei Bosik]] — review and update the Wi-Fi requirements already written, for MVP 2 — due unspecified (the notes mark the assignment "implied") — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]] [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]

## Open questions

- Who plans the next two weeks with fewer people (vacations, Lyosha on the RIS re-issue)? Pavel and Irina to look at the tasks — [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- What exactly goes into MVP 2 after Val's session with Andrei — the transcript's "все экспресс экс п email" (Pavel, on what gets the MVP 2 mark) is garbled — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]

**§15.8:** clear — scope, dates and staffing only; vacations are availability facts. **§15 #9:** none.

## Update, Oct 16 2026 — Pavel to the Minsk stand-up: MVP 2 is "only" two tasks; Flex Pay is renamed MVP 3; three weeks

At the [[wiki/meetings/2026-10-16-daily-standup-mvp2-wi-fi-scope-and-modem-mac-rollback.md|Oct-16 Minsk stand-up]] (Russian; Val absent), after Irina asked about the MVP 2 capabilities, [[wiki/people/pavel.md|Pavel]] reported on "вчера был митинг координационный по поводу транзакшного продуктов" [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]:

- **The rename.** "то, что до сих пор называлось MVP 2, то есть флекс пэй. Переименован в 3."
- **The scope.** "в мвп 2 попадает исключительно там 2 задачи это поднятие вай фай. На flex спартах вайфай на флекс IQ. И ремонт апдейт портов через fex IQ." (The notes read "ремонт апдейт" as remote update [[raw/Meeting_Notes_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]].)
- **Why.** "вал не хочет миксовать всё вместе. Это будет потому что сложно всё параллельно и проверять, и. Там запускать".
- **How long.** "ближайшие 3 недели это будет вот какието улучшательства по флекс ай q портам включая вайфай. И включая ремонт апдейт". With Chudinov back from vacation only in a week, Pavel will see whether to reshape the work, for example by giving Sergey some tasks.
- **Requirements.** Check which capabilities and requirements exist and create the missing ones: "Большинство из этих требований… не функциональное. Поэтому мы сами можем отгенерировать." [[wiki/people/irina-shishko.md|Irina]] will finish the tests she started, then look at the MVP 2 capabilities.
- **The payment hub, not in this list.** Pavel said the payment hub came up "вчера" too: [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]]'s experiment with Stripe and card payment "тоже надо будет делать", but no timeline was set, and "нейтану чтото надо будет доделать" ([[wiki/people/nathan-carver.md|Nathan]]). Sergey: it runs through the billing service; the open part is the UI — pay one unpaid invoice, a list of unpaid ones, part-payment. Pavel: "давай пока не будем фокусироваться. Давай сначала вот рисом занимаемся"; later, have Claude draw the screens from existing ones and show them "валу, показать Андрею" (this Andrei is not identified — Klimovich is likely, **inference**). Sergey has looked only at Stripe; fees differ by vendor. Pavel: Stripe "один из самых самых крупных по Америке". Which MVP this belongs to was not said. This bears on the location shortfall paid by card, above.

The notes record the scope as "Decided by Val, reported by Pavel Frolov", and the payment-hub wait as Pavel's decision [[raw/Meeting_Notes_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]].

### Open contradictions (Oct 16 2026)

- **How wide MVP 2 is.** On Oct 15 Val listed Flex IQ, Wi-Fi configuration, remote update of the Flex-Ports and Flex IQ, diagnostics, Galaxy transactional reporting and dashboards, and the location shortfall paid by card [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]. On Oct 16 Pavel reported that MVP 2 holds "исключительно" two tasks, Wi-Fi and remote port update through Flex IQ [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]. Pavel's "coordination meeting" may be a later session that narrowed the list (for example Val's session with Andrei), or the same Oct-15 talk retold — not said. Both are kept; nothing resolved.

### Open commitments (Oct 16 2026)

- [ ] The Minsk team (Pavel) — check the MVP 2 capabilities and requirements and create the missing ones, mostly non-functional — due within the next three weeks — [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]] [[raw/Meeting_Notes_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
- [ ] [[wiki/people/irina-shishko.md|Irina Shishko]] — finish her open tests, then review the MVP 2 capabilities — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]

## Update, Oct 19 2026 — Flex Pay still sits in MVP 2 in Jira; Irina moves it herself; tests for MVP 2

At the [[wiki/meetings/2026-10-19-daily-standup-clover-fortune-on-nova-and-encrypted-settings-qr.md|Oct-19 Minsk stand-up]] (Russian; Val absent) [[wiki/people/pavel.md|Pavel]] told [[wiki/people/irina-shishko.md|Irina]]: "нам надо уже для MVP 2 создавать", review which capabilities and requirements exist, "Тебе нужны будут тесты." Irina: "у нас на MVP 2 стоит пей, а нам нужен то, что стоит на MBP 3". The capabilities are Andrei's ("Андрей же capaбилити за это заведует" — which Andrei is not said; **not identified**), "но если мы его будем ждать, мы ещё… Год будем ждать." So she will move Flex Pay to MVP 3 herself and re-sort what fits. Pavel: "Да да… надо самим. Самим пересмотреть." [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]

The notes record it as Irina's decision with Pavel agreeing: "The team moves Flex Pay to MVP3 itself instead of waiting for Andrei" [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]. Nothing new was said on the width of MVP 2; the open contradiction above stands.

### Open commitments (Oct 19 2026)

- [ ] [[wiki/people/irina-shishko.md|Irina Shishko]] — move Flex Pay to MVP 3 in Jira, re-sort the MVP 2 capabilities, and create the MVP 2 tests — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]

## Sources
- [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
