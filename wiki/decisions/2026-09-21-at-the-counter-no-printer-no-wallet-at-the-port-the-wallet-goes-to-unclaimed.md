---
type: decision
title: No paper in the printer is handled two ways — at the counter Flex IQ checks the printer first and creates no wallet if it cannot print; at the Flex-Port the wallet is created and sent to unclaimed, where the cashier prints it
date: 2026-09-21
aliases: [no paper in the printer, нет бумаги в принтере, check the printer first, wallet not created if printer fails, printer check before wallet, cashier flow printer check, FlexPort cash-out to unclaimed, скидываем в анклейт, print from unclaimed, wallet invalid if not printed, воли инвалидный, он 2 раз к тебе не придёт, reprint later rejected]
source-count: 2
status: active
open-commitments: 1
open-questions: 1
---

# At the counter: no printer, no wallet. At the port: the wallet goes to unclaimed.

Settled at the [[wiki/meetings/2026-09-21-transactional-mvp1-flexport-and-iq-ux-design.md|Sept 21 2026 8:02 AM call]] (Russian). It took longer than any other point on the call [[raw/Meeting_Notes_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]].

## The question

[[wiki/people/irina-shishko.md|Irina Shishko]] asked it: "если нет бумаги в принтере. Начал создавать volet что будет?" — what happens if there is no paper and a wallet is being created? [[wiki/people/dmitri-chudinov.md|Chudinov]] answered at once: "Не создаст. Принтер бросит ошибку, и ошибка будет волят не может быть создан." [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]

## Klimovich's first design, and why it lost

[[wiki/people/andrei-klimovich.md|Andrei Klimovich]] wanted to create the wallet anyway and let the cashier reprint: "мы можем создать его лет, бросить ошибку после создания… его лит создан, он падает в не детеншн и оттуда можно сделать репринт, перезагрузить бумагу." His view: the player has paid, so "он дождётся перезагрузки бумаги" [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]].

**Irina objected hard.** The cashier has taken real money and given nothing back: "ты как кассир забрал деньги и теперь сказал иди гуляй", and "Он 2 раз к тебе не придёт." Later: "Когда человек к тебе пришел с деньгами, это реальные деньги, ты у него отбираешь их и ничего не даёшь взамен, а говоришь посиди на стульчике, подожди." [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]

**Chudinov agreed with her:** "принтер бросил ошибку, всё значит не напечатано и воли инвалидный." His reason goes past this release: if the server creates a wallet that the terminal then fails to print, "не транзакция должна быть… В одну транзакцию все происходит с подтверждениями." [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]

**[[wiki/people/pavel.md|Pavel]] gave the practical picture:** the cashier hands the money back, says wait, and does a new transaction once the paper is loaded — "Вроде логично." [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]

## The port is different, and everyone agreed why

Irina then asked about a player who went straight to a machine, played, and pressed print. Chudinov first said the port should also report a wallet-creation error. Irina stopped that: "у нас же с флекс порта деньги не возвращаются, они ж просто пропадут тогда." Chudinov saw it: "он не может больше поиграть." Pavel stated the rule, and Chudinov agreed: "в любом случае, где мы не можем перечислить деньги на его лет на порте мы это всё скидываем в анклейт, а из анклейт уже может напечатать кассир." — "Да, согласен." [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]

## The rule, as Klimovich closed it

Klimovich accepted: "Хорошо… давайте так и сделаем." [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]

- **Cashier flow (Flex IQ at the counter):** "мы сразу делаем проверку на принтер, и если принтер не может распечатать carver, то мы сразу не создаём и уволят. Это случай работы с кассиром."
- **Flex-Port cash-out:** "То мы создаем уволится. Отправляем его на ну к кассиру, а там они уже с кассиром разбираются."

He said he would change the requirement: "окей, я поправлю эту, хорошо?" [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]

## How this fits the earlier rulings

- **The port half confirms Sept 14.** On the port, the wallet is still created before the ticket prints, so a dead printer cannot lose the money — [[wiki/decisions/2026-09-14-the-ewallet-is-created-before-its-ticket-prints.md]].
- **The counter half matches what FlexPay already did.** On Sept 14 Chudinov said FlexPay puts wallet creation inside the output transaction: no printer, no wallet — see the same page. Sept 21 applies that to the Flex IQ counter. *(This link is an inference from the two pages, not something said on Sept 21.)*
- **Unclaimed.** Sept 15 put the unclaimed-money handling out of MVP 1 ([[wiki/decisions/2026-09-15-a-timeout-sends-the-money-to-unclaimed-and-the-player-never-loses-it.md]]). Sept 21 routes a failed port print to the unclaimed screen inside the MVP 1 screen walk. See the open question below.

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — change the wallet-creation requirement so the cashier flow checks the printer before creating the wallet — due unspecified — [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]

## Open questions

- **Does the "send to unclaimed, print from unclaimed" port path bring part of the unclaimed-money handling into MVP 1?** Sept 15 said unclaimed money is not MVP 1; Sept 21 designs this path in the MVP 1 screen walk without saying which release it belongs to — [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]

**§15.8:** clear — money-flow design only; no pay, rate or personal judgement. **§15 #9:** no identifier appears.

## Sources
- [[raw/Meeting_Notes_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]
