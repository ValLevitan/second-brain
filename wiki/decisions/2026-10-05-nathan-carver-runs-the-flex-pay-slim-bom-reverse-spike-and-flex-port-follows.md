---
type: decision
title: Nathan Carver runs the Flex Pay Slim BOM reverse spike — flatten the MSBC BOM into GitHub, rebuild it through projects, repos, data contracts and agents, push it back and compare; freehand; the Flex Port is spiked next; the work sits under DTP-1083 (or IP-965)
date: 2026-10-05
aliases: [Flex Pay Slim reverse spike, BOM reverse spike, reverse engineer the bill of material, freehand spike, compile the BOM, Nathan implements the concept, hardware sync DTP-1083, IP-964, IP-965, Flexport second spike, Flex Port second spike, pretend this was not our starting point]
source-count: 4
status: active
open-commitments: 6
open-questions: 2
---

# Nathan Carver runs the Flex Pay Slim BOM reverse spike (Oct 5 2026)

Ruled by [[wiki/people/val-levitan.md|Val Levitan]] in two steps on the afternoon of Oct 5 2026. First, at the end of the [[wiki/meetings/2026-10-05-design-to-msbc-zero-trust-repos-and-data-contracts.md|1:19 PM meeting with Genadi Peari]], Val agreed Genadi cannot build this alone and said he would hand it to [[wiki/people/nathan-carver.md|Nathan Carver]]: "Этот концерт легко подхватит. Нейтан… Я позвоню ему сейчас… и попрошу его имплементировать… flax pay slan. Чтоб он наладил всё это и показал… и тогда вы на всё это посмотрите" [[raw/Meeting_Transcript_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]]. Then, five minutes later, at the [[wiki/meetings/2026-10-05-nathan-carver-flex-pay-slim-bom-reverse-spike.md|1:58 PM call with Nathan]], Val set the spike and Nathan took it [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]. The thread is sequenced on [[wiki/decisions/2026-09-23-the-bom-source-of-truth-is-the-latest-design-in-github-and-sync-runs-one-way.md]]. The repo model the spike tests has its own page: [[wiki/decisions/2026-10-05-hardware-follows-the-developer-repo-model-one-jira-project-one-repo-zero-trust-data-contracts-no-monorepo.md]].

## What was ruled

- **The spike, in Val's words.** "Let's take flex, pay, slim, and let's reverse engineering out of that bill of material. Let's just grab this bill of material, let's flatten it… put it in GitHub, and then let's reverse out of it, going into projects. Then when we broke it down into projects, we'll create repos… We'll create data contracts in those repos… And then we'll create the logic of how these. Let's call it compiling… Let's put it. On AI." [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]
- **Start from the existing BOM, then forget it.** "We want to go into MSBC and grab that bill of material and flatten it out. And then pretend… that this was not our starting point… the moment you started with the bill of material and extracted the initial information, forget that we have that bill of material." The agents build the result; it is pushed into MSBC "in the form of a bill of material", and compared with the one they started from. "Theoretically, they should be identical, but I suspect that through the agents, you'll come up with problems, something better… the agents will find many issues that we are closing our blind eye on." [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]
- **Freehand, not bound by today's hardware repo.** Nathan asked whether the parts "all live right now. In a repo, right? In the hardware manufacturing repo." Val: "I'm not sure that we need to pay attention to what exists today… I would kind of run a just just a freehand spike… I don't want to be bound to what's created, because I'm not sure that it will give us the right picture." [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]
- **A wrong BOM means a wrong data contract.** "when we troubleshoot… We came up with the wrong bill of material… because our data contracts are flawed. Let's go back into data contract, because the source of truth now is the actual data contract." Nathan: "Correct. Okay. That makes sense to me." [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]
- **A second product after, spiked on its own.** Val first offered a smaller device if the Slim was "too big for a spike". Nathan chose to start with the Slim, then "Take a second product, spike it out maybe independently and see how they align". Val named the second one: "take a flex port… much less items, but it also has… plastics, it has sheet metal fabrication, it has screen, it has touch screen, it has hardware, it has connectors." [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]] The notes write it "Flexport" [[raw/Meeting_Notes_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]].
- **Where it lives in Jira.** Val asked Nathan to break it "into a new project… architecture of ball or alignment between GitHub and MSBC, however you want to call it… into capabilities and just start implementing it." Nathan offered his existing "hardware sync" item, "DTP 1083", under "IP 964, modernization and improvements", value stream "DevOps tools and processes". Val: "let's do it there… actually, you could also put it under Business Central application, which is IP 965… Either case is fine with me." [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]

## Why

- **Genadi cannot do it alone, and wants to see it first.** At the 1:19 PM meeting Genadi asked to break the plan into simpler steps ("На на более простые степс. Как мы тут и как мы идём туда?"). Val: "Да, с этим Я согласен, Я согласен, вы сами это не подтянете." [[raw/Meeting_Transcript_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]]
- **Genadi's time.** Val to Nathan: "I don't want Genadi to be burdened with the logic because his design time is 30% of the time. 70% of the time is building the assembly manual… bill of material, descriptions, et cetera… filing names." Naming and filing conventions should let Claude do that work. [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]
- **Nathan agreed with the idea.** "Like, I don't see why that wouldn't work. With the proper conventions in place, you should be able to do that." [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]

## Genadi's condition (1:19 PM)

Before the hand-over, Genadi asked that the earlier agreement not be lost: "Очень важно правильно сделать флат. Вот этот гитхабе… флат лист. В партс. С правильным нумеровацией, чтоб можно было намберс по нашей системе продолжить… откуда pol ревижнс? Откуда pol droings? Вот это… как кирпичики… это всё надо построить. Чтобы это все было перфект. И потом идти апп." Then it can be used "для заказов". Val: "Я я, я не вижу в этом проблем… Это это очень просто делается." [[raw/Meeting_Transcript_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]] Who builds that flat list is not named; the notes mark the owner "[Needs Val's confirmation]" [[raw/Meeting_Notes_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]].

## How this changes Oct 1

On Oct 1 Val said he would build the first GitHub structure himself with Claude Code from the Flex Pay Slim part number, then spend about two hours on it with Genadi; whether Nathan's Sept-30 experiments still stood was garbled on tape ([[wiki/decisions/2026-10-01-only-the-finished-bom-goes-into-msbc-the-configurator-is-ai-logic-outside-it-no-hybrid-and-the-pilot-is-the-flex-pay-slim.md]]). **Oct 5 answers it:** the same Flex Pay Slim pilot goes to Nathan, Genadi reviews the demo. The product and the "work backward from the BOM" method are unchanged; the doer changes. **Evolution, not contradiction.** [[raw/Meeting_Transcript_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]] [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]

## Open commitments

- [ ] [[wiki/people/nathan-carver.md|Nathan Carver]] — break the work into a project and capabilities in Jira, under DTP-1083 (IP-964) or IP-965, and start implementing — due unspecified — [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]
- [ ] Nathan Carver — run the Flex Pay Slim spike: pull the BOM from MSBC, flatten it into GitHub, break it into projects and repos with data contracts, let agents build the BOM, push it to MSBC and compare with the original — due unspecified — [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]
- [ ] Nathan Carver — then spike the Flex Port on its own and compare it with the Slim result — due after the first spike — [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]
- [ ] Nathan Carver — turn some of this over before his week off ("Just one week next week, so I'll try to turn some of this… over this week") — due the week of Oct 5 2026 — [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]
- [ ] [[wiki/people/val-levitan.md|Val Levitan]] — send Nathan the call transcript, so he has "your objectives and your undertakings from it" — due Oct 5 2026 — [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]] *(the notes say an attachment was posted in the chat at 2:43 PM; that it was the transcript is not confirmed [[raw/Meeting_Notes_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]])*
- [ ] Owner not named — build the GitHub flat list of parts first: numbering that continues JVL's system, clear rules, and set places to pull revisions and drawings from (Genadi's condition; Val: "очень просто делается") — due unspecified — [[raw/Meeting_Transcript_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]]

## History

- [x] Val Levitan — call Nathan right after the Genadi meeting, explain the concept and ask him to implement it on the Flex Pay Slim — [[raw/Meeting_Transcript_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]] — **discharged Oct 5 2026, 1:58 PM** (the Nathan call) [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]

## Open questions

- Which product categories become projects (and repos)? Val named peripheral devices, monitors, PC boards, sheet metal, plastics and harnesses, thought Genadi's part-number categories may already be the projects, and asked Nathan to "help me think it through". Not settled — [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]
- Does building the BC BOM need an agent at all? Nathan: "Once we know the structure, once we know the input. We wouldn't even need an agent, I don't think… We should be able to programmatically build it." Val's answer was that the assembly logic should come from data contracts, handled by AI. Not settled — [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]

**§15.8:** clear — no rate or hours are stated. Val stepped out twice for other calls; nothing from them is recorded. **§15 #9:** clear — DTP-1083, IP-964 and IP-965 are Jira work items, not corporate identifiers; no MSBC part number is spoken.

## Sources
- [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]
- [[raw/Meeting_Notes_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]
- [[raw/Meeting_Transcript_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]]
- [[raw/Meeting_Notes_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]]
