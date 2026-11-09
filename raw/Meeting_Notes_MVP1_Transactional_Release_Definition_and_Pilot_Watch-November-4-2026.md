# Meeting Summary — MVP1 Transactional - release sync and pilot field watch
**Date:** November 4, 2026, 8:00 AM – 9:28 AM Eastern
**Duration:** ~85 minutes
**Attendees:** Andrei Klimovich, Pavel Frolov, Irina Shishko, Val Levitan, Andrei Bosik, Dzmitry Chudzinau
**Raw transcript:** [[Meeting_Transcript_MVP1_Transactional_Release_Definition_and_Pilot_Watch-November-4-2026]]

## Summary

Held in Russian. Unclear words are marked "heard".

**Purpose (Andrei Klimovich).** Agree what is still not ready for MVP 1, how the release is made, who owns which Jira status, and how the first real location will be monitored. The location and machines are known; hardware (harnesses, brackets) is being prepared.

**Current state (Pavel).** Everything tagged MVP1 Transactional is Completed. Flex IQ releases are built by a GitHub release action, tagged to a commit, and the production build is uploaded to the AWS S3 store; from there it can be downloaded or pushed by remote update through the customer dashboard. Flex-Port updates work only via USB; remote port update is MVP 2. The Flex-Port release build exists only on GitHub, not on any production server.

**What "done" means.** Val: a release is done only when it is on the production server, cleaned of all development hooks and tools, with a number. After that nothing is added; only bugs are fixed, under the bug standard. Anything else goes to MVP 2 (or 2.5). The goal is a clear boundary between development and the market, so nobody calls Pavel on a Saturday. Pavel first objected that he wants to download the same build from GitHub; Val asked him to cool down; after discussion Pavel saw no objection. Pavel keeps the ability to rebuild any version from its GitHub tag; Val does not want to take GitHub access from anyone. Dzmitry: release = binary plus code snapshot; code stays on GitHub, binary goes to the server. For server services, Andrei Bosik runs the production deploy action.

**Release notes, compliance and exception reports.** Val: a release manager (not people writing by hand) uses Claude to write the release notes and to check them against the MVP capabilities and the prose in the repositories. Output is two reports: a compliance report and an exception report. Exceptions go to product ownership: either the capability is downgraded and requirements move to MVP 2, or the release waits. Dzmitry proposed a Claude step at the end of the GitHub Action; Pavel agreed it is one step. Andrei Bosik: this belongs before the release; a failed check must fail the release. Val: yes, it fails with an error. The release manager is Ivan Shpak, who reports to Irina; Irina sets up the release process.

**Jira status flow (agreed).** Developer finishes a feature branch, merges to GitHub → feature Completed. After the end-to-end test at capability level: features → Done (never touched again), capability → Completed. After the release (no exceptions, or exceptions approved by product ownership): capabilities → Closed. Requirements stay alive and are rarely retired. All MVP 1 features and autotests must move to Closed as the first trigger for release preparation. Val: the "Request Review" status on features dates from the peer-review plan and is replaced by Claude code review; Irina: it duplicates another status and confuses people. Agreed as an undertaking: Dmitri Kovalchuk removes it; if designers need it, split design features from development features. Andrei Bosik will explain it to Dmitri Kovalchuk from the transcript. Dmitri Kovalchuk also checks why a red build-error marker sits on a Completed item (Jira remembers the first build).

**Release standard.** Val asked Pavel to write the release flow into the standards knowledge repository (with Claude) so every Claude reads it as guard rails.

**MVP 1 scope gap: Flex-Port build download.** The dashboard shows production versions only for Flex IQ. Val: if the client cannot take it, it does not exist; MVP 1 cannot be released. Andrei Klimovich and Pavel argued it should not block (Andrei takes the port build from GitHub; the client needs a flashed port, not firmware). Val held firm. Dzmitry: Sergey's work can be split; uploading Flex-Port builds to the S3 dashboard takes a few days with testing; remote port update stays MVP 2. Val: it is one day, so it goes into MVP 1. Andrei Klimovich adds the requirement or capability to MVP 1 now. Two port artifacts will be downloadable: the programmer image (bare boards from the factory, for internal manufacturing) and the USB update. Andrei Klimovich: external operators do not update builds; JVL does. Andrei Bosik asked for release notes and a PDF manual next to the artifacts; Dzmitry: manuals in MVP 2.

**Installation and monitoring.** Locations are prepared in the warehouse: build on SD card, IQ registered to the location, ports flashed; InComm already approved the licence data. First location is an hour from the warehouse. Three locations are approved. Location 1: one JVL on SAS, one Aristocrat on SAS, and two HT in bill-validator mode. Irina: that means bill-validator mode gets tested in the field. Mixed mode in one location was tested in the warehouse "zoo". All port and terminal logs go to the servers; Dzmitry can add Grafana dashboards and alerts (paper out, long disconnect) in a later MVP. Andrei Klimovich has never updated ports by USB stick, only by programmer, and will test it; a USB harness may be needed for access in the bracket. Irina: USB is a one-time update; later updates are remote. InComm's second product is paused (regulator strike), so one product only.

**SIM data limit.** A day or two before the meeting a SIM ran out of data. Current limit is 4.5 GB; Andrei Klimovich can set any number (10 GB suggested). Current traffic is about 160 MB per day (about $1.50 per day); Dzmitry can thin repeated logs; Pavel: keep the high log volume for the first locations. Dzmitry had proposed (Pavel relayed it) that the machine report its SIM to the server so a micro-service can read traffic from the provider API. Andrei Bosik: such notifications are the provider's job. Andrei Klimovich will give admin rights to the SIM portal so someone can look for the setting. Traffic alerting goes to MVP 2.

**Tone.** Val asked for a more formal meeting and for Pavel to lower the tone; Dzmitry's "our Andrei" remark was noted as unkind to Andrei Klimovich; Val said he was also offended by Andrei Klimovich's "not part of your team" remark. The meeting closed on good terms.

## Decisions Made

- **"Done" means the cleaned release build is on the production server (AWS S3 store) under a number; only bug fixes after that; new work goes to MVP 2.** (Val; Pavel, Dzmitry, Andrei Bosik agreed)
- **Pavel keeps the ability to rebuild any release from its GitHub tag; nobody loses GitHub access.** (Val)
- **Release manager produces Claude-generated release notes plus a compliance report and an exception report; exceptions go to product ownership; a failed check fails the release.** (Val, Andrei Klimovich, Andrei Bosik)
- **Ivan Shpak is the release manager, reporting to Irina.** (Val)
- **Jira flow: features Completed → Done after the end-to-end test; capability Completed; after release capabilities → Closed; requirements stay open.** (Val, Irina, Pavel, Andrei Klimovich)
- **"Request Review" is removed from the feature workflow, or design features are split from development features.** (Val, Irina, Pavel)
- **Flex-Port build download (programmer image + USB update) is added to MVP 1 scope.** — About one day of work. (Val; Andrei Klimovich accepted)
- **SIM data limit stays as set by Andrei Klimovich (4.5 GB, can be raised); traffic alerting and SIM binding go to MVP 2.** (Andrei Klimovich, Dzmitry)
- **Manuals next to the artifacts go to MVP 2.** — Release notes beside the artifacts (Andrei Bosik's ask) were not decided. (Dzmitry)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Add the Flex-Port build download requirement/capability to MVP 1 in Jira (programmer image and USB update) | Nov 4, 2026 | High | "sit down and write it now" |
| 2 | Dzmitry Chudzinau, Sergey Tsimanov | Finish the Flex-Port build upload to the S3 dashboard, verify on STG, release | Nov 5, 2026 | High | Val: one day |
| 3 | Irina Shishko | Set up the release process and drive Ivan as release manager | TBD | High | |
| 4 | Ivan Shpak | Act as release manager: release notes, compliance and exception reports, move capabilities to Closed | TBD | High | Ivan was not in the meeting |
| 5 | Irina Shishko and team | Move all MVP 1 features and autotests to Closed | TBD | High | First release trigger |
| 6 | Pavel Frolov | Write the release standard into the standards knowledge repository | TBD | Normal | |
| 7 | Dmitri Kovalchuk | Remove "Request Review" from the feature workflow or split design and development features; check the Jira build-error marker | TBD | Normal | Not in the meeting |
| 8 | Andrei Bosik | Brief Dmitri Kovalchuk from the transcript | TBD | Normal | |
| 9 | Andrei Klimovich | Test a USB-stick firmware update on ports in the warehouse; check USB access in the bracket | TBD | Normal | |
| 10 | Andrei Klimovich | Give admin rights to the SIM portal to the team | TBD | Low | |
| 11 | Dzmitry Chudzinau | MVP 2 tasks: traffic limit alert, SIM-to-terminal binding, log thinning | MVP 2 | Normal | |
| 12 | Dzmitry Chudzinau | Add the Claude release-notes step to the GitHub Action | TBD | Normal | Proposed by Dzmitry; Pavel agreed; not formally assigned |

## Open Questions

- Whether the SIM provider portal can send its own data-limit notifications. (Andrei Bosik)
- Whether MVP 2 gets a Jira notification "when ready" (Andrei Klimovich, unclear audio).
- Testing two InComm card products is on hold while the second product is paused. (Dzmitry)
- Release notes and a PDF manual placed next to the download artifacts. (Andrei Bosik asked; manuals deferred to MVP 2, release notes not decided)

## Dispatch Log

---
*Processed from Teams transcript on November 5, 2026*
*Source meeting: MVP1 Transactional - release sync and pilot field watch*
