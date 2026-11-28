---
type: decision
title: Genadi Peari's top priority is to finish the data contracts and load every data sheet into GitHub — starting the same day with the controller boards of the 5 current monitors (part numbers matching MSBC) and the electromechanical counter; his new monitor-controller requirements (built-in LED backlight control and power supply, no extra boards) go into the data contracts; supplier search is to become agent logic built on the data contracts, not hand work, with Andrei to help if he is stuck; the question of how the revision-2 board check was opened in Jira is parked (Val, with Genadi Peari, Nov 23 2026)
date: 2026-11-23
aliases: [Nov 23 Genadi call, Alignement Nov 23, finish the data contracts first, доделать дата контракты, положить все дата шиты, monitor controller kits, controller boards for 5 monitors, Akira monitors, integrated LED backlight control, integrated power supply, electromechanical counters 50 percent, supplier search by agents, manufacturer or trading company, Alibaba sourcing agent, revision 2 boards, revision 3 boards, 20 boards multiplexer, Genadi in automation not procurement]
source-count: 6
status: active
open-commitments: 5
open-questions: 4
---

# Genadi: data contracts and data sheets first; supplier search becomes agent logic (Nov 23 2026)

Taken at the [[wiki/meetings/2026-11-23-genadi-rev-2-boards-monitor-controller-sourcing-and-data-contracts.md|Nov 23 2026, ~1:17 PM call "Alignement"]] (Russian; ~38 minutes) between [[wiki/people/val-levitan.md|Val Levitan]] and [[wiki/people/genadi-peari.md|Genadi Peari]], three days after the [[wiki/decisions/2026-11-20-genadi-works-only-on-the-bom-with-nathan-not-procurement-and-his-purchasing-know-how-goes-into-standards-checked-daily-by-his-own-po-agent.md|Nov-20 ruling]] that Genadi works on the BOM, not procurement [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]].

## 1. The 20 revision-2 boards

- **The question.** Genadi opened with Andrei's question about Val's message asking "Евгению послать 20 бортов, чтобы он починил" [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]]. "Евгений" here is read as [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]], the board contractor (**inference** by §4 context — hardware boards, a contractor, Wi-Fi support work).
- **New boards already coming.** Genadi: 20 boards of the new revision are ordered, and "В пятницу, то есть уже на в конце недели из Китая должны выслать нам эти 20 штук". Val: "мы называем её как бы ревизия 3"; Genadi: the main interface board "на IQ". Price: "В районе где то 16 $17", plus "Ещё получается 50%"; Val: "То есть $25 борт. 20 бортов это $500" [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]]. The notes read the 50% as duty and say "ordered Friday"; on tape Friday is the shipping day [[raw/Meeting_Notes_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]].
- **Genadi's doubt.** "Послать туда обратно будет не дешевле нам"; the contractor already has two boards of this revision (Genadi had them put in an earlier shipment) and was asked to check whether they can be fixed — no answer yet, "не факт, что он их сможет починить"; he was busy at the weekend on Wi-Fi support and an adapter check. Val: repaired boards "просто будет сток" [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]].
- **Val on responsibility.** The contractor "сам контрактор… он не работает у меня на perel"; "он просто поставил туда мультиплексер", and the fix he suggested — "откусить там этот мультиплексер. И запаять 2 ножки вместе" — "Это проверили, это не работает." If he cannot fix it, "пусть тогда он снимет свой чарч" [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]]. No amount was named.
- **Not settled.** The call did not say whether the 20 boards still go back [[raw/Meeting_Notes_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]].

## 2. How the check was opened in Jira — parked

Genadi: "Все Джерри всё Джерри есть абсолютно всё". He opened a story for the check — "Это стори. На проверку" — under the initiative the notes name "Flex IQ transition to production", assigned it and set it To Do; the contractor has not opened it. Val: "Это неправильно", but he could not focus now: "у нас на это есть стандарт, как открывается task? Если вы туда своего клод направите, то он правильно откроет"; "Окей, я пока заборку это дело" [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]] [[raw/Meeting_Notes_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]]. Standards context: [[wiki/decisions/2026-09-04-point-claude-at-the-standards-repository-first.md]].

## 3. Monitor controllers and counters — what Genadi is sourcing

- **Controller kits.** He is replacing the controllers "для всех наших мониторов, которые мы все покупали у акиры" — "примерно гдето 5 мониторов актив, на них есть разные киты". For the 43-inch a sample is ordered and the saving is big ("Сейвень большой") [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]]. "Akira" is the supplier name as transcribed; a Jan-2025 retrofit meeting named a former monitor supplier "Angus/Akira" ([[wiki/projects/used-machine-retrofit-and-inventory-clearout.md]]) — the same firm is **not confirmed**.
- **How he sources today.** "В основном 90%" on Alibaba, rarely the "maidinчая" site (Made-in-China, notes); keyword search, then by hand: "чтоб это было не трейдинг компани чтоб это был манифеер"; he chats with them "вечером ночью", asks "Где вы делаете innause?… кто производит контроллеры или вы их покупаете"; then moves the talk to Outlook "чтобы было всё задокументировано" and brings in procurement. He has a short list of potential suppliers — on tape "300 плейера", the notes read "likely 3"; **unclear** [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]] [[raw/Meeting_Notes_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]].
- **What the new controller must have.** Chinese offers add "power bord потом какието дополнительные провода", which means new brackets and cables. Genadi: "я только сейчас понял, что мы хотим" — an integrated LED backlight control ("интегрейт ledy back lide control") and an integrated power supply for big monitors, "мы не хотим дополнительных партий". Val: "то, что вы говорите, это в принципе дата контракты" [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]].
- **Counters.** The electromechanical counters in the machines: "им сказали, что цена повышается на 50%"; he will look for another source [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]].

## 4. The ruling — data contracts first, then agents

- **Data sheets today.** Val: the controller boards of the 5 monitors go into GitHub "Чтобы ихние парк номера. Совпадали с теми парномерами, которые сейчас записаны в м с би си"; Genadi: "Полчаса"; Val: "Я буду считать, что сегодня будет сделано." The counter's data sheet too: "Вы можете положить детащит сегодня?" — "Да" [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]].
- **Supplier search as agent logic.** Val: "на это можно сделать всю логику. Вот построить логику через агентов", if there is a starting set of data contracts; an agent could suggest what to add to a contract, ask the questions that tell a manufacturer from a reseller, and talk to suppliers through Alibaba — Alibaba has "свой есть билд своего эйя агента" and "Свой свой собственный месседжинг". Genadi: "Это может работать"; he already writes rules for his Claude and "он их запоминает и делает" [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]].
- **The later steps.** Genadi: order a sample ("мы блайндли не хотим это верить"), change the bracket and mounting, talk to SolidWorks "MCP", maybe change the video cables from DVI to HDMI. Val: with a new data contract from the supplier, the agent should mark the old harness obsolete and the new harness keeps the same routing; for the metal, "он должен. Сказать солидворкс, что нужно сделать" ("может я сейчас сильно мечтаю") [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]] [[raw/Meeting_Notes_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]].
- **Help.** Val: "Андрей, если у вас чтото вы застряли, Андрей вам может помочь в этом. И сделать для вас всю эту переписку автоматически" [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]]. Which Andrei is not said.
- **Why.** Val: "мне надо всё делать на 10 голов быстрее"; "если я вас завяжу в прокюрменд, это будет смерть… В автоматике вас завязать." A new controller board or counter alone is "очень маржинал"; the big benefit comes "тогда, когда заработать эту систему". Priority: "сделайте себе приоритет. Чтобы закончить это контракт? И положить все тетящится." Genadi: "без этого нельзя. Весь все эти тулсы дальше" [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]].
- **Genadi's motive.** "когда вижу, что мы вдруг платим там какието $1000 непонятно за что, это же неправильно"; Val: he is the only one in the company with that quality [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]].

## Note — the ~11:46 AM call the same day had ruled the opposite way

About 90 minutes before this call, at the [[wiki/meetings/2026-11-23-pavel-irina-lte-modem-build-rev-2-boards-and-wifi-updates.md|Nov-23 ~11:46 AM call]] with Pavel and Irina (Russian), Val ruled: "Эти 20 плат нужно отправить обратно", packed and sent now with no more experiments ("Не надо не, не надо делать эксперимент"); revision 3 then was counted as 10–15 days "когда он закажет" [[raw/Meeting_Transcript_Pavel_Irina_LTE_Modem_Build_Rev_2_Boards_and_WiFi_Updates-November-23-2026.md]]. This call questioned that ruling without settling it (above) — [[wiki/decisions/2026-11-23-the-20-revision-2-boards-go-back-to-alekseev-for-repair-build-4377-with-the-modem-is-field-tested-on-different-modems-before-the-lab-and-remote-updates-and-wi-fi-setup-are-the-two-must-haves.md]].

## How it sits against earlier rulings

- [[wiki/decisions/2026-11-20-genadi-works-only-on-the-bom-with-nathan-not-procurement-and-his-purchasing-know-how-goes-into-standards-checked-daily-by-his-own-po-agent.md|Nov 20]] — same line: no hand procurement for Genadi; data sheets into GitHub. New on Nov 23: the data contracts are named the top priority, and supplier search itself is to become agent logic. Genadi was still doing sourcing by hand. **Evolution.**
- [[wiki/decisions/2026-11-18-the-next-bom-spike-is-a-self-learning-supplier-loop-the-agent-finds-the-supplier-asks-for-the-missing-data-updates-the-data-contracts-and-reassembles-with-no-human-answers.md|Nov 18]] — the agent that finds the supplier and asks for missing data; Nov 23 adds Genadi's manufacturer-vs-reseller test and Alibaba's own messaging as the channel.

## Open commitments

- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — put the data sheets of the controller boards for all 5 current monitors in GitHub, part numbers matching MSBC — due Mon Nov 23 2026 ("сегодня будет сделано") — [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]]
- [ ] Genadi Peari — put the electromechanical counter's data sheet in GitHub, to look for another source — due Mon Nov 23 2026 — [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]]
- [ ] Genadi Peari — add the new controller requirements (integrated backlight control, integrated power supply, no extra boards) to the data contracts — due unspecified — [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]]
- [ ] Genadi Peari — finish the data contracts and load all data sheets, as his top priority — due unspecified — [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]] [[raw/Meeting_Notes_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]]
- [ ] Genadi Peari — build the supplier-search logic with agents; ask Andrei if stuck — due unspecified — [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]]

## Open questions

- Are the 20 revision-2 boards still sent back for repair, now that 20 new-revision boards ship this week? — [[raw/Meeting_Notes_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]]
- Can the revision-2 board be fixed at all? The contractor has not answered — [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]]
- Does the contractor drop his charge if he cannot fix the boards? — [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]]
- How should this kind of check be opened in Jira (story vs the task standard)? Parked by Val — [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]]

**§15.8:** clear — the board prices are part costs, and no amount of the contractor's charge was named. **§15 #9:** clear.

## Note, Nov 25 2026 — the data sheets also feed MSBC item attributes

Two days later, at the Nov-25 MSBC attributes meeting, Val said the attributes of each item in Business Central should come from its data sheet, "потому что атрибют и это часть дельта контракта", and that a hand-kept table of Flex configurations should give way to the data contracts and requirements [[raw/Meeting_Transcript_MSBC_Item_Attributes_vs_Description_and_Part_Revisions-November-25-2026.md]]. Record: [[wiki/decisions/2026-11-25-the-item-description-holds-only-the-product-name-configuration-moves-into-msbc-item-attributes-lev-tests-them-first-in-a-test-company-and-there-is-no-configuration-table.md]].

## Note, Nov 26 2026 — the monitor-controller change: about $95 a machine on paper

Three days later, at the [[wiki/meetings/2026-11-26-genadi-components-repo-structure-and-monitor-sourcing-savings.md|Nov-26 2:31 PM call]], Genadi said prices from Korea for the monitor driver boards had risen sharply, and "на бумаге у меня уже сейчас сейвинг 95 долларов на машину"; a 22-inch sample was sent and two 43-inch samples at about $25 each are on the way; he is checking brackets and wires on every monitor and needs "few days" for the transition and production instruction [[raw/Meeting_Transcript_Genadi_Components_Repo_Structure_and_Monitor_Sourcing_Savings-November-26-2026.md]] [[raw/Meeting_Notes_Genadi_Components_Repo_Structure_and_Monitor_Sourcing_Savings-November-26-2026.md]]. Whether the Korean source is the "Akira" named on Nov 23 is **not confirmed**. The Nov-23 commitments above are not reported as done. Record: [[wiki/decisions/2026-11-26-a-bom-has-two-sources-of-truth-the-product-description-and-the-github-data-contracts-mery-orders-from-msbc-revision-1-now-and-genadi-finishes-the-data-contracts-for-revision-2.md]].

## Sources
- [[raw/Meeting_Transcript_MSBC_Item_Attributes_vs_Description_and_Part_Revisions-November-25-2026.md]]

- [[raw/Meeting_Transcript_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]]
- [[raw/Meeting_Notes_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026.md]]
- [[raw/Meeting_Transcript_Pavel_Irina_LTE_Modem_Build_Rev_2_Boards_and_WiFi_Updates-November-23-2026.md]]
- [[raw/Meeting_Transcript_Genadi_Components_Repo_Structure_and_Monitor_Sourcing_Savings-November-26-2026.md]]
- [[raw/Meeting_Notes_Genadi_Components_Repo_Structure_and_Monitor_Sourcing_Savings-November-26-2026.md]]
