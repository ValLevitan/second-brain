---
type: decision
title: Set up the Light & Wonder SAS test bench in the Georgia office and build a Minsk emulation of it
date: 2026-08-26
aliases: [L&W SAS test bench, Light and Wonder test station, SAS test bench Georgia, SAS emulation on VMs, self-test trust with Lonnie]
source-count: 2
status: active
open-commitments: 2
open-questions: 1
---

# Set up the Light & Wonder SAS test bench in the Georgia office and build a Minsk emulation of it

On the [[wiki/meetings/2026-08-26-alignment-planning-nova-september-releases.md|Aug 26 2026 alignment call]] [[wiki/people/irina-shishko.md|Irina Shishko]] asked how the coming South Dakota submission would be pre-tested. Her account of the last submission: the certifier **Lonnie** ran JVL through first, JVL corrected many small defects across several passes, and only then did it go to the lab — an arrangement [[wiki/people/juan-martinez.md|Juan]] had negotiated. Val's answer set the process for this round. [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]

## What was decided

- **[[wiki/people/elizabeth.md|Elizabeth]] sets up the test bench in the Georgia office**, with Val supervising on site — "Нужно, чтобы Элизабет его setup сделала бэнч… Я нахожусь здесь, поэтому я смогу проконтролировать." [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- **JVL then runs, itself, the tests Lonnie used to run** — "чтобы… Протестировал с вами… То, что раньше тестировал лони." [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- **Testing must be thorough, because the trust is the asset.** Val: if Lonnie notices JVL skimped and did not test everything properly ("Просачко вали и не все протестировали досконально"), "То он вернет нас обратно" — he sends JVL back to the old regime where he does the testing, "значительно дороже" and significantly slower. "тот знак доверия, который мы сейчас получили. Нам нужно капитализировать его?" [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- **Pavel's addition, accepted: build a full emulation of the Light & Wonder player-tracking / SAS system on virtual machines in Minsk.** Method: capture what the real system does — "какие у неё есть ручки и крючки" (what handles and hooks it has) — with Claude's help, and reproduce it on VMs so Minsk has a similar system. Val's framing of the payoff was to make it part of the automated test suite; Pavel's was field diagnosis — whenever a field problem raises "как это себя ведёт там с их сасом?" (how does it behave with their SAS?), the team can attach the emulator. Pavel qualified it: he will talk to Elizabeth, look at the tooling and see how complex the system is first. [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- **Who does the technical testing in Georgia:** Val does not want to wait — [[wiki/people/elizabeth.md|Elizabeth]] is there now, [[wiki/people/anibal.md|Anibal]] (whom Val moved from Peru) is there too, and [[wiki/people/sebastian.md|Sebastian]] arrives shortly. Irina's version of the loop: Minsk prepares a version and hands it over, and the Georgia side checks it on the bench. [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]

## Background: how the bench got to Georgia

Lonnie had required JVL to buy the **Light & Wonder test station**. JVL bought it; it sat in the South Dakota office; when that office was closed everything was shipped to Georgia, where the test kit has now arrived — "Мы его купили, он у нас находился раньше садоофисе. Мы с алтокотофис закрыли и всё отправили в джорджию. В джорджио пришёл этот тест им кит." [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]

## Open commitments

- [ ] [[wiki/people/elizabeth.md|Elizabeth]] — set up the Light & Wonder SAS test bench (SD VLT) in the Georgia office — due ASAP; Val on site to oversee — [[raw/Meeting_Notes_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — assess the Light & Wonder SAS/player-tracking system with Elizabeth and, if tractable, build a full VM emulation of it in Minsk for the automated test suite and field diagnosis — due unspecified — [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]

## Open questions

- How complex the Light & Wonder SAS system actually is, and therefore whether the Minsk emulation is feasible — Pavel: "Насколько она сложна, если она не сильно сложная, то думаю, что мы это сможем… Сделать" — [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]

## Sources
- [[raw/Meeting_Notes_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
