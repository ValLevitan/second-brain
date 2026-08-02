# Meeting Summary — CI/CD for Flex IQ
**Date:** 7 July 2026, 3:20 PM Eastern
**Duration:** ~41 minutes
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko

## Summary

**Current build state.** Pavel laid out what exists today for Flex IQ: three GitHub actions. One builds the binary artifact for the device. One makes the installer — it takes the binary plus a prebuilt OS and packages an image for SD-card install (used at the factory for first install, when the case is open). One builds an encrypted binary for USB-stick software updates in the field (no case opening). The USB update works like this: the machine finds the file on the stick, pulls it in, and on the next power cycle it decrypts, checks the version is newer, installs, and tries to boot the new software. If the boot and database init succeed, it commits the new version; if not, it rolls back to the old one.

**Over-the-air updates.** Val wants to move past USB sticks to remote ("download") updates. Pavel said the infrastructure is basically built and the code probably already exists (Sasha wrote it), but nobody has tested it. With proper planning and bug-fixing it's doable in a short, reasonable time — but not for the August exhibition. Target is September/October.

**How to deliver builds.** Pavel objected to any action that pushes straight to all live devices. He wants a separate management step. The CI/CD result should be a release procedure that fixes the version and binaries in GitHub (stored in the artifact repo). The open question is what tool then delivers a specific build to a specific Flex IQ. Val does not want to build their own service — he wants a ready-made third-party "deployment management" tool (his analogy: airport flight management), with an approval gate so updates aren't fired off casually, especially by internal developers. Pavel added that no update should ever go to all machines at once — start with a trial batch of ~3 machines that are physically reachable by car, in case a device needs swapping.

**Approval layer.** Val wants product managers Filippo and Irina (plus Pavel/Juan) in the approval loop — a deployment shouldn't go out until the group agrees.

**Prose / documentation.** Val pushed to adopt "prose" (living documentation) and keep it updated as code changes. His concern: prose he wrote once took ~14 hours and goes stale the moment code changes, so it's only useful if it lives and updates continuously. Pavel saw no real objection — it helps AI retrieve information fast, and can be ignored for specific tasks if the repo grows large. Nobody rejected it, so Val considers it agreed.

**Reverse-engineering requirements from code.** Val described his method for generating requirements from existing code: don't jump straight from prose to capabilities. Instead, extract "architectural clusters" (viewable as visual/Mermaid diagrams, fast to approve), then derive machine-level requirements with acceptance criteria (this produces a huge "binary" set — for RIS it was 222 requirements and ~1,600 acceptance criteria). Then translate those into human-written requirements, which reduces roughly 5:1 down to an estimated 50–70. From there, use cases and diffs ("I had this, now I want this") drive new requirements → capability → features → feature branches → code → tests. He runs this largely automated with multi-agent tooling and has had Juan review the human-level output with few corrections.

**Skepticism.** Irina doubts the 5:1 reduction will hold for RIS given how many distinct items there are — she expects the result to be fairly general, and noted the Kislovodsk games set is its own product with its own requirements. Val will finish the RIS pass within two days and show them the output to judge.

**Vacation note.** Irina reminded that Andrei goes on vacation starting tomorrow for two weeks — don't expect anything from him in the coming days.

## Decisions Made

- **Adopt "prose" (living documentation) and keep it updated as code changes.** Reason: stale one-off docs are useless; only continuously-updated docs help. Nobody objected. (Decided by Val, no objection from Pavel/Irina)
- **Remote/over-the-air update deferred to September/October, not August.** Reason: not ready for the August exhibition and no push to rush it. (Val, agreed by Pavel)
- **Use a ready-made third-party deployment-management tool, not a home-built service.** Reason: avoid building infrastructure that already exists off the shelf. (Val)
- **No update pushed to all machines at once; deployment goes through an approval layer and a small trial batch first.** Reason: bad updates happen; need ~3 reachable machines to test and recover. (Pavel, endorsed by Val)
- **Reverse-engineer existing code into requirements via architectural clusters → machine requirements → human requirements → use cases.** Reason: fully manual is too slow and tiring; this is largely automatable with good quality. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Bosik | Research a third-party deployment/fleet-update management tool (OTA, with version control, scheduling, and an approval gate) for pushing builds to specific Flex IQ devices | After vacation (~July 28) | Normal | Val called this out on-transcript to pass to Andrei; needed for Sept/Oct remote-update goal. Andrei is on vacation for 2 weeks from July 8 |
| 2 | Val Levitan | Finish the RIS code-to-requirements reverse pass and show Pavel/Irina the result (~50–70 human requirements) | ~July 9 (within 2 days) | High | Basis for validating the reverse-engineering approach and the 5:1 reduction claim |
| 3 | Pavel Frolov, Irina Shishko | Review Val's RIS requirements output once ready and give their read | After #2 | Normal | Irina is skeptical the reduction holds; needs their judgment |

## Open Questions

- Build own AWS deployment service vs. use a third-party tool — leaning third-party, pending Andrei's research.
- Will the ~5:1 requirement reduction hold (222 req / 1,600 AC → 50–70)? Irina doubts it; to be judged after Val shows the RIS output.
- Whether to pilot the reverse-requirements approach on Flex Recycler first (it already has some capabilities written) — Pavel raised it, not decided.

---
*Processed from Teams transcript on 7 July 2026*
*Source meeting: CI_CD_Flex-IQ-July-7-2026*
