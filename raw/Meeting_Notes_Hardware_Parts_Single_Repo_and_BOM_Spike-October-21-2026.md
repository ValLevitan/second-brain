# Meeting Summary — Hardware parts repositories for Flex - repo structure and BOM assembly
**Date:** October 21, 2026, 10:01 AM – 10:20 AM Eastern
**Duration:** about 18 min
**Attendees:** Val Levitan, Andrei Bosik
**Raw transcript:** [[Meeting_Transcript_Hardware_Parts_Single_Repo_and_BOM_Spike-October-21-2026]]

Held in Russian. Some terms are garbled in the transcript.

## Summary

**Why many repos.** Val wanted to learn how a bill of materials (BOM) gets assembled from single parts in GitHub. Each part (purchased part datasheets, JVL drawings and specs) has a data contract that lists what the part can do. Val proposed many repos (harnesses, monitors, Genadi's sheet metal) so a GitHub Action could assemble sub-assemblies, the same way Actions build the ISO image for developers.

**One repo instead.** Andrei: a repo is only a storage level. One repo with subfolders works the same; an Action can read any subfolder. Many repos are harder for Genadi to work with, and parts overlap (board, power supply, cables between them). Splitting later is easy; joining is hard. Val accepted this and closed the question.

**Spike: power supply sub-assembly.** Val wants a first raw test: build the power supply sub-assembly from purchased parts, Genadi's metal drawings and the purchased harness, using data contracts and Actions. The output is a BOM (in place of an ISO image). Nathan then loads the BOM into Business Central. The data contract also explains the function: power in, 12 V and 5 V out.

**No manual work.** Today Genadi builds this by hand in Excel. Val does not want that, for two reasons: to save Genadi's time, and because an automatic BOM is a key checkpoint. If the BOM builds correctly, the data contracts, datasheets and data are right. Val does not want this milestone faked by hand. Genadi only discusses the logic. Andrei may ask Genadi how he works today, but only to learn what not to do.

**Who checks the data contracts.** Val: Claude can write data contracts from the datasheets. Val would read them only when a BOM fails. An audit agent should find parts that did not land in any sub-assembly. Andrei worried that an early error spreads; Val said a failed build or the audit will show it.

**Val stays in the loop.** Val asked Andrei to study the topic but not to move him aside or settle things with Genadi without him. Andrei asked for a technical spec; Val said this transcript is the spec.

## Decisions Made

- **Hardware parts go into one repository with subfolders, not many repositories.** — Easier to work with, parts overlap, can split later. (Val, on Andrei's proposal) This replaces the Oct 20 plan to settle repos vs tags by email.
- **First spike: build the power supply sub-assembly BOM automatically from data contracts and GitHub Actions; Nathan loads it into Business Central.** (Val)
- **Genadi does not build the BOM by hand; he only discusses the logic.** (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Bosik | Study the topic, take the spec from this transcript, and prepare the power supply BOM spike | Tue Oct 27, 2026 | Normal | Busy Thu–Fri with PM agent and autotests with Zhenya |
| 2 | Val Levitan | Book a meeting with Andrei for Tuesday Oct 27 at 7:00 | Before Oct 27, 2026 | Normal | Andrei asked for Tuesday, not Friday |

## Open Questions

- Who reviews the data contracts Claude writes, before a BOM fails? Andrei thinks Genadi; Val would only read them on a failure. (Andrei)

## Dispatch Log

---
*Processed from Teams transcript on October 21, 2026*
*Source meeting: Hardware parts repositories for Flex - repo structure and BOM assembly*
