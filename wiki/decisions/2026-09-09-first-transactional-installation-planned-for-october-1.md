---
type: decision
title: The first transactional installation is planned for October 1 and the whole schedule is built on that assumption — FlexPay in self-service with bill acceptor, card dispenser and ticket printer
date: 2026-09-09
aliases: [first installation October 1, assume October 1, one installation on the first of October, self-service wallet case, bill acceptor card dispenser and printer, it might be September 28, the October 1 case]
source-count: 5
status: active
open-commitments: 3
open-questions: 0
---

# The first transactional installation is planned for October 1

Stated twice by [[wiki/people/val-levitan.md|Val]] on the morning of Sept 9 2026 — first to the Minsk engineers at [[wiki/meetings/2026-09-09-september-resource-plan-and-flex-port-readiness.md|7:02 AM]], then to the North-America group at [[wiki/meetings/2026-09-09-october-rollout-staging-and-unit-ramp.md|8:43 AM]]. It is a **planning anchor**, and Val said so in as many words.

- **The anchor, in the engineering call:** "давайте график [постро]им[,] условно 1 [ин]ст[ол]лейшн[,] 1 октября" — build the schedule assuming one installation on October 1 [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].
- **The anchor, in the rollout meeting, with the uncertainty stated openly:** "Let's hypothetically assume, well, with high probability, that our first installation of transactional equipment will take place October first… **I don't know if it's October first or September twenty-eighth, but let's just assume that it's October first**" [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]].

## What the October 1 installation has to do

Val walked the target case through in the engineering call and [[wiki/people/pavel.md|Pavel Frolov]] confirmed it — "этот кейс мы планируем 1 октября" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]:

- **FlexPay must be ready with three devices in it** — "должен быть в готовности, что в нем стоит билл[-]а[кце]птор[,] card dispenser[,] и принтер[,] тит[о]" — bill acceptor, card dispenser and ticket printer [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].
- **It runs in self-service.** "[Э]то работает в режиме self serv[ice]. Человек пришёл на лаке[йшн]… [з]асунул [би]л[л] в [ф]лекс[-]п[э]й или в машину… [т]огда ему выдаётся [е-волет,] он подходит к машине, начинает играть… если произошёл [пейаут,] он тогда печатается на flex[p]ay" — the player feeds a bill into the FlexPay or into the machine, gets a wallet, walks to a machine and plays, and the payout prints at the FlexPay [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].
- **The wallet can be created before or after play, and the player is mobile.** "[В]ол[е]т может генерироваться или в начале игры или после игры… [о]н может тогда ходить по машинам и дальше играть или обменять и сделать себя карточку" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]. Pavel checked the printing-without-a-wallet branch — "[е]сли он [е-волет] не предоставил, а говорит распечатать" — and it was accepted [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]. This is the zero-balance / wallet-lifetime behaviour ruled on [[wiki/decisions/2026-09-07-the-e-wallet-must-exist-with-a-zero-balance.md]].
- **An LTE modem is mandatory at the location** — "на лакейшине обязан быть [LTE] мо[дем]… и на машине и на flexpay[,] или на IQ" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]. Restated in the rollout meeting: "the machine and the pay [and] IQ needs to have the LTE modem… Gateways for sure. IQ and pay" [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]] [[raw/Meeting_Notes_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]. Consistent with [[wiki/decisions/2026-08-21-cell-modem-on-every-machine-from-september-1.md]].
- **Both FlexPay and Flex-IQ are built on the RK3568, and the modems on it work.** Pavel: "[ТЕ] мод[емы], которые мы подключали к рк 35[]68[,] они у нас заработали. Мы и флекспей и флекс IQ будем делать именно на р[]к" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]. Confirms [[wiki/decisions/2026-09-01-flex-pay-onto-rk3568.md]].

## The office rehearsal comes first

Val required the whole thing running in the office — however roughly — at least two weeks ahead: "для Того, чтобы на лаке[йшн] 1 октября поставить вот эту вот всю вещь[,] в принципе[,] она должна в офисе начинать работать… каким[-]то корявым образом… [н]у как минимум за 2 недели раньше." Pavel offered "[н]а следующей неделе?" and Val answered "2" [weeks]. Then: "и Андрей начинает [от]тестировать" — with Pavel and Irina confirming on the call that this Andrei is **[[wiki/people/andrei-klimovich.md|Klimovich]]** ("про этот[,] Климович") [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].

## The customer side of the same date, set ninety minutes later

The 7:02 AM and 8:43 AM statements above are internal planning. At **10:04 AM** the same morning Val put the same date to the counterparty who would actually host it — [[wiki/people/narasimha-rao-namburi.md|Rao]], at the [[wiki/meetings/2026-09-09-rao-machine-performance-and-exclusivity-offer.md|Rao meeting]] [[raw/Meeting_Transcript_Rao_Machine_Performance_and_Exclusivity_Offer-September-9-2026.md]]:

- **"My start date is the first of October."**
- **Five locations, not one:** "Let's plan **five locations for October. Only five locations**" — and then, separately, "Let's aim it for **installation in the first week of October**." So the internal "one installation on October 1" and the customer-facing "five locations for October, first install in the first week" are **compatible but not identical**, and neither source states the relationship.
- **The precondition is the same one the engineers set.** A JVL colleague in the room: "we will do some **in-house testing next week**"; "The roadmap is that we need to do internal testing… **We make it polished. Only after that are we ready to install.**" That is the customer-facing form of the office-rehearsal requirement above.
- **And JVL undertook to carry the first ones itself:** "we will be **ready to support those five locations in October**… We will support your team with all the learning curve of installing them. **Me personally, I'll be at the first couple of locations.**"
- **One test condition was added:** a colleague asked that the October test location be one where **all machines are dual source**; Rao said they already are. See [[wiki/decisions/2026-09-09-jvl-supports-both-dual-sas-and-single-sas-and-not-mudagoose.md]].

**Rao's own caveat, given in the same conversation:** he cannot force the incumbent system out — "**It will happen organically**" — which Val accepted. So the October window has a named host and a named count, and no guarantee the locations will be clear of a competing system by then [[raw/Meeting_Transcript_Rao_Machine_Performance_and_Exclusivity_Offer-September-9-2026.md]].

## What this collides with

The readiness estimate given in the same call — best case **September 25** for the Flex-Port MVP — leaves almost no margin before October 1. Both stand as stated; see [[wiki/decisions/2026-09-09-flex-port-readiness-slips-to-september-25-and-stays-the-bottleneck.md]]. The one-unit-per-location limit that shapes what can actually be installed is on [[wiki/decisions/2026-09-09-one-transactional-unit-per-location-until-the-wi-fi-iteration.md]].

## Open commitments

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — build the work schedule on the assumption of one installation on October 1 and have it ready by Friday; Val set the Friday meeting specifically ("Я особенно назначил [ап]poi[n]tment") — due Sept 11 2026 — [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]] [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [ ] [[wiki/people/val-levitan.md|Val Levitan]] and [[wiki/people/pavel.md|Pavel Frolov]] — meet Friday to work the schedule through — due Sept 11 2026 — [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [ ] [[wiki/people/narasimha-rao-namburi.md|Rao]] — select the five October locations so the first-week-of-October installation has a host — due week of Sept 14 2026 — [[raw/Meeting_Transcript_Rao_Machine_Performance_and_Exclusivity_Offer-September-9-2026.md]]

**§15.8:** clear.

## Sources
- [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Notes_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]
- [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]
- [[raw/Meeting_Transcript_Rao_Machine_Performance_and_Exclusivity_Offer-September-9-2026.md]]
