---
type: meeting
title: Call with Pavel Frolov and Irina Shishko ("Alignment by the coffee machine") — modems on the machines have no reliable date (mixed firmware and carrier locks; the modem test tool is released); Georgia build 4377 with all fixes and the modem goes to Elizabeth and Sebastian to test on different modems before the lab; the 20 revision-2 boards go back to Alekseev, no more experiments; reliable remote updates and Wi-Fi setup are the two must-haves for transactional version 2; an update failed in Seregin's autotests; the Flex-Port update path and Wi-Fi setup as built; South Dakota GLI status; no date for the first transactional install (Nov 23 2026, ~11:46 AM–~12:18 PM)
date: 2026-11-23
aliases: [Alignment by the coffee machine Nov 23 2026, Pavel Irina LTE Modem Build Rev 2 Boards and WiFi Updates, Nov 23 Pavel Irina call]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Call with Pavel and Irina — modem build, revision-2 boards and Wi-Fi/updates (Nov 23 2026, ~11:46 AM)

**Date/time:** Monday November 23 2026, **~11:46 AM – ~12:18 PM Eastern**, about 32 minutes, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_Pavel_Irina_LTE_Modem_Build_Rev_2_Boards_and_WiFi_Updates-November-23-2026.md]] [[raw/Meeting_Notes_Pavel_Irina_LTE_Modem_Build_Rev_2_Boards_and_WiFi_Updates-November-23-2026.md]]. Teams title "Alignment by the coffee machine", Val organizer [[raw/Meeting_Notes_Pavel_Irina_LTE_Modem_Build_Rev_2_Boards_and_WiFi_Updates-November-23-2026.md]]. **Language: Russian.** Between the [[wiki/meetings/2026-11-23-nova-sync-ip-481-root-and-weekly-mvp-plan.md|~8:14 AM NOVA sync]] and the [[wiki/meetings/2026-11-23-genadi-rev-2-boards-monitor-controller-sourcing-and-data-contracts.md|~1:17 PM Genadi call]] the same day.

**Who spoke** (speaker labels): [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]] [[raw/Meeting_Transcript_Pavel_Irina_LTE_Modem_Build_Rev_2_Boards_and_WiFi_Updates-November-23-2026.md]].

**Purpose:** Val's check-in on the transactional and Georgia work: modems, the Georgia build, the boards, updates and Wi-Fi [[raw/Meeting_Transcript_Pavel_Irina_LTE_Modem_Build_Rev_2_Boards_and_WiFi_Updates-November-23-2026.md]].

## Where the substance lives

- [[wiki/decisions/2026-11-23-the-20-revision-2-boards-go-back-to-alekseev-for-repair-build-4377-with-the-modem-is-field-tested-on-different-modems-before-the-lab-and-remote-updates-and-wi-fi-setup-are-the-two-must-haves.md]] — modems, build 4377, the boards ruling, updates and Wi-Fi, the install date; all commitments and questions.
- Earlier rulings with Nov-23 notes: [[wiki/decisions/2026-11-05-the-modem-stays-always-on-with-no-operator-on-off-screen-and-is-disabled-only-through-a-deliberate-qr-scan-server-event-and-activation-code-routine.md]] · [[wiki/decisions/2026-11-05-mvp-2-is-kept-narrow-wi-fi-with-the-flex-iq-as-access-point-or-client-remote-flex-port-update-robust-installation-and-install-diagnostics-due-november-20-and-the-rest-goes-to-mvp-3-around-january-20.md]] · [[wiki/decisions/2026-11-20-a-failed-flex-port-firmware-update-is-not-shown-on-the-port-screen-and-hardware-only-autotest-scenarios-are-marked-manual-in-a-separate-feature.md]] · [[wiki/decisions/2026-11-23-genadi-first-finishes-the-data-contracts-and-loads-every-data-sheet-into-github-and-supplier-search-becomes-agent-logic-built-on-them.md]]
- Topics / projects: [[wiki/topics/test-automation-strategy.md]] · [[wiki/projects/south-dakota-vlt-market.md]] (both Nov 23)
- People (all Nov 23): [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/evgeniy-alekseev.md]] · [[wiki/people/sebastian.md]] · [[wiki/people/elizabeth.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/sergey-tsymanov.md]] · [[wiki/people/anton-seregin.md]] · [[wiki/people/ivan.md]] · [[wiki/people/andrei-klimovich.md]] (all in absentia except Pavel and Irina)

## Notes on the sources

- **§12 — new meeting.** Notes and transcript share date, time and title and link each other. A corpus-wide search for both filenames, "Pavel_Irina_LTE", "coffee machine" with Nov 23 and "4377" found no page citing either file. The 1:17 PM Genadi call on the same boards is a different recording.
- **Notes vs transcript.** They agree. The notes' later note that the Genadi call reopened the board ruling is kept on the decision page.
- **§4 name calls.** "Ира" = Irina Shishko (QA / test builds — the speaker label; not Makarych); "Алексеев" = [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] (boards, Wi-Fi-module firmware; registry context — this call names him by surname); "Элизабет" = Elizabeth Palomino; "Себастьян" = Sebastian Cortes; "ваня" = Ivan; "ефим" = [[wiki/people/efim-podvoiski.md|Efim Podvoiski]] (South Dakota maths); "Антон… серёгин" = Anton Seregin; "Алексей хамин" = Alexei Khamin; "цимонов" / "Сымонов" / "Сергей" = Sergey Tsymanov (**inference** from the update work); "Андрей" (install date; the pin fix with Sebastian) = Andrei Klimovich (**inference**; Pavel names "Андреем. Климовичем" just before); "саша" and "Игоря" in the team-mood talk — not matched (mood talk skipped).
- **Garbles kept as heard.** "пол ранут" — **unclear**; "Селфо" — **unclear**; "Гитлер" = GitHub (**inference**); "риск" / "риск модифишн" = RIS / RIS modification (notes); "jobia" / "джорджии" = Georgia; "мандары" — **unclear**; "бюлт" / "белда" = build; "флекс закуам 11 14 34344 снэпшот" = Flex GA-COAM build name, **unclear** beyond that; "интролота" = Intralot; "Инкома" = InComm; "Про лопс. Постролайн тролот" — **unclear**; "джелай" = GLI (notes); "Проверщик" — **unclear**; "DVP 22 подчеркивание один" = MVP 2_1 (**inference**); "2122" = 2_1/2_2 (notes); "ikel" / "i kup" / "Айкэ" = Flex IQ; "ws" = WebSocket protocol (**inference**); "USBC" = USB stick (notes); "эстелинк" = ST-Link; "стм 32" / "с т м 32" = STM32; "Аккумуляторов" = emulators (notes); "гевей" — **unclear**; "22 ревизий порта" = 2 port revisions (**inference**); "репорта" / "бортов" = boards; "ждок" — **unclear**; "акция спойта" = access point; "бэнка" — **unclear**; "лакейшн" = location; "барда" = dashboard (**inference**); "выбиратка" — **unclear**; "Шаманов цимона" — **unclear**, read with Tsymanov; "Ремонт андрейт" = remote update.
- **Skipped as chatter.** Team mood and praise of "Саша" and "Игорь" for using AI with thought; Pavel's view that land-based games need detail an AI alone will not supply; greetings and the close.
- **Not recorded.** Val's one-line remark on Seregin's level as a specialist — a personnel assessment, not recorded.
- **Privacy.** No personal passage. **§15.8:** clear. **§15 #9:** clear.

## Sources

- [[raw/Meeting_Transcript_Pavel_Irina_LTE_Modem_Build_Rev_2_Boards_and_WiFi_Updates-November-23-2026.md]]
- [[raw/Meeting_Notes_Pavel_Irina_LTE_Modem_Build_Rev_2_Boards_and_WiFi_Updates-November-23-2026.md]]
