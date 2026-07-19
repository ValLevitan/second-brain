---
type: meeting
title: e-Wallet / TITO FlexPay-FlexPort implementation update (May 29 2025)
date: 2025-05-29
source-count: 2
---

# e-Wallet / TITO FlexPay-FlexPort implementation update (May 29 2025)

An action-list review of the e-Wallet architecture for FlexPay/FlexPort, chaired by [[wiki/people/val-levitan.md|Val]]. Attendees (as named): [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]], [[wiki/people/eugine-yavorski.md|Eugine Yavorski]] ("Егорский"), [[wiki/people/genadi-peari.md|Genadi Peari]] ("Геннадий Перий"), and "**Ирина Шишко**" ([[wiki/people/irina-shishko.md|Irina Shishko]] per transcript; she raises firmware-version-naming / test-vs-prod-folder / build-numbering questions — a QA/release-process role) (owner-confirmed 2026-07-18: meter/QA interpretation → Shishko). Continuation of the [[wiki/decisions/2025-05-27-release-ewallet-mvp-first.md|e-wallet-MVP-first]] decision.

Purpose: review the point-by-point action list. Substance — the 64KB→8KB remote-update packet change (Chudinov), the two-architecture reminder (e-Wallet vs TITO/SMIB), the 10 delivered SMIB boards + porting firmware to a cheaper fewer-pin processor (Alekseev), Yavorski's money-in/out corrections (minor-units field, real SAS device number, command logging), partial-redemption done (Chudinov, with an API for [[wiki/people/ihar-hrybko.md|Ihar Hrybko]]'s FlexPay UI), and GitHub repos (SMIB + FlexPort done, FlexPay Bitbucket→GitHub ~June 7) — is on [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. Next meeting Monday June 2, 7am.

**§12 notes.** (1) The transcript exists as a byte-identical download pair; the "(1)" copy was skipped, this base transcript is the source of record. (2) This meeting also produced a **derived "E-Wallet/FlexPay Implementation Summary & Action Plan"** ("Based on May 29, 2025 Meeting — For June 2, 2025 Review"), staged as **two files whose bodies are byte-identical** (only the frontmatter tags differ): `meeting_summary_action_plan.md` and `meeting_summary_action_plan_edited.md`. Per §12, the *edited* copy is cited as the derived source of record and the plain copy is **skipped** (byte-identical body). Its content — the 64KB→8KB packet fix, 10 SMIB boards + cheaper-processor port, partial redemption done (API for "Igor Khrebkov" = [[wiki/people/ihar-hrybko.md|Ihar Hrybko]]), FlexPay Bitbucket→GitHub moved to June-7, Genadi to plan FlexTower/POS next — is already captured above and on [[wiki/topics/flexpay-business-architecture-payout-devices.md]]; the derived doc adds no new durable facts.

## Sources

- [[raw/e-wallet_tito_flex-pay_flex-port_implementation_update-may-29-2025.md]]
- [[raw/meeting_summary_action_plan_edited.md]]
