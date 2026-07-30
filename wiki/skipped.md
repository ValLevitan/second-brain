# §12-Skip Ledger

Authoritative machine-readable list of raw files staged into `raw/` then deliberately **§12-skipped** — re-transcriptions, Obsidian numbered/conflicted copies, or session segments already covered by a fuller **source of record**. These are *handled* but will never be cited, so the pending-sweep must exclude them (see CLAUDE.md §9). This file is a ledger, **not a content page** — exclude it from the index=disk bijection count alongside index/overview/log.

Format: `raw/<skipped file>` — source of record `raw/<cited fuller file>` — reason.

## Confirmed skips

- `raw/tax_litigation_mexico-july-3-2025-1.md` — SoR `raw/mx_tax-dispute_status_review-july-5-2025.md` — depreciation/multi-component segment of the July-3 6:00pm MX-tax meeting; fuller WebVTT (4,156 lines) already carries it. (Batch 57; re-verified Batch 59.)
- `raw/tax_litigation_mexico-july-3-2025-2.md` — SoR `raw/mx_tax-dispute_status_review-july-5-2025.md` — appeals-stages/statute/fee-schedule/fiscal-domicile segment of the same July-3 session. (Batch 57; re-verified Batch 59.)
- `raw/games_design-july-8-2025 (1).md` — SoR `raw/games_design-july-8-2025.md` — Obsidian numbered re-transcription of the same July-8 games-design meeting (near-identical content, ~90.2KB both; the (1) has heavier stuck-repetition). Cited base is `wiki/meetings/2025-07-08-games-design-mathematician-debate.md`. (Batch 59.)

### Audit #6 reconciliation — the remaining 14 never-cited files (all §12-skips; 0 holes)

- `raw/7_performance_analysis_january_13_2025_2025-01-14.md` — SoR `raw/fp-7_performance_analysis_january_13_2025.md` — second transcription run of the same Jan-13 FP-7 performance meeting (jaccard 0.75; 81% of target tokens present in SoR; target-unique tokens are transcription noise/mistranslations e.g. "demagodition", "duratka"). Cited base is `wiki/meetings/2025-01-13-fp7-performance.md`.
- `raw/assisted_development_with_code_git_and_mcp_2025-01-14.md` — SoR `raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md` — lossier re-transcription of the same Jan-14 AI-dev workshop; SoR is much fuller (74.2KB vs 51.7KB norm), fullest-wins §12. Target-unique tokens are garbled tool names of the same tools ("bitfucket"/"arbitbucket"=Bitbucket, "chargegpt"=ChatGPT). Cited base is `wiki/meetings/2025-01-14-ai-dev-workshop.md`.
- `raw/mort_ansky_interview_january_2_2025.md` — no SoR (failed transcription) — 334-char stub: "[Failed to transcribe chunk 1] [Failed to transcribe chunk 2]" plus Korean auto-caption garbage; zero durable content (§12 stub rule). Underlying Jan-2 interview audio (.m4a, 40:52) never transcribed — see queue note. **[owner-closed 2026-07-20: UNRECOVERABLE — no re-transcription available; accepted timeline gap.]**
- `raw/Asimex - Importation of Flex machines.md` — SoR `raw/Asimex - Importation of Flex machines_2.md` — re-transcription of the same Asimex Flex-import meeting (jaccard 0.89; 95% of target tokens in SoR). SoR cited by 4 pages.
- `raw/asimex_importation_of_flex_machines.md` — SoR `raw/Asimex - Importation of Flex machines_2.md` — case/format re-transcription variant of the same Asimex meeting (jaccard 0.90; 96% of target tokens in SoR). SoR cited by 4 pages.
- `raw/Back office next step forward - Dzima Chudinov.md` — SoR `raw/back_office_next_step_forward_dzima_chudinov.md` — case/format re-transcription of the same back-office/CMS meeting with Dzima (Dmitri) Chudinov (jaccard 0.86; 95% of target tokens in SoR). SoR cited by 4 pages.
- `raw/andrei_klimovich_update-may-16-2025 (1).md` — SoR `raw/andrei_klimovich_update-may-16-2025.md` — Obsidian numbered copy of the same May-16 Klimovich update; base is fuller (78.9KB vs 67.3KB norm) and 99% covers the (1). Cited base is `wiki/meetings/2025-05-16-klimovich-update-echo-website-pace.md`.
- `raw/architecture_of_sql_olap_visualization_2.md` — SoR `raw/architecture_sql_olap_visualization_2_2025-03-29.md` — re-transcription of the same Mar-29 SQL/OLAP part-2 session (jaccard 0.73; 92% of target tokens in SoR; only 0.03 jaccard with the distinct part-1 file, confirming it's part-2). SoR cited by 10 pages.
- `raw/cms persona requirements-march-23-2025.md` — SoR `raw/cms_persona_requirements-march-23-2025.md` — English tool-truncated (~30 min) capture of the same Mar-23 CMS-persona meeting; fuller Russian file (98:47) is SoR. Low token jaccard (0.02) is a language difference, not distinct content. Already noted in overview.md §12 dedup; cited base `wiki/meetings/2025-03-23-cms-persona-requirements.md`.
- `raw/daily_omni_progress-april-16-2025.md` — SoR `raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md` — Obsidian conflicted-copy pair of the same Apr-16 daily Omni planning meeting; the conflicted copy is fuller (84.7KB vs 82.0KB norm) and cited. jaccard 0.92; 96% of target tokens in SoR. Cited base `wiki/meetings/2025-04-16-daily-omni-feature-story-planning.md`.
- `raw/e-wallet_tito_flex-pay_flex-port_implementation_update-may-29-2025 (1).md` — SoR `raw/e-wallet_tito_flex-pay_flex-port_implementation_update-may-29-2025.md` — Obsidian numbered copy, byte-for-content identical to base (jaccard 1.00, same char length). Cited base `wiki/meetings/2025-05-29-ewallet-tito-flexpay-implementation.md`.
- `raw/incomm_meeting—april-3-2025-2.md` — SoR `raw/incomm_meeting—april-3-2025-1.md` — 4:19 closing "markets tail" segment of the same Apr-3 InComm recording; its distinctive facts (Fannin County TX skill-machine ruling, print-on-receipt gift-card product, PA card-to-ATM product, Iowa/Nebraska expansion) are already captured on `wiki/organizations/incom.md`. The meeting stub `wiki/meetings/2025-04-03-incomm-coam-gift-card-solutions.md` explicitly names it as the not-separately-cited tail segment.
- `raw/meeting_summary_action_plan.md` — SoR `raw/meeting_summary_action_plan_edited.md` — unedited near-identical twin of the edited May-29 e-wallet action-plan doc (jaccard 0.99, same length). Cited base `wiki/meetings/2025-05-29-ewallet-tito-flexpay-implementation.md`.
- `raw/product_capability_feature_jira-may-8-2025.md` — SoR `raw/product_capability_feature-may-8-2025.md` — generic PCF research essay (cites a "2023 Gartner study", SAFe framework); not a JVL transcript and contains no JVL-specific durable facts (§12 derived/generic document). The real May-8 transcript is the SoR. Already noted in `wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md`.

### Batch 60
- `raw/2025-07-31_Transactional-Architecture-Discussion.md` — SoR `raw/transactional_architecture-july-31-2025.md` — byte-identical duplicate (md5 99353aef…, 1830 lines / 75,690 bytes both). Ingest the SoR; this copy is a filename variant of the same Jul-31 session. (Batch 60.)

### Batch 61
- `raw/development_review_2.md` — SoR `raw/game_development-july-3-2025.md` — re-transcription of the SAME Jul-3-2025 8:04PM game-development weekly (same date/time/attendees: Val/Michael Gottlieb/Lena/Efim/Juan; same topics — At-Any-Bet Jackpot Rush progressive bug on the framework side, Nebraska art schedule to end-July, HHR framework Aug-1, Texas Golden-Husk→Lone-Star nudge carry-over, Gayocho/Calle-Ocho hold drop at Hialeah, feature-level-not-story-level forecasting into GitHub, La Rosa/Fiery-Ice sequencing, grandson-born-June-18 aside). The `development_review_2` copy adds speaker labels but is TRUNCATED (ends at the ~41:07 "unrelated issue" close; ~41 min) whereas the SoR is fuller (65:35 m4a, and carries the post-close production-headcount / "Lena is the bottleneck" tail dev_review_2 lacks). Fullest-wins §12 → SoR is the source of record. Cited base is `wiki/meetings/2025-07-03-game-development-weekly.md`. (Batch 61. NOTE: staged as its own session per the batch note, but §12 cross-check against already-ingested files found it is a re-transcription of an existing meeting — prohibition #7 "never ingest both.")

### Audit #7 backfill — 6 documented §12-skips missing from the ledger (Feb–Mar batches)
*(These were correctly skipped and documented in overview.md/meeting-stub dedup notes, but never written into this ledger — so the citation-or-ledger pending sweep re-surfaced them. Backfilled 2026-07-20 per Audit #7 finding #1. Each verified: no `[[raw/…]]` wikilink citation on any content page; SoR wikilink-cited.)*
- `raw/GitHub_Commit_to_LFS_2025-02-18.md` — SoR `raw/GitHub_Commit_LFS-Feb-18-2025.md` — plain-text-blob duplicate of the WEBVTT (speaker-labelled) source of record; same Feb-18 Git-LFS session (identical open/close). Cited base `wiki/meetings/2025-02-18-git-lfs-vscode-onboarding.md`.
- `raw/game_design_meeting-2025-03-07.md` — SoR `raw/game_design_meeting_march_7_2025.md` — partial (~9k words) re-transcription of the fuller (~17.5k words, 105-min) Mar-7 game-design meeting. Cited base `wiki/meetings/2025-03-07-game-design-review.md`.
- `raw/developing_games_faster_michael_gottlieb-2025-03-12.md` — SoR `raw/developing_games_faster_michael_gottlieb_march_12-2025.md` — duplicate of the fuller Mar-12 Gottlieb "developing games faster" meeting. Cited base `wiki/meetings/2025-03-12-developing-games-faster-gottlieb.md`.
- `raw/game_development_how_animation_are_made_with_lena-2025-03-12.md` — SoR `raw/Game Development How animation are made with Lena - March 12-2025.md` — lossier line-broken 3rd transcription of the Mar-12 Lena animation meeting. Cited base `wiki/meetings/2025-03-12-lena-animation-process.md`.
- `raw/game_development_how_animation_are_made_with_lena_march_12-2025.md` — SoR `raw/Game Development How animation are made with Lena - March 12-2025.md` — near-identical 2nd transcription of the same Mar-12 Lena meeting. Cited base `wiki/meetings/2025-03-12-lena-animation-process.md`.
- `raw/recap_with_andrei_klimovichonlineecho_2025-03-29.md` — SoR `raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md` — truncated TurboScribe re-transcription (cut at "longer than 30 minutes") of the already-ingested Feb-1-2025 ECHO recap (identical specifics); the 03-29 filename is misleading. Cited base is the Feb-1 recap's meeting stub.

### Batch 71
- `raw/Flex Capabilities Weekly Update.md` — SoR `raw/Flex Capabilities Weekly Update-september-3-2025.md` — byte-identical duplicate (md5 0a9e7de0…, 40,930 bytes both); undated filename variant of the Sept-3 Flex Capabilities weekly. Ingest the dated copy. (Batch 71.)


### Batch 76
- `raw/echo_distribution_marketing-september-17-2025.md` — NO SoR (failed transcription) — 1,111-char stub of repeated "室温" (Chinese "room temperature") auto-caption garbage; zero durable content (§12 stub rule). The Sept-17 ECHO update is lost to failed transcription (Sept-15/16/26 ECHO updates are intact). (Batch 76.)

### Batch 98
- `raw/responsibilitie_split_Yavorski_Chudinov-February-5-2026.md` — SoR `raw/Aaron_Briefing_FlexPay_FlexPort_WSS-February-5-2026.md` — derived-document family member (§12): a ~1.2KB prose summary of the Feb-5 Aaron WSS responsibility-split briefing (opens "How the responsibilities are split between Eugune Yavorski and Dzime Chudinov. (Detailes are in the attached)"). Content is a subset of the briefing — Yavorski owns Flex-Port + WSS protocol spec, Chudinov owns Flex-Pay kiosk + backend, WSS is the contract, Chudinov "21 closed + 2 done", single-point-of-knowledge risk. Folded into the stub `wiki/meetings/2026-02-05-flexpay-flexport-wss-responsibility-briefing.md` (named there as the not-separately-cited derived-summary companion) and noted on `wiki/topics/flexpay-business-architecture-payout-devices.md`. NO separate stub.

### Batch 106
- `raw/Claude_Code_Implementation-Dzima_Chudinov.md` — no substance (30s greeting-only aborted-start fragment; Val / Pavel Frolov / Dzmitry Chudzinau, Feb-16 2:17pm) — no stub.

### Batch 116
- `raw/Undertakings_IT_JIRA_GitHub_Loop_Claude-March-9-2026.md` — byte-identical duplicate (md5 9ae1d6394cbd10dfcddfe94555c5396e) of `raw/IT_GitHub_JIRA_infrastructure-March-9-2026.md` (same "Call with Andrei Bosik" recording, 3:58pm/3m8s) — SoR the canonical; no stub.

### Batch 123
- `raw/SREDs_review_March-20-2026.md` — byte-identical duplicate (md5 55e4e3ae91702230e627c8f86cd85842) of `raw/SREDs_progress_review-March-20-2026.md` (same "SREDs progress review" recording, 3:05pm) — SoR the canonical; no stub. (Dup NOT staged to raw/.)

### Batch 127
- `Alignment Andrei Klimovich-March-27-2026/README.md` — bundle-manifest/index metadata (file list + attendees + session breakdown), not meeting content; substance captured via the bundle's transcripts + notes — not staged, no stub.

### Batch 128
- `Game Development March-27-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcript(s)+notes — not staged, no stub.
- `OMNI Architecture Challenge-March-27-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcript(s)+notes — not staged, no stub.
- `Review of Engineering Guides-March-27-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcript(s)+notes — not staged, no stub.

### Batch 129
- `OMNI Architecture Biratko-March-30-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcript+notes — not staged, no stub.
- `Genadi OMNI Board Communication-March-30-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcript+notes — not staged, no stub.
- `IT Follow Up Reports and Code Review-March-30-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcript+notes — not staged, no stub.

### Batch 130
- `Transcripts MCP Setup Lena-March-31-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcript+notes — not staged, no stub.

### Batch 131
- `Felipe Credit Terms Sales Strategy-March-31-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcript+notes — not staged, no stub.
- `SREDs Claim Review-March-31-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcript+notes — not staged, no stub.

### Batch 133
- `EGM_Freezing_Issue_Full_Investigation_Report-V1.2.md` (md5 4193863179502ef22a783d02edeef0a1) — SUPERSEDED by V1.3 (the folded latest full investigation report); §3/§12 superseded-version, not staged, not folded. SoR = raw/EGM_Freezing_Issue_Full_Investigation_Report-V1.3.md.
- `raw/Freezing_Investigation_Report.md` (md5 f08de3e5701cb1d7512e199e08edfde3) — "JVL Freezing Investigation — Comprehensive Report" (Claude-Code-compiled, Mar 9–25). §12 NEAR-DUPLICATE of the folded V1.3 full report: same investigation, same period, same conclusions (kernel/GPU root cause, IO-board watchdog, kernel-5.15 upgrade, South Dakota race condition, Alekseev consultation, monitoring daemon). It is fuller in *presentation* (10-theory tracker, 5 ADRs, 14-item undertakings register) but carries no durable FACT absent from V1.3, which covers the same Mar-24/25 meetings in prose (§§3–6). Per §12 "fold the fuller/canonical, skip the twin," V1.3 is the canonical source of record (Val-authored, explicitly versioned V1.2→V1.3, caller-designated latest) → this Comprehensive Report is skip-ledgered to avoid double-counting. SoR = raw/EGM_Freezing_Issue_Full_Investigation_Report-V1.3.md.

### Batch 134
- `transcript_Freezing investigation.md` (md5 e6255ca7a257c3b2e2f2953a8b28c3f3) — byte-identical duplicate of `raw/transcript_Freezing_investigation-March-25-2026.md` (same "Freezing investigation-20260325_070320" recording) — SoR the canonical; not staged, no stub.

### Batch 137
- `.claude/settings.local.json` (in the March-2026 transcript folder) — non-content Claude-config artifact (123B), not meeting/reference content — not staged, no stub, no fold.

### Batch 138
- `Code Prep Plan-April-1-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcript(s)+notes — not staged, no stub.
- `Game Development April-2-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcript(s)+notes — not staged, no stub.
- `SRED 2025 Claim Review-April-2-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcript(s)+notes — not staged, no stub.
- `Scheduling Maple-R Assembly-April-2-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcript(s)+notes — not staged, no stub.

### Batch 140
- `BOM Invoicing in Business Central-April-6-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcript+notes — not staged, no stub.

### Batch 141
- `Flex-POS Scheduling Gap Analysis-April-6-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcripts+notes — not staged, no stub.
- `Multi-Repository Project Management with Claude-April-6-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcripts+notes — not staged, no stub.

### Batch 142
- `BC Purchase Invoice Workflow-April-7-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcript+notes — not staged, no stub.
- `Accounting Dept Alignment-April-8-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcript+notes — not staged, no stub.
- `Media Tax Credit GL Requirement-April-8-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcript+notes — not staged, no stub.
- `Media Tax Credit GL Requirement-April-8-2026/OIDMTC_Car_Air_Travel_Hotel_Meals-2021-2022.xlsx` — **OUT OF SCOPE media (v1 is text-only, §1).** OIDMTC support spreadsheet (car/air/travel/hotel/meals, 2021–2022) in the Media-Tax bundle — not a transcript, not staged to raw/, no stub. Recorded so the no-file-loss audit doesn't re-flag it.
- `Media Tax Credit GL Requirement-April-8-2026/OIDMTC_Marketing_Distribution_Template-March-2024-v1.xlsx` — **OUT OF SCOPE media (v1 is text-only, §1).** OIDMTC marketing/distribution template (the prior-year format Inna reuses) — not a transcript, not staged to raw/, no stub. Recorded so the no-file-loss audit doesn't re-flag it.

### Batch 143
- `Game Development-April-9-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's three transcripts + three per-segment notes — not staged, no stub.
- `Flex-POS Alpha Build Schedule-April-10-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's two transcripts + notes — not staged, no stub.
- `Receivables Settings-April-10-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's three transcripts + three per-segment notes — not staged, no stub.
- `Receivables Settings-April-10-2026/Customer Ledger Entries (9).xlsx` — **OUT OF SCOPE media (v1 is text-only, §1).** The Business Central AR export discussed on the call (the ~400+-entry Customer Ledger Entries table Lev exports for the aging cleanup) — not a transcript, not staged to raw/, no stub. Recorded so the no-file-loss audit doesn't re-flag it.
- `Receivables Settings-April-10-2026/JVL CUSTOMER CREDIT REVISION 2.xlsx` — **OUT OF SCOPE media (v1 is text-only, §1).** Felipe's customer-terms/credit-revision spreadsheet (the source-of-truth terms Excel referenced on the call) — not a transcript, not staged to raw/, no stub. Recorded so the no-file-loss audit doesn't re-flag it.

### Batch 144
- `Aaron Claude Advancements Review-April-13-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's six transcript segments + notes — not staged, no stub.
- `Flex-POS Repo Architecture Review-April-13-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcript + notes — not staged, no stub.
- `Accounts Receivables GA-COAM-April-14-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcript + notes — not staged, no stub.
- (No out-of-scope xlsx/media in any of the three Batch-144 bundles — each contains only transcript(s), notes, and a README.)

### Batch 145
- `BC Progress Payments Payment Terms-April-15-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's two transcript segments + notes — not staged, no stub.
- `Flex-Pay Functionality Review-April-15-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's two transcript segments + notes — not staged, no stub.
- (No out-of-scope xlsx/media in either Batch-145 bundle — each contains only transcript(s), notes, and a README.)

### Batch 147
- `CI Architecture Payment Platform-April-17-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcript + notes — not staged, no stub.
- (The **Genadi Schedule Review Alignment-April-20-2026** bundle has **no README** — only transcript + notes .md — so no line for it. The **Genadi Continue Planning-April-21-2026** bundle holds **only the transcript** (no notes, no README, no media). **No out-of-scope xlsx/media in any of the three Batch-147 bundles** — recorded so the no-file-loss audit doesn't re-flag one.)

### Batch 148
- The **Transactional Financial Model-April-21-2026** bundle (dir) holds **only** the transcript + notes `.md` — **no README, no media**. The **Flex-S Cabinet Direction** meeting is **loose top-level** files (transcript + notes `.md`), not a bundle dir — **no README, no media**. Both meetings ingested as stubs; **no §12 skips** this batch. (Recorded so the no-file-loss audit doesn't re-flag either.)

### Batch 149
- Both April-24 bundle directories hold **only** the transcript + notes `.md` — the **CI Architecture Reconvene-April-24-2026** bundle has **no README, no media**, and the **Software Fix Rollout Plan-April-24-2026** bundle has **no README, no media**. Both meetings ingested as stubs; **no §12 skips** this batch. (Recorded so the no-file-loss audit doesn't re-flag either.)
  - *(Batch-150 correction: the **Software Fix Rollout Plan-April-24-2026** bundle DOES contain `README.md` and the `Letter_to_Operators_Freezing_Fix-April-27-2026.md` — the Batch-149 line above understated the bundle. Both are now handled below under Batch 150: the README ledgered, the letter ingested (folded, not skipped). No file loss.)*

### Batch 150
- `Efim Progressives Discussion-April-27-2026/README.md` — bundle-manifest/index metadata (folder title + attendees + file-contents table), not meeting content; substance captured via the bundle's transcript + notes — not staged, no stub.
- `Finance Automation Initiative-April-27-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance captured via the bundle's transcript + notes — not staged, no stub.
- `Software Fix Rollout Plan-April-24-2026/README.md` — bundle-manifest/index metadata (missed by Batch 149); not meeting content; substance captured via that bundle's transcript + notes — not staged, no stub.
- **Not skips (handled, no file loss):** `Meeting_Notes_Multi_Progressive_Initiative-April-27-2026.md` (loose top-level notes, previously un-swept) is **folded** into [[wiki/topics/slot-game-design-principles.md]] (Apr-27 multi-progressive subsection) — it is a §12 derived-notes companion of the Apr-27 8:38pm Efim call whose transcript+notes are the [[wiki/meetings/2026-04-27-efim-progressives-discussion.md]] stub. `Letter_to_Operators_Freezing_Fix-April-27-2026.md` (previously un-swept) is a §3 written operator letter, **folded** into [[wiki/topics/egm-freezing-investigation.md]] + cited on [[wiki/meetings/2026-04-24-software-fix-rollout-plan.md]]. Both are cited by content pages, so the pending-sweep no longer surfaces them.
- **No out-of-scope media this batch** — the two Apr-27 bundles (Efim Progressives, Finance Automation) contain only transcript + notes `.md` + a README; no images/xlsx/audio. (The `.docx` originals live under `_archive-dedup-2026/` and are the pre-conversion twins of the staged `.md`, handled by §12 conversion — not out-of-scope media.)

### Out-of-scope exclusions (non-JVL content — not ingested, not a §12 dup)
- `raw/koenigsegg_regera-verbal_orgasm-may-21-2025.md` — **OUT OF SCOPE (not a JVL meeting).** A YouTube-style narration/review of the Koenigsegg Regera hypercar ("…a bunch of Swedish engineers… 1,500 horsepower"), mis-filed into the May-2025 transcripts folder. Not a JVL business meeting, not §15.8-sensitive — simply off-topic per §1 scope. Excluded (recorded here so the pending-sweep and full-year no-file-loss audit don't re-flag it). Found in the 2025-complete full-year sweep, 2026-07-20.

### Out-of-scope media (owner ruling 2026-07-27 — v1 is text-only)

- `GitHub_Ways_Config_Integrations-March-16-2026.jpg` — out-of-scope media (v1 is text-only, owner ruling 2026-07-27); vault location: obsidian-jvl/Transcripts-JVL/2026/03_March/GitHub_Ways_Config_Integrations-March-16-2026.jpg — NOT staged to raw/, recorded per §1.

### Batch 151
- `CAS Cloud Migration Doc-Readiness Review-April-28-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance via transcript+notes — not staged, no stub.
- `Cash Reporting Standardization-April-28-2026/README.md` — bundle-manifest/index metadata; not staged, no stub.
- `Recycler Architecture Planning-April-28-2026/README.md` — bundle-manifest/index metadata; not staged, no stub. (Lena IP-MCP bundle has no README.)

### Batch 152
- `Flex-Recycler Development Planning-April-29-2026/README.md` — bundle-manifest/index metadata, not meeting content; substance via the bundle's notes (this bundle is **notes-only** — no transcript) — not staged, no stub.
- `Flex-Recycler REQ Daily Sync-April-29-2026/README.md` — bundle-manifest/index metadata; substance via transcript+notes — not staged, no stub.
- `CI Architecture Governance Framework Review-April-30-2026/README.md` — bundle-manifest/index metadata; substance via transcript+notes — not staged, no stub.
- `Flex-Recycler REQ Prep-April-30-2026/README.md` — bundle-manifest/index metadata; substance via transcript+notes — not staged, no stub.
- **No out-of-scope media in any of the four Batch-152 bundles** — each holds only transcript+notes `.md` + a README (the Dev-Planning bundle holds notes `.md` + README only); no images/xlsx/audio. (Recorded so the no-file-loss audit doesn't re-flag one.)
