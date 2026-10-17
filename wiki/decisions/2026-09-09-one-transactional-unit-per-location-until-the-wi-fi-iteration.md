---
type: decision
title: In the first iteration a location gets either FlexPay or Flex-IQ, never both — multiple units per location were to arrive in the second iteration with Wi-Fi; on Sept 30 2026 Pavel placed them in a probable MVP 3, with Wi-Fi staying MVP 2
date: 2026-09-09
aliases: [either Pay or IQ not both, one unit per location, serious engineering fork, single copy per location, second iteration with WiFi, the bundle delivered in stages, machine port IQ or machine port Pay, two devices per location MVP 3, MVP 2 is exclusively adding FlexPay, исключительно добавление флекспэя]
source-count: 8
status: active — the one-unit limit stands; the "second iteration with Wi-Fi" timing for multiple units was moved to a probable MVP 3 on Sept 30 2026 (see update); Oct 15 2026: Val takes Flex Pay itself out of MVP 2 into MVP 3, so the Sept-30 "MVP 2 is exclusively adding FlexPay" no longer holds
open-commitments: 1
open-questions: 0
---

# One transactional unit per location in the first iteration — FlexPay **or** Flex-IQ

[[wiki/people/pavel.md|Pavel Frolov]] raised it at the [[wiki/meetings/2026-09-09-september-resource-plan-and-flex-port-readiness.md|Sept 9 2026 7:02 AM call]] as the engineering consequence of the bundle Val had just described, and called it a fork: "[с] точки зрения инженерии[,] здесь сейчас у нас серьёзная развилка" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].

## The limit

- **Either device can be adapted quickly; only one of them can be at a location.** Pavel: "[н]аш флекс[-]пэй[,] так же как флекс IQ[,] можно относительно быстро доработать, чтобы они работали с флекс[-]портами. **Но в единственном экземпляре, то есть на лакейшн[,] нельзя поставить айкью плюс flexpay**" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].
- **Irina read the two permitted shapes back** — "[т]о есть смотри[,] 1 получается[,] может быть машина[,] порт[,] айкью… либо" — and Val completed it: "и[ли] машина[,] порт[,] п[э]й" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].
- **Multiple units per location come in iteration two, with Wi-Fi.** Pavel: "во 2 итерацию, когда мы, например, хотим вайфай внедрить[,] вот тогда мы можем делать доработку IQ плюс [с]пей[,] можно на лакейшн ставить несколько" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].
- **Val accepted it and offered to pre-run the wiring.** "Да[,] я могу это сделать[,] могу и могу пока проложить провода… под W[S]U протокол[,] параллельные" — he can lay the parallel wiring for the WSU protocol now [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]. *(The protocol name is rendered "w sc" in the transcript and "WSU" in the derived notes; recorded as the notes give it [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].)*

## Val restated it to the sales and hardware group ninety minutes later

At [[wiki/meetings/2026-09-09-october-rollout-staging-and-unit-ramp.md|8:43 AM]] — the derived notes record it as the hard constraint he restated to that group [[raw/Meeting_Notes_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]] — "In order to install October first, we cannot install Flex IQ and Flexport. We need to choose either Flex Pay or IQ. **But our offer still stands. It's just we have to do it in stages**" [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]. Asked what it means for the sales pitch, he was explicit that the promise does not shrink — "our sales pitch will be[,] yeah, we're giving you both. But first release, we wanna test. We wanna parse it out and test it. Yeah, we'll make it work" — and that IQ-plus-Pay is "for November first" [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]].

Asked in the engineering call what else he should stop promising in the market — "какая ещё есть проблема, что я могу на рынке что[-]то толкнуть?" — Pavel named this and only this: "[н]у лимитэйшн пока то, что мы это обсудили… [л]ибо [ай]кю либо пэй" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].

## Where it lands elsewhere

- The **printer fallback** in the rollout meeting rests on this limit — "we know that both do not work together. So it's either installing this or this" — see [[wiki/decisions/2026-09-09-the-mould-without-the-screen-comes-first-and-the-printer-has-a-fallback.md]].
- The Wi-Fi iteration it defers to is on [[wiki/decisions/2026-09-09-wi-fi-is-second-in-urgency-and-october-november-run-wires.md]] and [[wiki/decisions/2026-09-07-wi-fi-module-on-flex-port-with-an-external-router.md]].
- The bundle whose delivery is now staged is on [[wiki/decisions/2026-09-02-free-ports-and-pos-with-every-machine-bought.md]].

## Update, Sept 30 2026 — MVP 2 is "exclusively adding FlexPay" plus Wi-Fi; two devices at one location slip to a probable MVP 3

At the [[wiki/meetings/2026-09-30-transactional-mvp1-instructions-complete-and-modem-supply.md|Sept-30 8:03 AM MVP 1 call]] (Russian) [[wiki/people/andrei-klimovich.md|Klimovich]] sketched MVP 2 as he will take it up on his return: "в [MVP] 2 там будет акцент на [FlexPay] [в] [слим-факторе], и чтобы там актуальные все экраны были flow, всё был чистенько аккуратненький." Then: "Мы отложили на MVP 2 поддержку 2 устройств на одной локации помоему… или это позже ещё уехала." [[wiki/people/pavel.md|Pavel]]: "**Это наверное 3 будет уже**… [MVP] 2 это исключительно добавление [FlexPay]. [В]се остальное это уже [MVP] 3." Klimovich: "А вай фай коннект мы хотели помоему на [MVP] 2." Pavel: "Да да." Klimovich: "Вот это… главная такая будет [фича]" (garbled) [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]].

**Against the title.** The titular "multiple units per location arrive in the second iteration together with Wi-Fi" is now split: Wi-Fi stays MVP 2 ([[wiki/decisions/2026-09-07-wi-fi-module-on-flex-port-with-an-external-router.md]], Sept-30 update); multiple units per location go to a probable MVP 3 ("наверное"). Klimovich's "Окей" is acceptance, not a ruling. Recorded as evolution; the one-unit limit itself is unchanged. The derived notes read it the same way [[raw/Meeting_Notes_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]].

## Update, Oct 15 2026 — Flex Pay itself leaves MVP 2

At the [[wiki/meetings/2026-10-15-wi-fi-router-switch-power-loss-battery-and-mvp2-scope.md|Oct-15 11:04 AM Wi-Fi meeting]] (Russian) [[wiki/people/val-levitan.md|Val]] took Flex Pay out of MVP 2; Pavel will retag it MVP 3 — [[wiki/decisions/2026-10-15-mvp2-is-flex-iq-wi-fi-remote-update-diagnostics-and-galaxy-reporting-and-flex-pay-moves-to-mvp3.md]] [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]] [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]. So the Sept-30 "MVP 2 is exclusively adding FlexPay" is replaced (Val's view, pending his final list with Andrei). Wi-Fi stays MVP 2. Pavel also noted that in MVP 3, with Flex Pay and Flex IQ at one location each carrying a modem and an access point, they must agree "кто главный"; Bosik: the router-or-client switch handles it [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]. The one-unit limit itself is not touched.

## Open commitments

- [ ] [[wiki/people/val-levitan.md|Val Levitan]] — pre-run the parallel wiring for the WSU protocol at locations so the second unit can be added later — due unspecified — [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

**§15.8:** clear.

## Sources
- [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Notes_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]
- [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]]
- [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
