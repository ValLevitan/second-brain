---
type: project
title: South Dakota VLT market entry
date: 2025-01-22
aliases: [South Dakota, SD VLT, South Dakota lottery, South Dakota route, video lottery, Alani lottery, SDVLT, Epic 950]
source-count: 3
---

# South Dakota VLT market entry

JVL's effort to enter the South Dakota video-lottery-terminal (VLT) route market. It began with the MG Oil opportunity (Jan 7) and, by late January, was in lab testing with the South Dakota lottery ahead of a first field release. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]] [[raw/sd_vlt_recap-jan-22-2025.md]]

## Market opportunity (Jan 7)

- **MG Oil** controls most of South Dakota and could give JVL access to ~200 locations via an introduction; JVL decided to pursue it. See [[wiki/decisions/2025-01-07-pursue-mg-oil-south-dakota.md]]. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]

## Lab testing and certification path (Jan 22)

- The regulator/lab contact **Lonnie** is testing JVL's machine in the South Dakota lab. He agreed to accept **unapproved / experimental software** for pre-testing, which lets JVL iterate and reduce GLI costs before submitting final software to GLI. (Lonnie's exact affiliation — regulator vs. Light & Wonder lab — is unclear; see Owner Decisions.) [[raw/sd_vlt_recap-jan-22-2025.md]]
- Lonnie becomes tied up with lottery projects from **Feb 10**, so JVL has until ~Feb 9 to get software tested; the target is an urgent GLI approval and a first release around **Feb 1**, to be in the field by Feb 10. [[raw/sd_vlt_recap-jan-22-2025.md]]
- Val's caution: don't exhaust Lonnie's goodwill by over-using the unapproved-software favour. [[raw/sd_vlt_recap-jan-22-2025.md]]
- The system in the SD lab is a **Light & Wonder** (SAS) accounting system; JVL asked Light & Wonder for the lab system logs, and uses a **SAS emulator in Minsk** to reproduce ticket printing. [[raw/sd_vlt_recap-jan-22-2025.md]]

## Product issues to resolve for South Dakota

- **Printers:** the market's #1 printer is the **Transact Epic 950**, followed by FutureLogic/"Paycheck" printers; JVL must support the Epic 950. A **FutureLogic Gen 5** vs **Gen 2** discrepancy exists (software was written for Gen 2). See the printer decision [[wiki/decisions/2025-01-22-support-epic-950-printer-for-south-dakota.md]] and [[wiki/topics/jvl-machine-lineup.md]]. [[raw/sd_vlt_recap-jan-22-2025.md]]
- **Game-shutdown countdown bug:** the end-of-day "game about to be turned off" countdown (a lottery requirement) was wrongly triggering whenever the door was opened / the service menu was entered — a SAS-event handling issue to find urgently. [[raw/sd_vlt_recap-jan-22-2025.md]]
- **Volume:** operators want very quiet machines (Midwest venues where "you could hear a pin drop"); add an option to lower volume to zero. [[raw/sd_vlt_recap-jan-22-2025.md]]

## Status update (Feb 19)

The Feb 1 release target slipped; as of Feb 19 the regulator is tied up on another project for February, so JVL has a few weeks before the machine is touched again and now aims to send beta software to the lab in **early March** (this supersedes the Jan 22 "release ~Feb 1, field by Feb 10" plan). [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

- **Done:** the audit-ticket changes (Lonnie provided a sample); the Tito "void after business day" bug (verified by the test lab); Gen 5 / Gen 2 ticket-printer support; and the **"asset" → "permit number"** menu rename requested by the Alani lottery. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- **In progress:** **Epic 950** printer support (Pavel hopes to inject it by end of the next week); Epic Edge and nano-optics/Anoptic still pending. The Jira **cross-project release is SDVLT 1.11.5**, main feature **CT5029 (Transact Epic 950 printer support)**, datacenter version 3.9.6 with the build number TBD; each submission must get a new incremented version number. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- **Mystery freeze:** a lab machine froze/went offline twice (rebooting fixed it) then never again; the fan was correctly blowing inwards from the factory; cause unknown (possible overheating). Plan: ship a **brand-new, well-tested** CPU board/assembly and have [[wiki/people/sebastian.md|Sebastian]] install it and swap the Gen 5 for an Epic 950 for Lonnie to test. Ship **three printers to the lottery/Lonnie and three to GLI** (all brand new). [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- **SAS harness:** [[wiki/people/genadi-peari.md|Gennady]] is replicating a SAS harness from the manufacturer's schematics to replace the lottery-supplied adapter. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- **RTP/math issue:** JVL's partner misinformed it on which RTPs the regulator accepts, so only one was submitted; a future conversation (Val, [[wiki/people/efim-podvoiski.md|Efim]], "Michael," and the regulator) may tweak the math to offer an additional ~92% RTP after go-live. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- **Release discipline:** Val told Pavel to put [[wiki/people/ivan.md|Ivan]] on scheduling GLI ahead of time and to "loop" — keep checking the scheduled work is actually done. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## Who

- Driven by [[wiki/people/val-levitan.md|Val]] with [[wiki/people/juan-martinez.md|Juan]] (regulator/operator relationship, field side) and [[wiki/people/pavel.md|Pavel]] (Minsk software); [[wiki/people/irina-makarych.md|Irina]] on printer testing and GLI diffs, [[wiki/people/sebastian.md|Sebastian]] on field service, [[wiki/people/ivan.md|Ivan]] on GLI scheduling. **Lonnie** is the SD lottery-lab tester; **"Alani"** appears as the SD lottery (supplied the SAS adapter, requested the permit-number rename) — whether Alani is the lottery entity or a person there is unclear (see Owner Decisions). [[raw/sd_vlt_recap-jan-22-2025.md]] [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## Sources

- [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- [[raw/sd_vlt_recap-jan-22-2025.md]]
- [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
