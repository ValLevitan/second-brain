---
type: project
title: South Dakota VLT market entry
date: 2025-01-22
aliases: [South Dakota, SD VLT, South Dakota lottery, South Dakota route, video lottery]
source-count: 2
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

## Who

- Driven by [[wiki/people/val-levitan.md|Val]] with [[wiki/people/juan.md|Juan]] (regulator/operator relationship, field side) and [[wiki/people/pavel.md|Pavel]] (Minsk software). [[raw/sd_vlt_recap-jan-22-2025.md]]

## Sources

- [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- [[raw/sd_vlt_recap-jan-22-2025.md]]
