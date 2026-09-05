# Meeting Summary — Check framework + Kaliocha prose — Sasha (back from vacation) (Nova Prose QA Automation Strategy)
**Date:** September 1, 2026, 8:35 AM – 8:54 AM Eastern
**Duration:** ~19 minutes
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko, Alexander Biratko

**Raw transcript:** [[Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026]]

## Summary

A short check-back call with Alexander (Sasha) Biratko on his first days back from vacation. Pavel Frolov opened by explaining Sasha's new assignment: move Flex-Pay onto the RK3568 platform, targeting the 15th. The reason for moving it is that JVL already has a full build system for RK3568, service registration, working payment-hub integration, and the software-update mechanism is being finished for it — so keeping Flex-Pay on the same footing as Flex-IQ is the sensible choice.

Most of the call was about prose and how it connects to testing. Val's position: JVL has code for the Nova platform but no prose, and he does not want prose written only for the game — he wants it for the platform itself. (He noted the team deliberately avoids calling Nova a "framework"; he calls it a platform because he was told it is more than a framework.) Sasha pointed out that the game repository and the shared platform repository hold different code, and that the two bodies of prose can be split accordingly — describe the common part first, and describe the game either later or when the next new game is written. Val agreed with that split and restated why prose matters at all: from the prose you build the overall architecture, from the architecture you get capabilities, and from capabilities you get requirements with acceptance criteria that let Claude generate and run end-to-end tests automatically.

Val was explicit that the normal order was inverted. Properly, you write capabilities, then architecture, then code; JVL as usual wrote the code first. So September is the reverse-engineering month: write the prose, work back to the architecture, and produce the capabilities. He restated the schedule the team has agreed — during September the capabilities for the new platform get written, and from October 1 active development on Nova begins.

He also summarised the state of the experiments for the record: converting a horizontal ("dual-screen") game from Rage to Nova, and moving a vertical game into Nova, have both gone well and were straightforward with AI assistance, and Igor Metelski appears comfortable working that way. Val's stated worry is unchanged — the bottleneck will be QA. If everything cannot be checked automatically, QA stays a manual button-pushing job and, in his words, all the automation upstream is worth nothing.

Pavel reported that Vladimir Samusenko had shown him work from the previous day: beyond writing prose, Vladimir had built three Claude skills — one that indexes a codebase with no prose (analyses the code, creates a module/component index and writes per-module documentation), and one that, where prose already exists, inspects the diff at pull-request time, decides whether the change fits existing modules, and either amends the prose or works out which new module to add. Vladimir had run it on his own project; he and Pavel agreed he would try the same skills on a second repository, and if that also works the skills could be reused across other repositories.

Pavel raised the honest caveat that in the first phase there will be gaps — written capabilities and requirements with acceptance criteria will not cover everything QA currently holds in their heads or in their existing test cases. Val said that does not worry him. Pavel described the working approach: run the automated tests, notice what is not covered, and ask the AI to write tests for the gap and create the matching requirements at the same time; likewise when a bug arrives from the field that no test covered, go back and create the requirement, acceptance criteria and test for it so future runs cover it.

That led to the sharpest exchange of the call, about the existing hand-written test cases. Irina Shishko and Sasha argued some of them are worth keeping — bug-specific tests, location-specific checks, rare settings cases — and Sasha proposed a one-time analysis comparing old tests against newly generated ones to find the overlap and decide what is genuinely missing. Val disagreed with reaching backwards: he does not think today's manually written tests will be very applicable, expects them to "die", and recommended freezing them in their current warehouse untouched while new Claude-generated tests, built from requirements and acceptance criteria, go into a new warehouse. He would then watch how often anyone actually needs the old ones — his instinct being, very soon, never. If he finds coverage missing he would rather ask the AI to write more tests than return to the old set, because he sees no linkage between the old tests and what is starting now. He closed the topic by saying the discussion was becoming hypothetical and that practice would settle it.

Val ended by noting Igor Metelski is running the QA-automation experiment and that the check-in with him is this Friday; he said he would add Sasha Biratko to that meeting.

## Decisions Made

- **Flex-Pay moves to the RK3568 platform, targeting the 15th.** Chosen because RK3568 already has a complete build system, service registration, payment-hub integration and a nearly finished software-update path, keeping Flex-Pay aligned with Flex-IQ. (Pavel Frolov, endorsed by Val)
- **Prose is written for the Nova platform itself, not only for the trial game.** The common platform part is described first; the game's own prose can wait or be written when the next game is built. (Val, with Sasha Biratko's split)
- **Existing hand-written test cases are frozen in their current warehouse, not migrated.** New AI-generated tests, derived from requirements and acceptance criteria, go into a new warehouse; the team then observes how often the old ones are actually consulted. (Val's recommendation — Sasha's overlap-analysis alternative was heard and not adopted)
- **Schedule reaffirmed:** September is for writing prose and capabilities for Nova (reverse-engineered from existing code); active Nova development starts October 1. (Val, standing plan)
- **Sasha Biratko is added to Friday's QA-automation check-in with Igor Metelski.** (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexander Biratko | Move Flex-Pay onto the RK3568 platform | Target the 15th | High | Aligns Flex-Pay with Flex-IQ on a platform that already has build, registration, payment-hub and update support |
| 2 | Alexander Biratko | Write prose for the Nova platform's common/shared part (game prose deferred) | September | High | Val: September is the reverse-engineering month — prose → architecture → capabilities |
| 3 | Vladimir Samusenko | Try the three prose skills on a second repository and report whether the result is positive | Not fixed | Normal | If it works the skills get reused across other repositories |
| 4 | Val Levitan | Add Sasha Biratko to Friday's meeting with Igor Metelski | Before Friday | Normal | Val: "I'll invite Sasha Biratko here too" |

## Open Questions

- How much of QA's existing knowledge (in their heads and in current test cases) will be lost in the first phase, given capabilities and acceptance criteria will not cover everything — Pavel flagged the gap; Val accepted it.
- Whether the old hand-written tests should be compared against the newly generated set at least once to catch important edge cases — Sasha argued yes, Val argued against reaching backwards; left to practice rather than settled.
- Which specific Flex-Pay Val was referring to was not resolved on the call; he set it aside and moved on.

---
*Processed from Teams transcript on September 4, 2026 (scheduled watcher, catch-up capture after a multi-day scheduler outage)*
*Source meeting: Check framework + Kaliocha prose — Sasha (back from vacation) — September 1, 2026*
