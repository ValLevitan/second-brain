---
type: decision
title: Flex-IQ activates InComm cards by barcode, and reports drop the 16-digit card number for the barcode identifier
date: 2026-09-02
aliases: [barcode activation, activate cards by barcode, drop the 16-digit number, barcode identifier on the dashboard, scanner to the front panel, sealed card packaging]
source-count: 2
status: active
open-commitments: 3
open-questions: 2
---

# Flex-IQ activates InComm cards by barcode, and reports drop the 16-digit card number

The first of the three pre-pilot changes [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] brought to the [[wiki/meetings/2026-09-02-flex-iq-pre-pilot-updates-after-the-show.md|Sept 2 2026 pre-pilot call]]. It closes the wrapped-card blocker found at the Georgia show ([[wiki/decisions/2026-08-21-release-flex-iq-as-is-place-units-collect-facts.md]]) and is driven by [[wiki/organizations/incom.md|InComm]]'s packaging rule.

## What was decided

- **Activation runs off the barcode, for Flex-IQ only.** Andrei: "1. Главное это мы должны активировать карты инкома через баркод." The reason is the packaging: cards for non-kiosk devices ship sealed and "никто, Кроме финального получателя игрока, не имеет права распаковывать её. Соответственно наружу в этой карточке торчит только баркот" — nobody but the final recipient, the player, may unwrap it, so only the barcode is exposed [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- **Kiosks are explicitly out of scope and keep today's flow.** "Для киосков мы сейчас это не обсуждаем… в киоск карточке загружаются уже распакованные и то, как они у нас сейчас активируются, это пускай так и остаётся. Речь идёт только об айкью" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- **Reports and the operations dashboard drop the 16-digit number.** Andrei: "Опервешен олдешборд есть эти идентификаторы карты, и мы уберём всё, связанное с… Шестнадцатизначным номером и Добавим туда идентификатор, который на баркозе есть. То же самое думаю, можно брать 4 последние цифры номера, которые под бар кодом хранится" — remove everything tied to the 16-digit number, add the identifier carried on the barcode, and show the last four digits of the number held under the barcode. Pavel had asked for exactly this: "соответствующий репорт, чтобы был не по номеру карты, а по идентификатору" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- **The scanner moves to the front panel.** Andrei: "Геннадий уже придумал. Мы ждём на следующей неделе новые борды, которые позволят нам вывести сканер на переднюю панель." [[wiki/people/val-levitan.md|Val]] specified the geometry: "этот паркот мы поворачиваем на 90 градусов, и выносим… вперед" and, against Pavel's worry that 90 degrees would shine in the player's face, "мы не в лицо свете мы светим вниз, только вместо Того, чтобы светить, так мы светим вот так" — aimed downward, not at the face. Pavel accepted: "Всё понял" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].

## The objection that was raised and settled on the call

[[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (speaker label "Dzmitry Chudzinau") objected that the barcode does not carry the card number in the form a user recognises: "сканирование вот текущей карточки штрихкода не содержит, номера карточки вот в привычном понимании пользователя, то есть где мы впоследствии на дашбордах там отображаем последние 4 символа карты, как это сделано у визы мастеркард" — so the last-four-digits convention that Visa/Mastercard and banks use would be unavailable, and "расследование какихто событий" (incident investigation) would be hampered. Pavel extended it: if the real card carries both a card number and a barcode number, matching them would let the dashboard show the barcode's last digits and still find the card [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].

Val attacked the premise rather than the detail — "А почему ставится этот вопрос?" and then "почему вы так пришли к этому анализу? Что вас привело… к результату, что юзер после Того, что ему дали карточку, придёт обратно на лакейшен и скажет, что мне с этой карточкой делать?" He also rejected the framing that JVL is in the loop at all: "Это выдавал её ИНКОМ… мы вообще к этому ничего общего не имеем" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].

Andrei settled it with two answers:
1. **In real life the player calls InComm, not the location.** "то, что вы… описываете это в жизни совсем подругому работает… И локации до этого никакого дела. Единственное, что я могу сделать, это звонить напрямую инкому и жаловаться" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
2. **The card and the envelope carry the same barcode**, so reconciliation still works: "на карточке физически находится баркот ровно такой же, который находится на конверте, поэтому у нас после активации карточки даже по баркоду есть достаточное количество идентификаторов, чтобы забить в базу и чтобы… Администратор… мог визуально понять, о чём идёт речь" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].

Pavel closed it — "Все вопрос снят" — and Irina Shishko: "Всё это и хотели услышать" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].

## Implementation state as of the call

- **Scanning already works on JVL's own test cards.** Dmitri Chudinov: "Тестовая карта я пробовал уже сканировать всё у нас да всё работает," having built "Тестовый аппликейшн на сканирование штрихкода"; what remains is "Доработать функционал вместо свайпа сканирования" — change the function from swipe to scan [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- **His effort estimate is garbled in the transcript** — "По поводу реализации. Ну, в течение 13:00 можно сделать" — the derived summary note reads this as about an hour. Recorded as **unclear**; the only firm commitment he gave is end-of-week for all three IQ changes [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]] [[raw/Meeting_Notes_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- **Card scanning is the least risky of the three items.** Chudinov, on the plan-B scenario: "со сканом карточки проблем не будет точно" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- **Why the requirement appeared at all** — Andrei, asked by Chudinov: "изменились требования у инкома, они теперь… Поставляют их в вот в таком виде, и если это не киоск, он должен работать с такими карточками, упакованными" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].

## Open commitments

- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — replace the swipe path with barcode scanning in Flex-IQ and repoint the reports/operations dashboard onto the barcode identifier — due end of week — [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — re-verify barcode activation with InComm by activating a couple more cards ("Мы проверим это ещё раз с инкомом, сделаем ещё активацию карточки парочки") — due unspecified, ahead of the pilot — [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — test the new IQ build first thing Tuesday, Monday being a public holiday on his side — due Tuesday — [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]

## Open questions

- Should the scanner be angled slightly forward rather than straight down, so wider items than a card (Pavel's example: a ticket) can be presented? Pavel: the beam "рассчитан на довольно узкую картинку, даже если его повернули на 90 градусов" and asked to "сканер направить чутьчуть вперёд под углом." Andrei deferred it — "Обсуждаемо, конечно, обсудим, когда дело дойдёт до этого" — and questioned whether JVL even has a business requirement to redeem tickets from third-party machines: "Я не уверен, что у нас вообще есть такой бизнес требование… Мы обсуждаем только полностью клоузлуб системы" — [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- Does the scanner remove the swipe entirely? Chudinov asked; Andrei: "Ну я не знаю, снимается он или нет, но он мне нужен… В данном видении" — he does not know whether swipe goes, only that he needs the scanner in the current vision. **Unresolved** — [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]

## Sources
- [[raw/Meeting_Notes_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
