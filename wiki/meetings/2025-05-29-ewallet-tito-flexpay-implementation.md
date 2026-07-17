---
type: meeting
title: e-Wallet / TITO FlexPay-FlexPort implementation update (May 29 2025)
date: 2025-05-29
source-count: 1
---

# e-Wallet / TITO FlexPay-FlexPort implementation update (May 29 2025)

An action-list review of the e-Wallet architecture for FlexPay/FlexPort, chaired by [[wiki/people/val-levitan.md|Val]]. Attendees (as named): [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]], [[wiki/people/eugine-yavorski.md|Eugine Yavorski]] ("Егорский"), [[wiki/people/genadi-peari.md|Genadi Peari]] ("Геннадий Перий"), and "**Ирина Шишко**" ([[wiki/people/irina-shishko.md|Irina Shishko]] per transcript; she raises firmware-version-naming / test-vs-prod-folder / build-numbering questions — a QA/release-process role that may actually be [[wiki/people/irina-makarych.md|Makarych]]; not reconciled, Tier A). Continuation of the [[wiki/decisions/2025-05-27-release-ewallet-mvp-first.md|e-wallet-MVP-first]] decision.

Purpose: review the point-by-point action list. Substance — the 64KB→8KB remote-update packet change (Chudinov), the two-architecture reminder (e-Wallet vs TITO/SMIB), the 10 delivered SMIB boards + porting firmware to a cheaper fewer-pin processor (Alekseev), Yavorski's money-in/out corrections (minor-units field, real SAS device number, command logging), partial-redemption done (Chudinov, with an API for [[wiki/people/ihar-hrybko.md|Ihar Hrybko]]'s FlexPay UI), and GitHub repos (SMIB + FlexPort done, FlexPay Bitbucket→GitHub ~June 7) — is on [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. Next meeting Monday June 2, 7am.

**§12 note:** this source exists as a byte-identical download pair; the "(1)" copy was skipped, this base file is the source of record.

## Sources

- [[raw/e-wallet_tito_flex-pay_flex-port_implementation_update-may-29-2025.md]]
