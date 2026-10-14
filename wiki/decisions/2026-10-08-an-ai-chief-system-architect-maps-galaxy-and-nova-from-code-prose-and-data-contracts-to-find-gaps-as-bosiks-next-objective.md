---
type: decision
title: An "AI Chief System Architect" builds the whole Galaxy and Nova architecture from code, prose and data contracts only, to find gaps between intent and code; output is HTML block diagrams with the harness links and the prose behind each block; it is Andrey Bosik's next objective, in parallel with the AI PM
date: 2026-10-08
aliases: [AI Chief System Architect, AI-Chief System Architect, AI chief architect persona, gap-finding architecture, architecture from code prose and data contracts, prose and contracts quality check, Bosik next objective]
source-count: 2
status: active
open-commitments: 2
open-questions: 2
---

# An AI Chief System Architect maps Galaxy and Nova to find the gaps

Set on the [[wiki/meetings/2026-10-08-ai-chief-system-architect-gap-finding-task.md|Oct 8 2026 "AI-Chief System Architect" call]] (Russian) between [[wiki/people/val-levitan.md|Val Levitan]] and [[wiki/people/pavel.md|Pavel Frolov]] [[raw/Meeting_Transcript_AI_Chief_System_Architect_Gap_Finding_Task-October-8-2026.md]].

## What was decided

- **The idea (Val).** A next stage, in parallel with the [[wiki/projects/ai-project-manager-and-company-second-brain.md|AI PM]] work: a persona that looks only at the code, the prose and the data contracts, and from them builds the architecture of the whole system — both Galaxy and Nova. Val expects gaps and mismatches and wants to find them. Asked by Pavel "несоответствие чему", Val: a mismatch between what the team had in mind and what the code actually shows [[raw/Meeting_Transcript_AI_Chief_System_Architect_Gap_Finding_Task-October-8-2026.md]].
- **If inputs are missing, it should not build.** Val: if not all the prose and data contracts exist, the system "построится не должна". Pavel: then it is really a quality check of the prose and contracts across all dependent repositories, which different developers maintain; integration tests should be analysed too, because they link the repositories [[raw/Meeting_Transcript_AI_Chief_System_Architect_Gap_Finding_Task-October-8-2026.md]].
- **The output (Val).** The architecture in some format, for example HTML block diagrams; how the harness connects the blocks; and which prose text sits behind each block [[raw/Meeting_Transcript_AI_Chief_System_Architect_Gap_Finding_Task-October-8-2026.md]].
- **Owner.** Val: "это следующее задание, которое Андрею нужно дать… я тогда это вношу как… следующие объекты для Андрея босика" — [[wiki/people/andrey-bosik.md|Andrey Bosik]], who was not present. Pavel: "Давайте попробуем" [[raw/Meeting_Transcript_AI_Chief_System_Architect_Gap_Finding_Task-October-8-2026.md]].

## Pavel's view

- Claude can build the architecture from these inputs; if the prose is detailed, the result will reflect how the products are really made. The hard part is judging whether it is right and where the gaps are [[raw/Meeting_Transcript_AI_Chief_System_Architect_Gap_Finding_Task-October-8-2026.md]].
- Start from the main positive use cases. His example: Transactional — FlexPort, Flex IQ and the server, with FlexPort connected to the machine, one closed system. See how Claude pictures it from what is in GitHub, then extend to failure cases [[raw/Meeting_Transcript_AI_Chief_System_Architect_Gap_Finding_Task-October-8-2026.md]].
- He expects a near 100% match, because autotests already catch mismatches with requirements and contracts and these are fixed on the fly, with the prose updated. But he is not sure the prose is kept up to date in every repository; he has seen it in two [[raw/Meeting_Transcript_AI_Chief_System_Architect_Gap_Finding_Task-October-8-2026.md]].
- This task is better defined than the AI PM: clear limits and a more deterministic output (Val: more product-focused) [[raw/Meeting_Transcript_AI_Chief_System_Architect_Gap_Finding_Task-October-8-2026.md]].

## Open commitments

- [ ] [[wiki/people/val-levitan.md|Val Levitan]] — enter the AI Chief System Architect task as Andrey Bosik's next objectives — due unspecified — [[raw/Meeting_Transcript_AI_Chief_System_Architect_Gap_Finding_Task-October-8-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — build the Galaxy and Nova architecture from code, prose and data contracts as HTML block diagrams, with the harness links and the prose behind each block (to be assigned by Val) — due unspecified — [[raw/Meeting_Transcript_AI_Chief_System_Architect_Gap_Finding_Task-October-8-2026.md]] [[raw/Meeting_Notes_AI_Chief_System_Architect_Gap_Finding_Task-October-8-2026.md]]

## Open questions

- In what format must the architecture be shown so the team can judge whether it matches what they intended? (Val: "я не знаю, в каком виде она должна быть преподнесена вам") — [[raw/Meeting_Transcript_AI_Chief_System_Architect_Gap_Finding_Task-October-8-2026.md]]
- Is the prose updated in all repositories, or only in the two Pavel has seen? — [[raw/Meeting_Transcript_AI_Chief_System_Architect_Gap_Finding_Task-October-8-2026.md]]

## Related

- [[wiki/topics/nova-platform-architecture.md]] — the NOVA platform, its prose standard and data contracts; the human Chief Architect appointment of May 12 2026 is a different role.

**§15.8:** clear. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_AI_Chief_System_Architect_Gap_Finding_Task-October-8-2026.md]]
- [[raw/Meeting_Notes_AI_Chief_System_Architect_Gap_Finding_Task-October-8-2026.md]]
