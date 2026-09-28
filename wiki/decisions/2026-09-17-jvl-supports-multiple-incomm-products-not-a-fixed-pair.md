---
type: decision
title: JVL supports multiple InComm card products, not a hard-coded pair — a collection of products per location on the payment hub, identified by the UPC in the barcode; MVP 1 delivers ONE product (owner ruling 2026-09-20)
date: 2026-09-17
aliases: [multi-product, мультипродукты от инкома, collection of products, UPC is the product, product not available, SkillPay, Skill Pay, скилл пэй, скилпы, PrizePay, прайс пэй, PricePay, activation fee two dollars three dollars, payment hub product collection, location manager UPC check, add product, per-product limits and fees, second payment provider, capability 178, InComm card configuration capability, two products will not be in MVP1, 178 must be MVP1, single product fallback, UPC plus card code, card number not used, if SkillPay stays on the market]
source-count: 5
status: active — the payment-hub multi-product design stands. Its MVP 1 SCOPE was contested on Sept 18 2026 and is now SETTLED by owner ruling 2026-09-20: two-product support is not in MVP 1.
open-commitments: 4
open-questions: 6
---

# InComm card products are a collection on the payment hub — and on Sept 18 the MVP 1 delivery of it was cut to one product

> **Read the Sept-18 update at the foot of this page before relying on the MVP 1 scope.** The design ruling — a product collection on the payment hub, the UPC carried in the barcode — is unchanged and still governs. What changed the next morning is how much of it ships in MVP 1.

Taken on the [[wiki/meetings/2026-09-17-transactional-mvp1-skillpay-multi-product-and-device-network-security.md|Sept 17 2026 8:02 AM call]] (Russian). [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] proposed the shape on a shared screen and [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] ruled it in, correcting himself mid-sentence to widen it.

## What forced it — InComm put SkillPay on the market

Klimovich opened with the context: "**ИНКОМ вчера запустили официально на рынок карточку skill pay**" — InComm officially launched the SkillPay card yesterday, i.e. **Sept 16 2026**. What it does: "**загружается карточка так же как [прайспей]… можно оплачивать продукты, товары, пользоваться в интернете, но в отличие от прайспей, теперь её можно вставить в любой сертифицированный [ATM] и получить на выход кэш. Это большое изменение на рынке**" — it loads the same way and spends the same way, but unlike the existing card it can be put into any certified ATM and turned into cash [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

**Two things follow, and Klimovich stated both.** First the demand read: "**вся логика подсказывает, что игроки с большим удовольствием будут хотеть именно ск[ил]л[ ]пей карту, а не прайс[ ]пей карту**" — so JVL obviously has to be able to issue it. Second the risk: "**Ещё непонятно, как регуляторы на это отреагируют**", and concretely — "**если через неделю её закроют, мы сейчас проделаем работу и выяснится, что она не поддерживается, и надо возвращаться обратно на прайс[]пей**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

That regulatory risk is the reason the fork was posed as *support both and let the location choose* versus *switch wholesale to SkillPay* — and it is the reason the answer went wider than either.

### The naming note — "прайс пэй" is the $2 card

The transcript renders the incumbent card as "прайс пэй / прайспей", which the derived notes transliterate as "**PricePay**" [[raw/Meeting_Notes_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]. Every attribute given for it on this call — **$2 activation fee**, the Georgia incumbent, no cash access — matches the product the corpus already carries as **PrizePay** ([[wiki/organizations/incom.md]], June 23 2025: "$2 activation fee, single-load, up to $1,000, no cash access", against SkillPay's "$3, has cash access"). These pages therefore call it **"the existing $2 card"** in the wiki's own voice and identify it as **PrizePay**, with "PricePay" and "прайс пэй" recorded as aliases. *(This identification is made from the corpus by the writer; it is **not** an owner ruling and no new product page was created for "PricePay". Flagged for the owner — if PricePay is genuinely a third, distinct InComm product, this note is the place to correct it.)*

## The two products differ, and the differences are not frozen

- **Activation fee differs today:** "**если [прайс]пей — это $2, то у скил[л ]пей карты это $3**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].
- **Load minimum and maximum are the same today and may not stay that way:** "**Мин[/]макс кепы загрузки на карту совпадают[,] пока это 5 и 1000, но не факт, что они такими останутся**" — **$5 and $1,000** [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].
- **Daily cap and velocity may differ per product:** "**Возможно[,] d[ai]ly cap[,] возможно[,] v[e]l[oc]ity отличаются по продукту**" — stated as possibility, not fact [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

Klimovich drew the conclusion that drove the design: the two products' settings "**должны существовать раздельно, чтобы их можно было настраивать независимо друг от друга**" — they must exist separately so they can be configured independently.

## Chudinov's shape — the UPC *is* the product

Looking at the location record on screen: "**у нас сейчас [U]PC представлен в виде единичного поля. По факту [U]PC — это продукт**" — today the location holds a single UPC field, and a UPC is in fact a product [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

His proposal, in his own words [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]:

- **Group the field into a collection:** "**добавить продукт[:] мы… нажимаем добавить продукт, [задаём] ему имя… вводим UPC, котор[ый] скажет ИНКОМ, и соответственно все лимиты по этому продукт[у]**". "**Мин[,] макс[,] фи — всё это можно будет различить, и [U]PC будет заши[т] свой.**"
- The whole section becomes the set of products a location supports: "**вся эта секция превратится… в под[м]ножество, и тут будут… поддерживаемые наборы, то есть продукты, которые поддерживают локации**".
- **The card's barcode already carries both parts:** "**в баркоде… одна часть — это UPC, 2 часть — это код карты. Соответственно, [при] скан[ировании] карты мы всегда знаем, какой UPC идёт.**"
- **So the cashier screen barely changes:** "**на экране ничего… не поменяется. Мы[,] просканиров[ав, ]будем автоматически с сервера получать актуальные ф[и] для этого [U]PC и всё отображать; можем даже… название продукт[а] и иконку отобразить.**"
- **And the check happens server-side, against the location:** the payment hub receives "**скан карты на такую[-]то сумму с таким[-]то [U]PC**", knows which location the terminal belongs to, and asks whether "**этот [лок]эйшн поддерживает этот [U]PC[;] если поддерживает, он разрешает транзакцию, если не поддерживает — соответственно, отклоняем[:] вам продукт недоступен**". Chudinov names the answering component the **location manager**, distinguishing it from the payment hub.

He put the build cost low: "**работа есть, но… не настолько существенная и критичная. Там в рамках одной [спринта?] всё решается**" *(the unit of work is garbled and is not reconstructed)*.

## The ruling, including the self-correction

Klimovich first asked whether the location logic changes so products can be added rather than two being hard-coded — "**это не то, что у нас будет сейчас жёстко заши[ты] 2 продукта**" — and Chudinov answered "**важно добавлять любые. Главное, чтоб ИНКОМ [всё] поддерживал**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

Then he ruled, and corrected himself in the same breath [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]:

> "**давайте мы примем решение, что для [MVP] один мы делаем поддержку 2 продуктов — нет, не 2. Мы делаем поддержку мультипродуктов от инкома. Мы это делаем на уровне payment хаба, добавляем туда коллекцию продуктов.**"

**A second payment provider is explicitly deferred, not designed for now.** Klimovich: "**[Ин]ком[.] Потом появится… у нас есть и другие провайдеры — там появится ещё один уровень**"; Chudinov agreed to wait — "**когда появятся другие провайдеры, уже будем посмотреть, как нам расширять… Возможно, продукты вообще переедут… отдельно, и мы будем просто их выбирать се[ле]кторами**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

Klimovich took the Jira write-up himself: "**этот к[а]п[абилити] имеет право жить… я его распишу**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

This extends, rather than replaces, the Sept-2 ruling that InComm cards are activated by barcode on Flex IQ ([[wiki/decisions/2026-09-02-activate-incomm-cards-by-barcode-on-flex-iq.md]]) — the barcode now also tells the terminal *which product* it is holding.

## What was deliberately NOT decided — where the cashier picks the product

The second half of the same discussion was the cashier's screen flow, and Klimovich parked it overnight: "**давайте мы ещё поспим с этой идеей… можем завтра вернуться к этому… флоу[,] подумать ещё раз, как сделать его удобным и желательно универсальным**", and "**давайте сейчас припаркуем это обсуждение**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

**Three positions were on the table and none won** [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]:

- **[[wiki/people/pavel.md|Pavel Frolov]] — no extra button, a product screen after the amount.** "**зачем нам кнопку здесь нажимать? Мы здесь можем отобразить 2 продукта со своими… фи[:] здесь така[я]-то[,] здесь така[я]-то[;] здесь опция, что вы сможете деньги получить, а здесь только [покупки]**… и здесь мы ожидаем просто сканирования[:] как только отсканировали… баркод карты, мы сразу идём по правильному воркфлоу**". His screen needs no Continue: "**Зачем континиу?**"
- **Chudinov — amount and product on one screen, because the amount decides the product.** "**не сойдётся, потому что ты ведёшь сумму, а конкретный продукт уже не подойдёт**", and therefore "**одним экраном решит проблему**". His picture: the keypad slides left, the available products sit on the right, and entering an amount "**автоматически отсеива[ет] один продукт, если он не удовлетворяет требованиям**". His worked example is the $1,500 case below: "**если вы выбираете этот продукт, это будет… 2 карточки[,] нулевой остаток, а если выбираете этот продукт, он будет одна карточка, и на [волете] останется такая-то сумма**".
- **[[wiki/people/andrey-bosik.md|Andrey Bosik]] — keep it automatic: maximum amount, best product pre-selected.** "**Всё равно высвечивать максимальную сумму по умолчанию и по умолчанию выбирать продукт**" — and when Pavel checked that he meant the product with the larger limit, "**По умолчанию здесь, да**". His analogy is a corporate fuel card at a Belarusian filling station (the transcript says "Беларусь нефть"): "**тебе же не говорят[:] выбери карту, которой ты будешь оплачивать… они просто ей чиркают по терминалу, и всё**". He also warned the one-screen version does not scale: "**если нас больше продуктов будет[,] представляешь, какой у тебя экран будет перегружен информации… а если у тебя 3 продукт[,] будет 4**".

**The fixed points everyone accepted**, stated by Klimovich: "**Это деньги игрока, и он всегда будет хотеть забрать всё. Если он выиграл $5000, он говорит[:] хочу все $5000**", and therefore it is good to say straight away which cards can carry the amount — "**ни одна из карточек не поддерживают 5[000]. Но вот эти поддерживают тысячу[:] ты можешь забрать сейчас тысячу, потом снова отсканируем твой ти[кет], заберёшь ещё тысячу, и так 5 раз**". Chudinov's alternative in the same breath: "**либо [прайспей] будет поддерживать 2 с половиной, и так вы можете забрать 2 карточки, а так 5 карточек**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

**Why the existing pre-fill rule breaks.** Klimovich restated the behaviour already written into the regulations for one product: take the redeemable balance, try to put all of it into the amount field, trim it to the product's max cap if it is bigger, and hang a banner saying the redemption exceeded the limit and the wallet can be scanned again. With **two different max caps** that rule silently decides for the player: "**если мы [вбиваем] максимальный макс, то мы можем… по дефолту отрезать один из продуктов сразу… здесь… мы уже приняли какое[-]то решение за игрока**". He floated leaving the field empty or at zero to force the conversation; Chudinov and Bosik both pushed back — "**Я бы делал дефолт всё равно максимум**", "**ноль по дефолту всё равно невозможен**", "**зачастую это будет 20[,] 50 баксов… Зачем тогда усложнять жизнь?**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

Pavel's compromise inside Chudinov's one-screen layout, also unadopted: the product selector on the right with the higher-limit product pre-selected, the redeemable shown as $1,500 with the issuable amount under it, and clicking the other card re-filling the amount to that product's maximum — "**сумма автоматически вбива[ется,] максимально доступная для данного продукта**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

*(The worked example — a player holding **$1,500** against one product capped at **$1,000** and another at **$1,200** — was posed by **Klimovich**, not by Chudinov: "**2 продукта[:] у одного макс лоуд 1000, у 2 — 1200, а у игрока было 1500**". The derived notes attribute it to Chudinov. Corrected here against the source.)* [[raw/Meeting_Notes_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

## Update, Sept 18 2026 — the capability has a number, and its MVP 1 scope is cut back to one product against Val's written instruction

At the [[wiki/meetings/2026-09-18-transactional-mvp1-capability-cleanup-and-the-monday-deadline.md|Sept-18 8:03 AM call]] this was the **first** item on the cleanup sweep, and it did not move forward.

**The capability is number 178.** Klimovich, filtering the board: "**Один [капабилити] прополз[ —] это ИНКОМ карт конфигур[ейшн капабилити]. Это то, что мы вчера обсудили[:] поддерживать несколько продуктов**", and when Bosik asked for the number, "**Да[,] 178 — это то, что мы вчера обсуждали про появление нового продукта инкома**". *(The Sept-17 recording never gave it one.)* [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

**He would not advance it, and named both possible outcomes:** "**Я его не готов перевести дальше[:] пока он или вообще уедет на [MVP] 2, или… в каком[-]то супер урезанном [виде] останется в [MVP] один**"; "**он не доработан, он не может переехать дальше, он требует ещё работы**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

**Then, later in the same call, he went further than he had on Sept 17** — prompted by [[wiki/people/dmitri-chudinov.md|Chudinov]] naming the two-product, two-card requirement split as one of his two biggest blockers ("**они визуально… сильно меняют логику значительно**") [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]:

> "**я склоняюсь к тому, что 2 продукта мы к [MVP] один не будем делать[.] Я могу вам почти уже финально это заявить.**"

**Val's chat message says the opposite, and was read out in the room.** [[wiki/people/irina-shishko.md|Irina Shishko]]: "**178 — [маст би MVP] один**"; Klimovich asked what that was; [[wiki/people/pavel.md|Pavel Frolov]] confirmed "**Это текст от Вала**". [[wiki/people/val-levitan.md|Val]] did not speak on this recording — he was in the meeting chat [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

**Klimovich's answer was a fallback, not a reversal:** "**мы можем сделать поддержку одного продукта, например, всё[-]таки[,] просто у нас сейчас уже всё работает. Мы можем сделать поддержку [скилпей]**" — a single product, **SkillPay**, because it already works end to end. Pavel costed that small: "**со стороны сервера это можем очень легко сделать[,] в интерфейс добавить для оператора**", needing "**данные по карточкам**" from InComm and a graphical check, "**и с точки зрения бэкэнда это будет сделано**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

**Nothing was reconciled.** Irina cut the discussion off to keep the meeting moving — "**давайте мы не будем сейчас это много говорить**", "**чтоб… не переливать из пустого в порожнее**" — and the only action recorded is that Klimovich finishes 178's window designs: "**Андрей делает[,] заканчивает окна 178 [капабилити]**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

**What the Sept-18 call did NOT touch:**

- **The cashier's product-selection flow** — parked overnight on Sept 17 with a commitment to bring it back to "tomorrow's call". **Tomorrow's call is this one, and it never came back.** The commitment stands undischarged and the three positions are untouched.
- **The naming question.** The incumbent $2 card is **not named at all** on Sept 18 — only "**скилпей**" is spoken. The "прайс пэй / PricePay"-versus-**PrizePay** identification recorded above therefore gains no new evidence in either direction and stays exactly as it was. **Not resolved.**
- **The SkillPay test card, the InComm documentation request and the broker-verification email thread** — none is mentioned.

## How the 178 scope question was settled

**RESOLVED by owner ruling, 2026-09-20 — Klimovich's position is correct.** Asked directly, the owner ruled: **"Klimovich is correct."** Capability 178 / two-product support is therefore **NOT in MVP 1**; the owner's own Sept-18 chat instruction that "178 must be MVP 1" is **withdrawn by the same owner** and moved to History below. The multi-product payment-hub design itself is unaffected — it stands as the architecture, and only its MVP 1 *delivery* is cut back to a single product. *(An owner ruling is its own citation — §16. No source in `raw/` records it.)*

**Residual, NOT ruled on:** Klimovich's stated fallback was to support **SkillPay** alone ("Мы можем сделать поддержку скилпы"). The owner endorsed his position but did not separately name which single product MVP 1 ships, so that is left as an open question rather than inferred.

### History — the two positions before the ruling (Sept 18 2026, same hour, neither withdrawn at the time)

- **[[wiki/people/val-levitan.md|Val Levitan]], in the meeting chat:** "**178 — [маст би MVP] один**" — it must be in MVP 1 [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].
- **[[wiki/people/andrei-klimovich.md|Andrei Klimovich]], aloud, minutes later:** "**2 продукта мы к [MVP] один не будем делать[.] Я могу вам почти уже финально это заявить**" — near-final that two products are not built for MVP 1 [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

## Update, Sept 21 2026 — the room still calls it undecided; the code is built for many products

On the [[wiki/meetings/2026-09-21-transactional-mvp1-flexport-and-iq-ux-design.md|Sept-21 call]], the day after the owner ruling, [[wiki/people/dmitri-chudinov.md|Chudinov]] asked whether MVP 1 does multi-product on cards. [[wiki/people/andrei-klimovich.md|Klimovich]]: "Я не знаю, надо сегодня это решить. Мы не дожали этот вопрос." His fallback is unchanged: if the screens are not ready, "мы сделаем поддержку просто одного продукта… скорее всего, это будет скилпей, если он останется на на рынке." Chudinov: "реализацию мы закладываем на мультипродукт просто не знаем, будем ли использовать" [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]].

**This does not reopen the owner ruling.** The ruling (two-product support is not in MVP 1) stands; the room had simply not been told, or had not yet closed it in Jira. *(Inference.)* It adds one data point to the residual point recorded under "How the 178 scope question was settled": Klimovich again names SkillPay as the likely single product, with a condition — if SkillPay stays on the market.

**The barcode layout is confirmed from the card-search design.** Chudinov: the barcode carries "юпис плюс карткод" — the UPC plus the card code. Klimovich: the card number "у нас походу вообще нигде нет", so JVL works with the card code everywhere [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]. That fits the UPC-is-the-product shape above.

## Open commitments

- [x] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — finish the reworked window designs for capability 178; Chudinov named them as his single biggest blocker — due **Monday Sept 21 2026** — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]] — **discharged in substance Sept 21 2026:** the reworked Flex IQ and Flex-Port screens were walked on the call, functional side fixed, polish and Jira load still to come; no separate two-product screens were shown, which the owner ruling makes moot for MVP 1 — [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — write the multi-product capability up in Jira (a product collection on the payment hub) — due unspecified; **partly advanced on Sept 18** — the capability exists as **178** and is being worked, but Klimovich called it "**не доработан**" and refused to move its status — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — rethink the cashier UI flow for choosing the product and bring it back to tomorrow's call — due **Sept 18 2026**; **the Sept-18 call came and went without it being raised — overdue and unmentioned** — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — find a production SkillPay card with a barcode and swipe it on a Flex IQ so Chudinov can read the logs and see what the magnetic stripe carries; his own test card has no barcode yet — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — open a new email thread to InComm saying JVL is ready to support SkillPay, and ask for the documentation and test cards, **including two test cards of different products with different UPCs** (Chudinov's request); thread to include Pavel Frolov, Chudinov, Irina Shishko and Sergei — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

## Open questions

- **Where on the cashier flow the product is chosen.** Parked overnight; three positions on the table, none adopted — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- **What the amount field pre-fills when two products have different max caps** — the higher cap (which silently rules a product out), the lower one, or nothing — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- **Whether SkillPay uses the same InComm endpoint as the existing card.** Pavel: "**надо будет уточнить[,] такой же IP у них или нет для этого продукта**"; Chudinov answered only that "**UPC передаётся в контракте**" — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- **Whether a SkillPay card carries the UPC on its magnetic stripe.** Needs a production card swiped and the logs read; Chudinov: "**если [UPC] там не появился, то… дилемма[:] как узнавать, что за продукт?**" — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- **How regulators respond to a card that cashes out at any ATM.** Nobody knows, and Klimovich named the risk that the product is closed a week after JVL builds for it — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

**§15.8:** clear — card-product economics (activation fees, load limits) are product economics, not any named person's pay; no compensation or performance judgement appears. **§15.9:** no UPC value, card number, endpoint address or credential was spoken — UPCs and card numbers are discussed only as *fields* in a barcode.

## Sources

- [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]
