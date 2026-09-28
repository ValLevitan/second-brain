# Meeting Summary — Hardware GitHub standard + Business Central sync design (Val & Genadi Peari)

**Date:** August 12, 2026, 3:00 PM Eastern (mixed Russian/English)
**Duration:** approximately 174 minutes (long working session)
**Attendees:** Val Levitan, Genadi Peari (hardware/electronics lead). Nathan Carver brought in near the end. Referenced: Andrei (repo organisation), Misha (purchasing/PO approvals), Alexey (electronics engineer who commits to GitHub), Pavel Frolov (recommended an earlier structure), Ignatiy. ("Abiguele" in the raw diarization is an artifact, not a person.)
**Raw transcript:** [[Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026]]
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Calendar pairing:** Outlook event "General_alignment-August-12-2026", 3:00 PM ET, organiser Val, attendee Genadi Peari. Confirmed.
**Context:** Deep-dive follow-on to [[Meeting_Notes_AI_Engineering_Workflow_and_Hardware_CxO-August-6-2026]]. This is the working session that designs the GitHub↔Business Central sync for hardware, under the [[Hardware Repositories]] standard adopted August 12. Feeds the AI-executive / agent operating model and Nathan's BC-API work.

## Summary

Two intertwined threads ran for ~3 hours: **(A) component sourcing** and **(B) how JVL stores hardware information in GitHub and keeps Business Central in sync** — the latter is the substance.

**A. Recycler and component sourcing.**
- **JCM recycler (four real drums, 30 notes each)** — Val wants it as a second source alongside MEI/Mars. JCM finally opened up (full SDK, docs, engineering/sustaining contact "Cliff") after earlier friction over a sample and a document JVL refused to sign. Unit ~**$1,850**; JCM has stock in the US (can ship quickly) but a sample to Minsk takes ~a month. Decision leaning: **buy one unit** (ship to Minsk via CMA), keep JCM as a supplier. The four-drum design beats MEI's (MEI must keep a half-empty drum to shuffle denominations). Complaint: JCM shipped the unit **without a bezel** and the narrow bezel is unavailable ahead of a show.
- **Rockchip board:** a 3576 with **8 GB** sample (~$150, cheaper in production) is "more than enough" for a street machine; the 16 GB (~$250–290) judged not worth it.

**B. Hardware GitHub standard + BC sync (the main decision).** Val walked Genadi through a structure worked out live with his "second brain" agent:

- **GitHub is the source of design truth; Business Central follows it. Nobody types design data into BC by hand.** SharePoint is explicitly rejected as a source of truth (no versioning, weak controls, agents work poorly with it).
- **Two repositories matter:**
  1. **`hardware-components`** — every **purchased** part (monitors, power supplies, printers, bill acceptors) gets a folder with datasheets/drawings/manuals and a machine-readable `item.yaml`. Organised **category first, manufacturer second** (an engineer searches by what the part does, e.g. Component → Monitor → Cortek; Power Supply → MeanWell; Bill Acceptor → JCM MyVision). When a manufacturer folder grows crowded, add a **model** subfolder. Each folder's README carries the **MSBC item number**, which is the bridge between the two systems.
  2. **`hardware-manufacturing`** — parts JVL **manufactures itself** (e.g. Flexport). Val initially split PCBA / mechanical / manufacturing into three repos, then **merged hardware-mechanical into hardware-manufacturing** — only final/production releases live in GitHub (not daily CAD working files; SolidWorks/Altium builders cannot run against GitHub). Each release revision holds both the native CAD source and the factory package (Gerbers, pick-and-place, BOM CSV, schematic PDF).
- **Why hardware differs from the software repo standard:** binary files can't be merged by Git and CI can't build/test them, so hardware uses **few larger repos with Git LFS**, not many small buildable ones.
- **Feature-branch / pull-request discipline applies to hardware too:** an engineer (e.g. Alexey) works on a branch, copies the old revision folder to a new one (Git LFS stores unchanged files once), replaces only what changed, commits and opens a **pull request**; a **separate approver** (Genadi/Eugene) reviews and **merges** — the merge is the company's approval gate (same person may not author and merge). The approver then applies a **tag** (e.g. "Flexport revision C"). This is JVL's equivalent of an ECO/engineering-change-order.
- **The sync robot (Nathan's to build).** On a new tag, a **GitHub Action / small routine reads the BOM CSV from the tagged version, validates each line, and rewrites the item's assembly BOM in Business Central in place** (delete old lines, write new), and **stamps the tag name on the BC item card** so anyone in BC can see which frozen GitHub version the current BOM came from. New parts carry item number `new` in YAML; **BC assigns the numbers, GitHub assigns the meaning**.
- **BOM history — the key BC finding.** Val checked the live BC: JVL uses **assembly BOMs**, which have **no version history** (one current list; the only trace of past builds is posted assembly orders — "archaeology"). Rather than switch to production BOMs (heavier for the shop floor, needs routing/production orders and staff JVL doesn't have), the decision: **let GitHub tags be the BOM history; BC holds only the current mirror of the latest tag.** "What was the BOM in March?" → GitHub tag (revision B). "What went into a specific unit?" → posted assembly order in BC. Each system answers the question it is built for. Genadi will write this up as the **BOM-synchronization** section of the draft standard.

**Close.** Genadi will read/approve the draft standard (invite to the knowledge repo, accept, review, approve the pull request). Val is asking **Nathan** to define and start building the **sync-service capability** on the BC API, and asked Genadi to write a scope/task so Nathan can get into the flow.

## Decisions Made
- **GitHub = source of design truth; Business Central follows. SharePoint rejected as source of truth.** (Val)
- **Two repos:** `hardware-components` (purchased parts, category→manufacturer→model, README carries MSBC item number) and `hardware-manufacturing` (JVL-made parts, final releases only, CAD source + factory package per revision). (Val)
- **Merge hardware-mechanical into hardware-manufacturing** — only production/final versions in GitHub, not daily CAD builds. (Val, revised live)
- **Feature-branch + pull-request + separate-approver merge + release tag** is the hardware change process (JVL's ECO). (Val)
- **BOM history lives in GitHub tags; BC assembly BOM holds only the current mirror**, stamped with the tag name. No move to production BOMs. (Val)
- **Nathan owns and builds the GitHub→BC sync robot** on the BC API. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi Peari | Read and approve the draft hardware standard (PR in the knowledge repo); write the BOM-synchronization section | Days | High | Standard must be right before it propagates |
| 2 | Genadi Peari | Write a scope/task for Nathan describing the sync capability from this discussion | Days | High | So Nathan can start |
| 3 | Nathan Carver | Define and start building the GitHub→BC sync service on the BC API | After scope | High | Reads tag BOM CSV, rewrites BC assembly BOM, stamps tag on item card |
| 4 | Genadi / purchasing | Buy one JCM recycler unit (ship to Minsk via CMA); chase the missing bezel | Days | Normal | Second recycler source |
| 5 | Engineering | Proceed with the Rockchip 3576 8 GB board | — | Low | 16 GB not worth it |

## Open Questions
- Whether the final repo layout is confirmed or bettered — Val stressed nothing is decided until Genadi (and Pavel/Andrei) agree.
- Confirm BC assembly BOM supports the in-place "current mirror" cleanly across stock cutovers (old vs new revision while stock exists).

## Possible mis-transcriptions
- "GCM / G7" — **JCM**; "MI / MEI / Mars" — **MEI (Mars Electronics)**; "tricycle" — **recycler**; "Git LFC / GitLab" — **Git LFS / GitHub**; "bond / bomb / blob material / Billow / bone" — **BOM (bill of materials)**; "Pismo" — письмо (Russian: "letter/message" — i.e. the write-up); "Ignatiy / Eugene" — the approver, name unconfirmed; "Duncan / rootkit / left rootkit" — garble.

## Dispatch Log

---
*Processed from Plaud recording on September 25, 2026 (backlog batch 7). Source: 08-12 Engineering & Operations Strategy (Plaud).*
