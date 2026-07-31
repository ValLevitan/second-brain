# Meeting Summary — Testing with AI
**Date:** May 29, 2026, 10:03 AM (per transcript)
**Duration:** ~1h 0m
**Attendees:** Val Levitan, Andrei Bosik, Pavel Frolov, Irina Shishko, Evgeny Kharetski
**Mentioned (not present):** Dzmitry Chudzinau (Dzima), Sergey Simonov, Alexander Biratko (Sasha), Anton Liashkevich, Aaron Bockelie

## Summary

This was a working session on how to test products, and how products get built. The team had agreed Wednesday to pause forward work until they settle the direction, so this was a smaller "think it through" meeting.

**Direction on testing.** Val said the old vision from ~6 months ago — building a deterministic framework for automated tests — is the wrong direction. The team agreed. With constant integration testing, the need for big end-to-end runs goes down. End-to-end no longer has to mean "boot the whole machine, every light on, full path from one end to the other." It can be smaller, change shape, or run less often.

**AI in testing.** Pavel noted QA engineers don't run every recorded test for a release — they pick the relevant ones, and AI should work the same way. The team warned that AI with no boundaries will find a million useless ways to break things (DDoS their own web resource, port scanning, overheating hardware by re-running stress tools). AI needs to stay inside the real environment, with a person acting as operator. After some push from Val to stop shooting down ideas, the group landed on an approach: let AI propose negative scenarios, then the team reviews the list and keeps only the ones worth testing.

**How products get built (the main open problem).** Val pushed to understand who decides, once, how a product is assembled — since after the GitHub Actions are written it builds the same way every time. Answer: the developer/architect who owns that project. But no one owns architecture globally. For transactional services, Sergey Simonov wrote most of the build actions, based on decisions made with Andrei, Dzmitry Chudzinau and Pavel; Andrei treats Dzmitry as the source of truth there (Val does not). For gaming, work is split across repos: LGS by Evgeny Kharetski and Sasha Biratko, OS and final ISO image by Pavel, game packaging by Sasha Biratko. Local artifacts get consolidated into an "installer" — a separate project with its own CI/CD that produces the image written to the SD card.

**The gap.** Today, artifacts go into the installer independently and self-deploy. Whether the blocks actually work together is NOT checked at installer build time. Val said it should be. Pavel agreed — now that data contracts exist, it should be — but the installer was built long before data contracts. Andrei proposed: every repo with an API generates a data contract as a build-step output, which then enables automated tests between two or more dependent artifacts, catching problems earlier instead of at QA on the machine.

**Manifest approach.** Evgeny described (and prefers) a documented approach: a manifest in an integration repo holds the tested versions of every component a product is made of. When a component merges to main, an action opens a PR in the integration repo, spins up a runner, and tests the new component against the fixed versions of the others. If all pass, the manifest version updates — so anything in main is a known-good, contract-satisfied combination. He said Pavel's proposal from last meeting is the same idea but written only at the surface; his own document is more detailed.

**Forward-only versioning.** Pavel raised the multi-market problem: a certified version for one market (e.g., Georgia, LGS v50) may need a re-release while reference versions have moved on (LGS 55, progressive controller 33). Evgeny: we shouldn't go backward; versions only move up. Val agreed to make this a discipline — never roll back. Andrei noted this is the "forward" strategy. This mainly affects the gaming product; other products (LeeX, IQ) move forward fine. The old product on SVN is excluded. They agreed to call LGS, progressive controller, etc. "artifacts," not "components."

**Test taxonomy.** A long discussion tried to align on unit / component / integration / end-to-end. Not fully resolved. Andrei found a Habr article on the testing pyramid that he thinks matches their case (a hybrid Agile/DevOps pyramid) and answers most of their questions; he'll share it.

## Decisions Made

- **Drop deterministic frameworks for automated testing** — judged the wrong direction. (Val, endorsed by team)
- **End-to-end tests don't require booting the whole machine** — they can be smaller and run less often as integration testing grows. (Val, team)
- **AI testing must be bounded and operator-controlled** — approach: AI proposes negative scenarios, team curates which to keep. (Val, Pavel, Andrei)
- **Adopt forward-only versioning as discipline** — never roll back to old artifact versions; applies mainly to gaming; old SVN product excluded. (Val, Evgeny, Andrei)
- **Rename "components" to "artifacts"** (LGS, progressive controller, etc.) for clarity. (Pavel, agreed)
- **v5.1 repository standard accepted as working** (~80%, remaining 20% to be solved). (Andrei, Val)
- **Monday working session** to drive the build + test architecture to a written standard. Val deliberately set his slot early to force weekend prep. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel, Andrei, Evgeny | Drill the CI/CD build + test architecture further (how a product is reliably assembled from the start, including adding new modules), ideally on a whiteboard / block diagrams, and drive toward a written standard | Mon Jun 1, 2026 | High | Core unresolved problem; Val warned the thinking will dissipate if not pinned down now |
| 2 | Pavel | Once the Monday session recording ends, drop the transcript here in .docx format | Mon Jun 1, 2026 | Normal | Val asked explicitly so the next session can be processed |
| 3 | Evgeny Kharetski | Share his detailed manifest/testing document with the team (Anton, Irina, Andrei all asked) | Today (right after meeting) | Normal | More detailed version of Pavel's earlier proposal |
| 4 | Andrei Bosik | Share the Habr testing-pyramid article in the chat for everyone to read before Monday | Before Mon Jun 1 | Normal | He thinks it matches their hybrid-pyramid case and answers most open questions |

## Open Questions

- Exact definitions of unit / component / integration / end-to-end tests — debated, not settled. The Habr article is meant to help align.
- How to handle a re-release for one market on an older certified artifact version (Pavel's Georgia / GLI example) under a strict forward-only rule — Evgeny says "don't do it," but the multi-market edge case wasn't fully closed.
- Whether to formalize the integration-repo + manifest approach into the standard.

---
*Processed from Teams transcript on May 29, 2026*
*Source meeting: Testing with AI (20260529)*
