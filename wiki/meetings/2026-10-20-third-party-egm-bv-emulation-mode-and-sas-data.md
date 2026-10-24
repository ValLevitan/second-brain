---
type: meeting
title: Third-party EGM port connection sync — only JVL and Aristocrat work fully over AFT; other makers' machines go to bill-validator emulation plus pulses in MVP 1; SAS 6.0+ data from them may become a paid product; the port mode is set per port; MVP 1 release on a Wednesday and first install about November 2 (Oct 20 2026, 8:31–9:04 AM)
date: 2026-10-20
aliases: [3rd part EGMs Port connection sync, Third Party EGM BV Emulation Mode and SAS Data, Oct 20 third-party EGM call, bill validator emulation mode, BV emulation, режим билвалидатор эмуляции, pulses, SAS data as a product]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Third-party EGM port connection sync (Oct 20 2026)

**Date/time:** October 20 2026 (a Tuesday), **8:31 – 9:04 AM Eastern**, about 33 minutes, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]] [[raw/Meeting_Notes_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]. Teams session "3rd part EGMs Port connection sync". **Language: Russian.**

**Who spoke** (speaker labels): [[wiki/people/andrei-klimovich.md|Andrei Klimovich]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/irina-shishko.md|Irina Shishko]] [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]. Named but not present: [[wiki/people/sebastian.md|Sebastian]], [[wiki/people/elizabeth.md|Elizabeth]], [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]], [[wiki/people/alexei-khamin.md|Alexei Khamin]] and [[wiki/people/ivan.md|Ivan]].

**Purpose.** Sum up where the Flex-Port stands on other makers' machines after the Oct-16 tests, decide how those machines connect, and set the MVP 1 dates [[raw/Meeting_Notes_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].

## Where the substance lives

- [[wiki/decisions/2026-10-20-machines-without-working-aft-connect-by-bill-validator-emulation-and-pulses-in-mvp1-and-the-port-mode-is-set-per-port.md]] — the whole substance: the state by maker, Val's "mistaken decision", AFT vs SAS data, promotional credits, the per-port mode, bill acceptors, the SAS commands seen, this week's plan, the dates, and the eight commitments.
- [[wiki/decisions/2026-09-07-flex-port-goes-sas-and-jvl-drops-the-old-machine-segment.md]] (Oct-20 update) — the dropped bill-acceptor/counter connection is back in MVP 1.
- [[wiki/decisions/2026-10-01-sas-or-no-sas-is-set-per-flex-port-on-the-flex-iq-set-up-screen-and-sent-at-registration-with-the-pin-code.md]] (Oct-20 update) — the mode switch, now in MVP 1.
- [[wiki/decisions/2026-10-18-every-gap-found-on-another-makers-machine-becomes-requirements-and-the-machine-emulator-keeps-a-mode-per-maker.md]] (Oct-20 update) and [[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]] (Oct-20 update) — the borrowed-machine results and the Friday return.
- [[wiki/decisions/2026-10-14-the-first-ten-transactional-locations-go-in-from-november-1-on-stock-monitors-ports-without-wi-fi-and-hand-made-harnesses.md]] (Oct-20 note) — first install about November 2.
- [[wiki/decisions/2026-10-20-flex-port-mvp1-needs-only-an-easy-release-build-and-the-usb-update-and-alekseev-writes-stm32-freertos-rules-for-claude-review.md]] — the earlier meeting Val came back to.
- Topic: [[wiki/topics/test-automation-strategy.md]] (Oct 20, 8:31 AM)
- People: [[wiki/people/andrei-klimovich.md]] · [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/val-levitan.md]] · [[wiki/people/sebastian.md]] · [[wiki/people/elizabeth.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/ivan.md]] · [[wiki/people/evgeniy-alekseev.md]]

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search for both filenames, "bill validator emulation", "3rd part EGMs", "October-20-2026" and "2026-10-20" found no page citing either file. It follows the [[wiki/meetings/2026-10-16-third-party-egm-flex-port-sas-connection-tests.md|Oct-16 third-party EGM call]], and Val refers to the [[wiki/meetings/2026-10-20-flex-port-mvp1-usb-update-and-build-standards.md|7:01 AM Flex-Port meeting]] as "предыдущий митинг".
- **Name calls.** "Себастьян" / "сибащена" / "себащу" = [[wiki/people/sebastian.md|Sebastian]]. "Элизабет" = [[wiki/people/elizabeth.md|Elizabeth]]. "Евгений Алексеев" / "алексеевым" = [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]]. "Алексей" who writes the story for Alekseev, and "лёша" in Irina's team = [[wiki/people/alexei-khamin.md|Khamin]] (by context). "иван" = [[wiki/people/ivan.md|Ivan]]. "Андрей" = Klimovich (he answers).
- **Garbles kept as heard.** "Живел" / "джавеловскую" / "GVL" / "джил" = JVL; "аристократ" = Aristocrat; "банила" / "ванилу" / "звонила" = Banilla (as on the Oct-16 page; the notes write "Banilla"); "ig t" = IGT; "HTT" — Klimovich uses it in the same breath as "ig t" for the same machine, so read as IGT (**inference**; the notes keep "HTT"); "littend wander" / "лайтэн" / "лайт энд" = Light & Wonder; "FC" / "af t" / "IFT" / "FT" = AFT; "сас" / "с аз" / "sass" = SAS; "билвалидатор амулейшн" / "bvation mod" = bill-validator emulation mode; "пульсы" / "palses" = pulses; "аккаунторами" / "каунтеры" = counters; "айди зиру у zal 3" = the ID-003 protocol, as the notes read it; "Джей сиен" = JCM (**inference**); "gatway" = gateway (the Flex IQ); "праймеризас" / "секундоре" = primary and secondary SAS ports; "facetereset" = factory reset; "кетчул" = schedule; "кейпобилоти" = capability; "рекламы" / "рекламент" = requirements; "квармен" — **unclear**.
- **Not recorded:** a joke of Val's about the alternative to AFT, greetings and goodbyes.
- **§15.8:** clear — the $30–50 a month is a product price, not anyone's pay. **§15 #9:** clear.

## Sources

- [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]
- [[raw/Meeting_Notes_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]
