---
type: decision
title: Three more features go onto Flex-Port capability 165 — an optional PIN code, reading SAS flags from the machine, and remote log retrieval — and the wallet transfer becomes a capability of its own
date: 2026-09-09
aliases: [capability 165, FlexPort e-wallet and SAS support, optional PIN code, SAS flags door open machine blocked, remote logging over WSU, logs only to a USB stick, wallet transfer is its own capability, F PORT project, feature F Port 1]
source-count: 2
status: active
open-commitments: 2
open-questions: 0
---

# Three features added to capability 165, and the wallet transfer split out

Worked out live in Jira by [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/irina-shishko.md|Irina Shishko]] with [[wiki/people/val-levitan.md|Val]] watching, at the [[wiki/meetings/2026-09-09-september-resource-plan-and-flex-port-readiness.md|Sept 9 2026 7:02 AM call]]. Val had asked what other features belong under the capability — "так[,] как это [фича] может называться?" — and Pavel named them one at a time [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].

## The container

- **Capability 165 is the Flex-Port e-wallet and SAS-support capability.** Val, reading it back: "[ф]лек[с]порт и [е-]волет [плюс] сас суппорт" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]. The derived notes put it as "[t]he FlexPort e-wallet and SAS support work sits under capability 165" [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].
- **Flex-Port now has its own Jira project matching its repository.** Val asked what "Ф порт" is — "это название проекта или что это?" — and Pavel: "[д]а, это название проекта в [Jira], и она однозначно соответствует репозиторию. Это то, что мы говорили[ —] именование проекта… должны соответствовать." Before this, Flex-Port lived inside the **FP** project: "[д]о этого у нас флекспорт жил в проекте [ФП]. А сейчас у нас произошло разделение[ —] ну[,] Дима Ковальчук вот эти все… сделал, поэтому мы сейчас переходим на новое [нумерование]" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]. Credit for the split goes to [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]]. The one-repository-one-project convention is the one on [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]].
- **The feature number is arbitrary.** Val asked what "[Ф] порт 1" means; Pavel: "[о]дин — это номер"; Val: "это просто он арбитр[арно] дал такой номер, да?" — "Да." Irina: "это в этом репозитории 1 фича" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].

## The three features

1. **An optional PIN code.** "[Ч]то можно придумать? Это то, что нам надо **опционально сделать пин[-]код**… это то, что сейчас очевидно известно" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]. Already ruled configurable per location on [[wiki/decisions/2026-09-07-pin-and-wallet-load-configurable-per-location.md]] — this is that ruling becoming a Jira feature.
2. **Read the machine's flags over SAS and react to them.** "[н]ам надо по сассу получать какие[-]то **флаги от машины**… и учитывать в работе флекс[-]порта… там **дверь открыта**[,] на это надо как[-]то отреагировать, чтобы флег[с]порт не был доступен… там **заблокирована машина**[ —] по 1 [SAS-порту] мы это тоже должны анализировать" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]. Door-open is also the first negative case to be tested — see [[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]].
3. **Remote log retrieval.** "необходимо будет по WS[U] сделать всё[-]таки какое[-]то **логирование**[,] то есть у нас сейчас для флекспорта есть только логирование, снятие логов на **[ю]сб[-]стик**… и это удалённо невозможно получать логи" — today Flex-Port logs can only be pulled onto a USB stick, never remotely [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]. This is the work Pavel wants handed to [[wiki/people/evgeniy-alekseev.md|Alekseev]] — see [[wiki/decisions/2026-09-09-flex-port-readiness-slips-to-september-25-and-stays-the-bottleneck.md]].

Pavel said he could create the placeholders on the spot: "это я могу прямо сейчас создать заготовку" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].

## The wallet transfer is its own capability

"[В]от этот вот [wallet] трансфер[ —] это должен быть **свой [капабилити]**… и он будет касаться и серверной стороны. Ну то есть флекс[-]пей" — because it reaches the server side as well as FlexPay [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].

## One capability reworded, not created

A capability Pavel first attributed to Alekseev turned out to be **[[wiki/people/andrei-klimovich.md|Andrei Klimovich]]**'s, created the previous evening after a meeting — Val: "Алексеев не создавал[,] это создавал, скорее всего… Андрей [Б]осик"; Pavel then: "а нет, это вообще Андрей [К]лимович"; Irina: "это он вчера создавал, видимо, после митинга." Pavel proposed rewording it around the zero-value wallet — "[з]иро[-]в[э]лью и [в]олет[,] тогда это становится логично" — explaining the underlying case: "если у игрока нет его [е-волета,] то чтобы он имел возможность выбрать опцию на флекс[-]порте и он напечатается." Irina flagged that it carries no requirements at all yet: "здесь совсем нет требований никаких" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]. The zero-balance wallet itself is [[wiki/decisions/2026-09-07-the-e-wallet-must-exist-with-a-zero-balance.md]].

## Open commitments

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — create the three placeholder features under capability 165: optional PIN code, reading SAS flags from the machine (door open, machine blocked), and remote log retrieval over WSU/SAS — due unspecified; he said he could do it immediately — [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]] [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — create a separate capability for the wallet-transfer work, which touches the server side as well as FlexPay — due unspecified — [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

**§15.8:** clear.

## Sources
- [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
