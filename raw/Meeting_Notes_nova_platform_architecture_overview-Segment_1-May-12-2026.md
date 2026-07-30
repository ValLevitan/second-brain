# Meeting Summary — NOVA Platform Architecture Overview (Segment 1: As-Is Walkthrough)
**Date:** May 12, 2026, 12:20 PM Eastern
**Duration:** 14m 35s
**Segment:** 1 of 2
**Attendees:** Val Levitan, Alexander (Sasha) Biratko, Irina Shishko, Anton Leshkevich

> **Initiative cross-reference:** This meeting is the founding architecture session for what becomes the **NOVA Gaming Platform** (named in Segment 2). Canonical initiative record: `obsidian-jvl/Initiatives/NOVA Platform Architecture/`. These transcript notes capture the conversational record; design ADRs roll up under the initiative.

## Transcript Quality Note

Entire conversation in Russian. Summary in English. Sasha drove a whiteboard diagram throughout — the verbal record describes components and relationships, but the *visual* layout that grounded the discussion lives only in the shared whiteboard / Miro board file, not in the transcript.

## Summary

Sasha Biratko walked the team through the **current architecture of the on-cabinet platform** (what the team had previously been calling "Omni") — diagram on screen, component-by-component. Val explicitly framed the scope: *"let's first complete 'as is', then move to 'to be'."* This segment is the as-is pass.

**Naming guard rail set up front.** Val opened by saying the team will not call this platform "Omni" anymore and won't decide on what to call it during this session. Provisional handle: just *"that product, omni"* — purely as a placeholder. The actual naming decision happens in Segment 2.

**Scope of the diagram.** Per Sasha: the yellow blocks on screen are applications running **on the cabinet hardware itself (EGM)** — the structure of software running on the EGM. Signage is excluded from this scope (it doesn't run on the EGM). Anton's working name during the session was "land-based platform," tracking Irina's prior framing.

**Core architectural layers, as-is:**

- **LGS** sits at the centre. Currently the **central hub** through which all other elements communicate. In the new configuration the team had been working on, "Frob" (frol-over) no longer talks directly to the math engine — *all* communication now flows through LGS. Example: if the framework wants to ask the math engine for math, it asks LGS, LGS asks the math engine, and the answer comes back through LGS.
- **Linux OS + HAL** is the lowest layer. HAL = Hardware Abstraction Layer — the scripts and system libraries (correct Java version, correct Chrome browser version, codecs, system utilities) that the rest of the stack depends on. Has its own dedicated repository for assembling these system libraries.
- **Setup UI and In-Setup UI** are currently inside the LGS repository. They were briefly in separate repos historically, but they have no independent use case outside LGS, and the separation caused versioning drift between UI version and LGS version. Now in the same repo, so they build together.
- **Arrange and MathEngine** are Docker containers. Hold a *universal* math engine that works for both online and land-base, and a *universal* arrange (RG) server and a universal math engine server. Arrange server is contacted only by MathEngine — nobody else needs it. (Theoretically the progressive controller could touch arrange, but it currently runs on its own internal arrange.)
- **System libraries** (SoundLib, PrinterLib, BillLib, BoardLib, etc.) are currently **Java-native modules loaded into LGS's memory**. *Any error inside these libraries crashes all of LGS* — this is a known fragility.

**Planned upgrade (which Sasha tried to mix in, but Val redirected to finish "as is" first).** The team plans to convert the in-process Java native library modules into **standalone applications** ("self-standing services" / "services"). Discussed only verbally; Sasha agreed to defer the to-be detail to Segment 2.

**Firmware ownership.** Sasha enumerated firmware sources:
- **Printer firmware** is *not* written by JVL — it ships on the printer; not in scope.
- **BillBoard / Driver firmware** *is* written by JVL.

**Progressive controller.** Two variants currently exist:
- **External progressive controller.**
- **MBD (motherboard-on-device) variant** — most current installations use MBD.
- **Signage progressive controller** — placed directly on the signage device. Irina noted this is more relevant to legacy platforms; for *this* platform there's no signage yet. Sasha kept the box on the diagram anyway as a known-existing variant.

The progressive controller communicates with LGS — finds it in its environment and connects.

**Tools.** Two on the diagram:
- **Miranda** — a **Unity plugin / application** for creating game scenes. A *scene* = group of files unified by a single descriptive JSON file that distributes graphics, video, and text layout per the designer's plan. Based on the GameFramework. Multiple games can use the same Miranda-built scenes.
- **TS-360** — a broad-profile test tool. Creates Notes that test from button-press to result (player presses Spin → win amount → animation → counter increment → LGS history record). TS-360 has direct connections to both games and LGS (LGS is the source-of-truth for state being tested).

**CMS.** An *external* service. Two functions: it **configures LGS** (to a degree) and **collects statistics from LGS on the machine**. LGS is the storage point for both statistics and configuration. CMS talks directly to LGS.

**New elements.** Flex-Pay and Flexport added on the diagram as new elements. Flex-Recycler, Flex-Dispenser, and Flex-POS exist as JVL variants but have not yet been integrated into this platform's architecture, so they are not on the diagram yet.

**Val's redirect on scope.** When Sasha started inserting "we plan to make these into services" mid-presentation, Val stopped him: *"are you describing how it works *now* or what we want to build?"* Sasha confirmed "now." Val: *"let's finish 'as is' first; then we'll go to 'to be'. We're not even calling it Omni yet — we just call it Omni as a code word until we know what it is."* Sasha accepted: *"if we look at it that way, then we're discussing the omni architecture for now."*

**Session close.** Sasha said: *"if there are questions."* Anton: *"all clear."* Val stopped the recording. Segment 2 (the to-be design + naming) follows immediately.

## Decisions Made

- **As-is pass first, to-be design separate** — verbal scope rule, applied through the rest of the session. (Val.)
- **Scope of "the platform" = software running on the EGM cabinet itself.** Signage explicitly excluded. (Sasha, with Val.)
- **LGS remains the central hub** in the current architecture; all inter-component communication goes through LGS. (As-is fact, not new.)
- **System libraries (SoundLib, PrinterLib, BillLib, BoardLib, etc.) are today in-process Java-native modules loaded into LGS; this is the *known fragility* to address in the to-be design** — any library error crashes all of LGS. (As-is fact named explicitly as the migration driver.)
- **Setup UI / In-Setup UI remain in the LGS repo** (versioning rationale). (As-is fact.)
- **Arrange + MathEngine are Docker containers running universal math** that works for both online and land-base. (As-is fact.)
- **No signage in scope for this platform** (Irina's clarification, accepted). Signage progressive controller box stays on the diagram as a known external variant.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexander Biratko | Continue the architecture session — proceed to the to-be discussion in Segment 2 | Immediately after recording stop | High | The structural to-be decisions land in Segment 2 |
| 2 | All | Defer all naming and to-be design framing until the as-is is fully described | This session | Normal | Val's discipline: don't conflate current state with planned state |

## Engineering Signals

### Confirmed Signals

- **ADR — LGS as the single point of inter-component communication (as-is state).** Captured here for the record; the to-be design (Segment 2) will explicitly evolve this.
- **CAP — Hardware Abstraction Layer (HAL) repository.** Owns Linux system libraries, correct Java/Chrome versions, codecs, system utilities. Already exists as a separate repo today.
- **CAP — Universal MathEngine + Arrange in Docker containers** working for both online and land-base.
- **CAP — Miranda scene-authoring tool** as a Unity plugin producing JSON-described scenes consumed by GameFramework.
- **CAP — TS-360 test harness** spanning game-to-LGS history validation.
- **ADR (driver) — Library fragility under in-process Java-native loading.** The fact that a library bug crashes all of LGS is the explicit motivation for the to-be migration to standalone services.
- **REQ — JVL writes BillBoard and Driver firmware; does NOT write printer firmware.** Material to the responsibility map of the to-be architecture.

### Suspected Signals

- **Possible CAP — Flex-Pay / Flexport integration into the on-cabinet platform.** Newly added boxes on the diagram. Flex-Recycler / Flex-Dispenser / Flex-POS variants also expected but not yet integrated. — *Val, are these planned for the to-be architecture as separate services, or absorbed under existing services?*
- **Possible CAP — Signage progressive controller in the to-be platform.** Irina argued no signage in scope; Sasha kept the box. — *Worth deciding explicitly: is signage out of scope permanently, or just for the first NOVA pass?*

## Open Questions

- **Is the signage progressive controller in or out of scope?** Sasha and Irina disagreed mildly; not resolved.
- **What is the to-be design for the library/service decomposition?** Sasha started to describe it, Val deferred to Segment 2.
- **How do Flex-Recycler / Flex-Dispenser / Flex-POS surface in the to-be architecture?** Not yet integrated, no current diagram representation.

---
*Processed from Teams transcript on May 22, 2026*
*Source meeting: Overview_services_land-based_platform-May-12-2026 (20260512_082020) — Segment 1 of 2*
