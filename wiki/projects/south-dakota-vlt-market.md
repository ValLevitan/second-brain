---
type: project
title: South Dakota VLT market entry
date: 2025-01-22
aliases: [South Dakota, SD VLT, South Dakota lottery, South Dakota route, video lottery, Alani lottery, SDVLT, Epic 950, V43, D27, SD cap, Bioliches, Gypsy Spirit, Crazy Colt, Queen of Luxor, Liberty Spin, Rodeo Spin]
source-count: 10
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

## Printer status (Apr 3) — Epic Edge audit-ticket bug

On an Apr-3 call ([[wiki/meetings/2025-04-03-sd-printer-and-mh1-settings.md]]) the two Transact **Epic** printer models were clarified: the **Epic 950** is end-of-life; the **Epic Edge** is the current model (per Lonnie, only **Ainsworth** has started using it). Lonnie recommends Transact because ~80% of machines in his lab use them (spare-parts familiarity). Two live issues: an Epic Edge printed the **cash-out ticket correctly but scrambled the audit-ticket text** (the word "master" + period) — traced to JVL's audit-ticket implementation, needing a fix; and an **Epic 950 wouldn't power up** (possibly defective — [[wiki/people/sebastian.md|Sebastian]] troubleshooting with Lonnie). Crucially [[wiki/people/pavel.md|Pavel]] had **only tested the 950, not the Edge**, so JVL owes a new build regardless; he'll confirm with the manufacturer that the Edge's protocol and connector wiring match the 950. The Edge test unit for Minsk is delayed by the **Canada↔Belarus embargo** — routed via a Chinese supplier → Mongolia → train through Novosibirsk → Moscow → Belarus (~3 weeks; currently in Moscow). [[raw/tech_and_settings_issues-juan_martinez-april-3-2025.md]]

## Status update (Apr 5) — licence in hand, border office planned

On the Denis Desmarais call ([[wiki/meetings/2025-04-05-denis-desmarais-south-dakota-nebraska.md]]) Val stated the market entry is closing: "We're in the final stages of settling in South Dakota and Nebraska… as we speak today, I have a license in South Dakota. A VLT license… we can start operating next month in South Dakota." The SD role is **purely sales — "we're not allowed to do operations. There's no vertical integration."** [[raw/denis_desmarais_south_dakota_nebraska-April-5-2025.md]]

- **Border office plan:** open a **one-or-two-man mixed-use office right on the SD/NE border** ("I think there are two cities. One on South Dakota line and one is on Nebraska line") — commercial office in front, **small warehouse in back** to prepare machines for customers — serving **Nebraska, South Dakota, North Dakota and Wyoming** ("the area is huge"). Staffing it in the Georgia service-first mould; [[wiki/people/denis-desmarais.md|Denis Desmarais]] is the candidate being courted (after the Mar-29 Julian Puerta pitch). [[raw/denis_desmarais_south_dakota_nebraska-April-5-2025.md]]

## Trial status + office manager (May 1 2025)

From the [[wiki/meetings/2025-05-01-game-design-review.md|May-1 review]]: [[raw/game_design_review-may-1-2025.md]]

- **Software passed the regulator.** The final test build "passed from their perspective"; JVL now sends it to **GLI**, then runs a **mandatory trial for the first installation**. But JVL must also complete a **technician-training/certification program** so technicians are qualified to service the games — so the actual **first go-live is still ~45–50 days away**. [[raw/game_design_review-may-1-2025.md]]
- **SD game lineup:** Dutchville, Lions Riches, Dragons, Pennies, Liberty Spins, Clover, and Wild Cold (performance data from these won't be available before Nebraska decisions must be made). [[raw/game_design_review-may-1-2025.md]]
- **Border office manager starting May 19.** Val found "a good individual to manage our office in South Dakota" starting **May 19**, positioned **on the SD/NE border** with a new office opening there — the border-office plan from Apr 5 (candidate context = [[wiki/people/denis-desmarais.md|Denis Desmarais]], name not stated on this call — inference). Part of the revenue-focus imperative (SD/Nebraska/Georgia + the FlexPay financial product "must get revenue"). [[raw/game_design_review-may-1-2025.md]]

## MG Oil introduction — the operator and the beta offer (May 13 2025)

The Jan-7 "pursue MG Oil" decision finally produced its introduction: on **May 13** [[wiki/people/val-levitan.md|Val]] met **[[wiki/people/troy-erikson.md|Troy Erikson]]**, owner of **[[wiki/organizations/mg-oil.md|MG Oil]]** — putting a name and hard numbers to what Jan-7 had estimated as "controls most of South Dakota, ~200 locations." [[raw/mg_oil_south_dakota_intro-may-13-2025.md]] [[wiki/meetings/2025-05-13-mg-oil-troy-erikson-intro.md]]

- **MG Oil is far bigger than the Jan-7 estimate:** **~7,000 of the ~9,000 machines** in South Dakota and **~600 route locations** (vs the Jan-7 "~200 locations" guess) — the state's dominant operator by 2–3×. Company profile and fleet on [[wiki/organizations/mg-oil.md]]. (Evolution of the Jan-7 figure, not a contradiction — 200 was an early guess at accessible locations.) [[raw/mg_oil_south_dakota_intro-may-13-2025.md]]
- **Certification status Val gave Troy:** JVL had its **first GLI approval**, went through the **South Dakota lottery lab**, fixed all flagged deficiencies and **resubmitted the signed-off software to GLI a week earlier**; **GLI broke a monitor during retesting**, so JVL is shipping a new monitor before GLI resumes and issues the certificate. Val wouldn't commit to a duration — "could be a week, could be 30 days" — but "we see the finish line." Both the **V43 cabinet and the D27** are at the SD state lottery office (Troy saw them ~a month earlier). [[raw/mg_oil_south_dakota_intro-may-13-2025.md]]
- **SD office/employee (corroborates the May-1 note):** JVL's new SD office employee **starts May 19**, will open an office and train a couple of local technicians, and look for a **2,000–3,000 sq ft office/warehouse** — Val's preference is **near the Nebraska border** (Troy suggested North Sioux City on the NE/Iowa border; noted most operators are around Sioux Falls). [[raw/mg_oil_south_dakota_intro-may-13-2025.md]]
- **The beta offer (Troy):** MG Oil would be JVL's beta-test site once the lottery gives a go — **~4 A-plus locations** (Rapid City; 1–2 Sioux Falls; Pierre + Fort Pierre for the time-zone check), **one machine each, 14–21 days**, then a **10–100-machine order** at an agreed price. Val agreed to **ship six machines** to MG Oil's office; Troy keeps one in **demo mode** for the casino managers who visit daily. Coordination: Troy's GM **Dana** ↔ JVL's [[wiki/people/juan-martinez.md|Juan Martinez]]. Detail on [[wiki/people/troy-erikson.md]]. [[raw/mg_oil_south_dakota_intro-may-13-2025.md]]

### South Dakota market intel (from Troy, May 13)

- The SD market **replaces ~400 machines per year** across all manufacturers; it is a **mature market**. [[raw/mg_oil_south_dakota_intro-may-13-2025.md]]
- Competitors: **IGT** and **AGT** (both "very good companies"; **Grand Vision shares the AGT licence**), and **Grover** (the weakest — "people aren't buying anymore"). The **Signature** platform is still the best-played machine; Grand Vision's newer platform is weaker than Signature. **VLCs** are the old legacy machines being retired. [[raw/mg_oil_south_dakota_intro-may-13-2025.md]]
- A **10-machine location** typically holds two old VLCs plus a mix of AGT/Grand Vision, IGT and Grover; for a beta, MG Oil would pull the weakest machine (an old VLC or a Grover) and drop the JVL unit into an A-plus spot. [[raw/mg_oil_south_dakota_intro-may-13-2025.md]]

## Vertical V43 submission decided (May 15)

On the [[wiki/meetings/2025-05-15-game-design-nebraska-south-dakota.md|May-15 game-design review]] (mostly about Nebraska — see [[wiki/projects/nebraska-skill-market.md]]) [[wiki/people/juan-martinez.md|Juan]] added that, on new feedback, JVL now wants to submit a **vertical V43 cabinet for South Dakota**, alongside the Nebraska **D27** — so both form factors are in motion. SD is kept a **distinct math track** from Nebraska: SD has **introduced CAP** (win caps) and its wins run **even lower than Georgia**, so "what's good for South Dakota, mathematically" is *not* automatically good for Nebraska. [[raw/game_design_nebraska_south_dakota-may-15-2025.md]]

## The SD VLT six-pack — production status (May 29 2025)

On the [[wiki/meetings/2025-05-29-games-design-recap.md|May-29 games recap]], [[wiki/people/lena.md|Lena]] reported South Dakota is the **higher priority** over Nebraska (material now in hand). The SD VLT six-pack and statuses given: [[raw/games_design_recap-may-29-2025.md]]

- **Bioliches** — in **development** (screens designed, production opened; double reels on free spins). **Gypsy Spirit** — concept/GDD done, production stories starting. Both use "smaller gems." [[raw/games_design_recap-may-29-2025.md]]
- **Queen of Luxor** (GD626) — in **design** (Lena finishing screens; [[wiki/people/efim-podvoiski.md|Efim]] on the math — a reel-three pick bonus, 1/2/3 "onks" set the picks, plus free spins on reels 1–3). **Crazy Colt** — top wins being capped for market compliance; **Liberty Spin** and **Rodeo Spin** — still to-do. [[raw/games_design_recap-may-29-2025.md]]
- Art resources (**Dima, Andy, Igor Metelski**, **Anton**) are shared with Omni/Calle Ocho, limiting SD/Colombia throughput; **Vitaly** records regulator videos. No Spanish translation needed for SD. [[raw/games_design_recap-may-29-2025.md]]

## Software approved by GLI; cabinet/accessory approvals pending (June 11 2025)

On the [[wiki/meetings/2025-06-11-game-design-performance-nebraska.md|June-11 game-performance review]] [[wiki/people/juan-martinez.md|Juan]] reported JVL "**just got the South Dakota software approval from GLI**" — the certification that had been awaited since the May-13 "GLI broke a monitor during retesting" note. Still pending: the **cabinet and accessory (hardware) approvals** from GLI; per **Ivan**, GLI has an outstanding **request-for-information that [[wiki/people/genadi-peari.md|Gennady]] owes GLI**, which Juan will dig into. [[raw/games_design-june-11-2025.md]]

## Who

- Driven by [[wiki/people/val-levitan.md|Val]] with [[wiki/people/juan-martinez.md|Juan]] (regulator/operator relationship, field side) and [[wiki/people/pavel.md|Pavel]] (Minsk software); [[wiki/people/irina-makarych.md|Irina]] on printer testing and GLI diffs, [[wiki/people/sebastian.md|Sebastian]] on field service, [[wiki/people/ivan.md|Ivan]] on GLI scheduling. **Lonnie** is the SD lottery-lab tester; **"Alani"** appears as the SD lottery (supplied the SAS adapter, requested the permit-number rename) — whether Alani is the lottery entity or a person there is unclear (see Owner Decisions). [[raw/sd_vlt_recap-jan-22-2025.md]] [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## Sources

- [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- [[raw/sd_vlt_recap-jan-22-2025.md]]
- [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- [[raw/tech_and_settings_issues-juan_martinez-april-3-2025.md]]
- [[raw/denis_desmarais_south_dakota_nebraska-April-5-2025.md]]
- [[raw/game_design_review-may-1-2025.md]]
- [[raw/mg_oil_south_dakota_intro-may-13-2025.md]]
- [[raw/game_design_nebraska_south_dakota-may-15-2025.md]]
- [[raw/games_design_recap-may-29-2025.md]]
- [[raw/games_design-june-11-2025.md]]
