---
type: person
title: Sergey Tsymanov
date: 2026-07-14
aliases: [Sergey Tsymanov, Siarhei Tsymanau, Sergey Tsimanov, Tsymanau, Tsimanov, Sergei Tsyganov, Tsyganov, Цыганов, Sergei, Sergey]
source-count: 40
open-commitments: 15
disambiguation: "Minsk engineer who drafts CMS requirements with the backend 'Dima' (Chudinov). OWNER-CONFIRMED 2026-07-14 = the payroll 'Siarhei Tsymanau' (Belarusian) and the IT-records 'Sergey Tsimanov' — same person; Tsymanov canonical, Tsymanau/Tsimanov aliases. Distinct from other 'Sergei/Sergey' names (e.g. Sergei Novitsky the advanced-setup technician; Sergey Vysotsky the outside digital-growth specialist, wiki/people/sergey-vysotsky.md); resolve by context."
open-questions: 1
---

# Sergey Tsymanov

Sergey Tsymanov is a JVL **Minsk engineer** who works on the **legacy CMS requirements** effort alongside the backend "Dima" (context-resolved as [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]]). On the Mar 23 2025 CMS-persona call, Val asked Sergey Tsymanov and Dima to read his AI-written description of the current CMS and confirm whether it was accurately described. [[raw/cms_persona_requirements-march-23-2025.md]]

**Owner-confirmed (2026-07-14):** the same person as the Minsk-payroll "**Siarhei Tsymanau**" (Belarusian) and the IT-records "**Sergey Tsimanov**" — all three spellings acceptable, **Sergey Tsymanov** canonical. See [[wiki/topics/minsk-staff-roster.md]]. [[raw/minsk_staff_roster_2025_names-only.md]]

- He and Dima are the pair who drafted the first set of persona-based **functional/non-functional requirements** (for the personas Pavel and Juan) that Val and [[wiki/people/aaron.md|Aaron]] critiqued as too product-specific. See [[wiki/topics/persona-driven-design-and-orchestration-platform.md]]. [[raw/cms_persona_requirements-march-23-2025.md]]
- Val described Sergey and Dima's requirements work as a **training exercise** — he is deliberately having them practise requirements→features on the decades-old legacy CMS before tackling the new orchestration platform. [[raw/cms_persona_requirements-march-23-2025.md]]

(Name transcribed "Sergey Tsymanov" / "Сергей Цыманов"; spelling flagged — see Owner Decisions.)

## CMS requirements-review follow-up (~Mar 25 2025, date inferred)

- On the follow-up session ([[wiki/meetings/2025-03-25-cms-requirements-review-workflow.md]]) he is the second of the two people the legacy CMS rests on — Val: it all "держится на честном слове" between Dima and Sergey ("Мне просто повезло, что вы порядочные люди. Но так компания не строится"). He and Dima committed to re-review the AI-generated overview/use cases/requirements ("мы уже просмотрели много несоответствий"), collect the maximum of actually-used capabilities, and add the missing **таксоны** (taxonomies) by the booked Thursday meeting. See [[wiki/topics/persona-driven-design-and-orchestration-platform.md]]. [[raw/cms_requirements_development-dzima-sergei-andrei.md]]

## Open commitments

- [ ] Sergey Tsymanov (with Dima Chudinov) — re-review the generated CMS materials and add the missing taxonomies — due by the booked Thursday meeting (~Mar 27, inferred) — [[raw/cms_requirements_development-dzima-sergei-andrei.md]]
- [ ] Sergey Tsymanov — implement LGS 474 (LED Light Control) on Omni, in parallel, starting Monday (~June 16) — due before ~July 31 — [[raw/schedule_review_omni-june-12-2025.md]]
- [ ] Sergey Tsymanov — produce the **terminal-registration state-machine diagram** for the payment-hub ACH module — due Wed Nov 19 2025 — [[raw/Payment HUB_ACH module specification_10.11.25.md]]
- [ ] Sergey Tsymanov (with [[wiki/people/dmitri-chudinov.md|Dima Chudinov]]) — produce the **production-side migration estimate** for moving the CMS/CASS codebase to cloud (straight-line lift-and-shift, no optimization) — due next Monday (~Mar 30 2026) — [[raw/Meeting_Transcript_data_access_strategy_and_cms_cloud_migration-March-23-2026.md]]

## History

- **SQL/OLAP architecture (~2024, likely Q4):** attended both sessions. In part 1 he joins mid-call (the Miro edit-rights aside) and the local-AD example user is "Сергей Цимонов"; a speaker also names "программисты Сергея и Дима" as the ones who modify the application databases. In part 2 Val introduces "Dima and Sergei are designing back office solutions, back office architecture" — the same pairing that later produced the 2025 CMS-requirements work. See [[wiki/topics/olap-power-bi-architecture.md]]. [[raw/architecture_sql_olap_visualization_1_2025-03-29.md]] [[raw/architecture_sql_olap_visualization_2_2025-03-29.md]]

## CMS sessions (Apr 14–15)

- Present in both CMS migration sessions ([[wiki/meetings/2025-04-14-cms-svn-github-product-repos.md]], [[wiki/meetings/2025-04-15-cms-migration-staged-decision.md]]). Current work named: "Сергей сейчас занимается рестрикшенами для геймсетов, чтобы не было падений на машинах" (game-set restrictions against machine crashes). He has the team's GitHub Actions experience — "GitHub Action мы уже тренировались, Сергей проводил работу," including the earlier **протосервер (Protohost)** repo transfer with build/release working; he co-owns the transfer-sizing homework with Chudinov. [[raw/cms_github_svn-apr-15-2025.md]] [[raw/cms_svn_github-april-14-2025.md]]

## June 12 2025 — takes LED Light Control (LGS 474) on Omni

On the [[wiki/meetings/2025-06-12-omni-schedule-review.md|June-12 Omni schedule review]], to relieve the LGS/backend bottleneck (Kharetsky), **LGS 474 (LED Light Control) was reassigned to Sergey Tsymanov** ("Цыманов", who sits next to Sasha), starting **Monday**, running in parallel — Val accepted a slightly slower pace on other work for a faster overall result. He was also floated for the isolated money-transfer/LED framework tasks. See [[wiki/topics/omni-core-advancement-and-game-templating.md]]. [[raw/schedule_review_omni-june-12-2025.md]]

## Nov 10 2025 — assigned the terminal-registration state diagram

On the [[wiki/meetings/2025-11-10-payment-hub-ach-spec-review-undertakings-plaid-qa.md|Nov-10 ACH-spec-review session]] Sergey (present across the Nov 5/6/10 arc, largely a silent participant) was assigned to draw the **terminal-registration state-machine diagram** for the payment-hub ACH module, due Wed Nov 19. See [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Nov-10). [[raw/Payment HUB_ACH module specification_10.11.25.md]]

## Mar 23 2026 — data-access strategy call

On the data-access-strategy / CMS-cloud-migration call ([[wiki/meetings/2026-03-23-data-access-strategy-cms-cloud-migration.md]], 1:34pm, Russian, transcribed "Sergey Tsimanov"; with [[wiki/people/val-levitan.md|Val]], [[wiki/people/dmitri-chudinov.md|Chudinov]], [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]], [[wiki/people/andrey-bosik.md|Andrei Bosik]]) Sergey supplied the historical context that the Excel-to-cube approach was built **~2017** with hard-coded credentials for internal-network use, pressed for clarity on how Excel actually pulls from the cube, floated whether the cube itself has **per-user visibility/dimension-security** settings (unsure — to check), and asked whether the team should reconsider the OLAP-cube architecture at all. Assigned (with [[wiki/people/dmitri-chudinov.md|Chudinov]]) the **production-side migration estimate**. Substance on [[wiki/topics/olap-power-bi-architecture.md]] (Mar-23). [[raw/Meeting_Transcript_data_access_strategy_and_cms_cloud_migration-March-23-2026.md]]

## Apr 15 2026 — legacy CMS docs check: the `protoserver` metric-mismatch

On the [[wiki/meetings/2026-04-15-legacy-cms-documentation-progress-check.md|Apr-15 legacy-CMS docs check]] (transcript "Sergey Tsimanov") Sergey explained that the `protoserver` repo scores low on docstring coverage (~37%) not from poor work but because it is largely **auto-generated by plugins** — there's little code for Claude to document — so the metric mismatches that repo's structure rather than measuring quality. Substance on [[wiki/topics/docs-as-code-and-atlassian-exit.md]] (Apr-15). [[raw/Meeting_Notes_Legacy_CMS_Documentation_Progress_Check-April-15-2026.md]]

## Aug 24 2026 — lined up for the backend/CMS prose, and to verify the prose Val gave Dima

On the [[wiki/meetings/2026-08-24-nova-lgs-prose-standard-checkpoint.md|Aug-24 prose checkpoint]] (Russian; Sergey **not present**) [[wiki/people/pavel.md|Pavel Frolov]] proposed giving him work now that he is **back from vacation**: "сейчас Сергей циманов вышел из отпуска и можно будет ему давать… поможем сейчас Сергею цыманову дать работу, чтобы он сделал прозу именно для бэкэнда… CMS." [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]

- **Two things were proposed for him:** write prose and capabilities for the **backend / CMS**, and **verify that the prose Val handed to [[wiki/people/dmitri-chudinov.md|Dima Chudinov]] matches the current code** — Pavel: "нам надо подтвердить, что проза которую там есть сейчас судимые, что она соответствует действительности." [[wiki/people/irina-shishko.md|Irina Shishko]] made the call: "Ну её тогда отдать Сергею. Потому что дима сейчас занят, потом дима в отпуск, а Сергей пускай сейчас этим занимается." Owners of the assignment are Pavel and Irina. [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- **He is already a holder of Val's prose.** Val: "все прозы, которые я сделал и всякий побился, я отправил диме чудина у и Сергею циманову" — he sent everything he produced to Dima Chudinov and Sergey. See [[wiki/topics/nova-platform-architecture.md]] (Aug-24). [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- Context on the standard he would be writing to: [[wiki/decisions/2026-08-24-single-prose-writing-standard.md]]. [[raw/Meeting_Notes_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]

## Open commitments (Aug 24 2026)

- [ ] Write prose and capabilities for the backend/CMS, and verify that the prose Val gave Dima Chudinov matches the current code (assignment owned by Pavel Frolov and Irina Shishko; Sergey was not on the call) — due unspecified — [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]

## Sept 11 2026 — named for the FlexPay server side, and added to the capability project

At the [[wiki/meetings/2026-09-11-transactional-mvp1-scope-and-priorities.md|Sept-11 8:04 AM call]] [[wiki/people/pavel.md|Pavel Frolov]] named Tsymanov as the server-side half of FlexPay — "со стороны сервера [до]бавляет поддержку Сергей [Цы]манов" — opposite [[wiki/people/alexander-biratka.md|Alexander Biratka]] on the kiosk side. Later in the same call Pavel asked for him to be added to the capability project alongside [[wiki/people/alexei-khamin.md|Alexei Khamin]], and [[wiki/people/andrey-bosik.md|Bosik]] had it done during the meeting [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

**FlexPay is no longer MVP 1**, so this work runs in parallel to the October-1 line rather than on it — see [[wiki/decisions/2026-09-11-mvp1-goes-with-flex-iq-alone-and-one-kiosk-per-location.md]].

## Sept 22 2026 (4:48 AM stand-up) — modem metrics, and the CMS release handed to him

At the [[wiki/meetings/2026-09-22-daily-standup-capability-test-status-and-flexport-gui.md|Sept-22 stand-up]] (Russian; label "Sergey Tsimanov") [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]:

- **Done:** the export block, and a fix for a connection failure ("проблема с тем, что не подключалась") [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].
- **Now:** forwarding and collecting modem-connection metrics. He questioned the Grafana route and asked to add a Wi-Fi signal-to-noise parameter in the platform SDK repository. See [[wiki/decisions/2026-09-17-signal-quality-in-mvp1-means-remote-visibility-not-a-screen.md]] (Sept-22 update) [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].
- **"Where does MVP even come from?"** — "по моему тут не в VP тут уже всё вот готовый продукт". No one answered. All the tasks he has taken are MVP 1 [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].

## Open commitments (Sept 22 2026)

- [ ] Sergey Tsymanov — release the components changed for the CMS server; Ivan asked the day before and it was still not out — due Sept 22 2026 ("прям кровь из носу надо") — [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]


## Sept 23 2026 — his local Flex-Port emulation, and "why not one repository?"

At the [[wiki/meetings/2026-09-23-daily-standup-terminal-emulator-and-capability-split.md|Sept-23 Minsk stand-up]] (Russian; label "Sergey Tsimanov") [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]:

- **Metrics.** He is on metrics and wants to tidy the overlays ("почистить… оверлейна всякие").
- **A local Flex-Port emulation** from an earlier task — "он у меня локально" — which Anton may reuse. See [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] (Sept-23 update).
- **Capability 118.** He said his items there were done for Flex IQ, not FlexPay, and asked why the two alike products are not one repository built two ways. See [[wiki/decisions/2026-09-23-capability-118-is-split-by-product-and-two-devices-keep-two-repositories.md]].

## Sept 24 2026 — connection metrics done, and the Flex IQ wallet task

At the [[wiki/meetings/2026-09-24-daily-standup-firmware-delivery-and-capability-statuses.md|Sept-24 Minsk stand-up]] (Russian; label "Sergey Tsimanov") [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]], he finished the connection-state metrics and checked them on a new build. He took the Flex IQ task for creating a wallet and putting money into it; the requirements hold "куча противоречий", so he is preparing questions for Andrei. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 24).

## Open commitments (Sept 24 2026)

- [ ] Sergey Tsymanov — prepare the questions on the contradictory Flex IQ wallet requirements for Andrei (Klimovich, by context) — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]

## Sept 28 2026 — wallet creation, and a Grafana task that may be done

- **At the 4:56 AM stand-up** ([[wiki/meetings/2026-09-28-daily-standup-log-traffic-and-nova-rename.md|Sept-28 Minsk stand-up]], Russian; label "Sergey Tsimanov"): he finished wallet creation on Flex IQ and took the next task, wallet creation through the Flex-Port (name garbled; **inference** from the 8:02 AM call). A Grafana dashboard task (type TPT-INT, in the integration repository) may already be done: he thinks he updated the dashboards when he added the link-quality metrics. See [[wiki/decisions/2026-09-17-signal-quality-in-mvp1-means-remote-visibility-not-a-screen.md]] (Sept-28 update) [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]].
- **At the 8:02 AM call** ([[wiki/meetings/2026-09-28-transactional-mvp1-remote-updates-and-october-15-target.md|Sept-28 8:02 AM MVP 1 call]]; in absentia): Chudinov said "Сергей занимается по поводу создания voletnoflex портье" (read as wallet creation on the Flex-Port — **inference**) [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]].

## Open commitments (Sept 28 2026)

- [ ] Sergey Tsymanov — check whether the Grafana dashboard task is done; if so, comment and close it — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]]

## Sept 29 2026 — capability 156 implemented, no USB to flash the board, and zero balance (158) next

At the [[wiki/meetings/2026-09-29-daily-standup-firmware-reissue-and-modem-gateway.md|Sept-29 Minsk stand-up]] (Russian; label "Sergey Tsimanov") [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]:

- **156.** "Я заканчиваю с каппобилити 156 это по… [с]оздание [волета] это через [Флекс-Порт]" — wallet creation through the Flex-Port; "реализация закончена, сейчас тестирую на стенде". He cannot flash through the programmer ("fixot" — garbled) because the board it is attached to ("таммар 64" — **unclear**) has no USB; there are workarounds he is investigating, "если не получится, то понесу к тебе обратно" (to Pavel).
- **158.** Next, capability 158 — "[з]еро баланс": he and "Дима" (Chudinov, by context) looked quickly and "[п]оловина из них точно реализована уже"; he must work out which, and has already reassigned the tasks to himself (Pavel's view was out of date).
- Plan: finish 156 that day and move to 158. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 29, 4:49 AM). His Sept-28 Grafana commitment above is not mentioned.

## Open commitments (Sept 29 2026)

- [x] Sergey Tsymanov — finish capability 156 (wallet through the Flex-Port), find a way to flash the board or bring it back to Pavel, then start capability 158 (zero balance) — due Sept 29 2026 (156) / unspecified — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]] — **discharged Sept 30 2026:** "Закончил задачу созданием [волета] через [Флекс-Порт]" and he is on 158; the board flashing was not mentioned — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]

## Sept 30 2026 — the wallet through the Flex-Port is done; 158 has four tasks and some will be dropped

At the [[wiki/meetings/2026-09-30-daily-standup-flexport-firmware-delivery-and-network-loss.md|Sept-30 Minsk stand-up]] (Russian; label "Sergey Tsimanov"): "Закончил задачу созданием [волета] через [Флекс-Порт]" (156, by his Sept-29 report — **inference**). On 158: "там есть куча задач ну 4 задачи"; "какойто надо выкинуть допустим [pay mament hop 5]" (garbled) "потому что у нас [волеты] будут храниться пока. На терминале"; "много вещей, которые реализованы… выискивают, что надо дореализовать"; "планирую закрыть сегодня следующую взять". See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 30, 4:57 AM). His Sept-28 Grafana commitment is again not mentioned [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]].

## Open commitments (Sept 30 2026)

- [ ] Sergey Tsymanov — close one capability-158 (zero balance) task and take the next; drop the ones that no longer apply while wallets stay on the terminal — due Sept 30 2026 — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]] — *Oct 1 2026: "Закончил там с капбилити там остатки, которые были по экранам… [взял] другую [capability]" — no number given; not read as 158* — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]

## Oct 1 2026 — the support phone on the e-wallet ticket, a new ticket template, the printer-library API, "pass it through, right?", and the email about FP-85

At the [[wiki/meetings/2026-10-01-daily-standup-sas-mode-flag-and-feature-status-rules.md|Oct-1 Minsk stand-up]] (Russian; label "Sergey Tsimanov") [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]:

- **Status.** "Закончил там с капбилити там остатки, которые. Были по экранам… в порту там что тесты там добавить надо было. Я [взял] другую [capability]".
- **The printer library.** On Biratka's broken e-wallet-ticket printing: "в той библиотеке я ничего не делал, вообще ничего не делал"; what was added was "[API] для для нашего демона, который который мы создаём по созданию по принту чека. Для [e-wallet] никто ничего ничего не делал"; "Смотря какую ты версию тянешь"; "я делаю темплейт нового [e-wallet ticket]" — a new template, to be tested on all printers. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 1, 4:48 AM).
- **The support phone.** The new e-wallet ticket has a support-phone field; at location set-up step one there are two fields — phone number and contact phone number — "это один из них или надо добавлять ещё одно поле [support contact number]". "Я с Андреем вчера разговаривал" (Klimovich, by context): "Андрей сказал, этот это номер телефона, который будет указывать [—], чтоб связывался с лакейшином". He shared his screen ("у нас есть лакейшн дитейл… 2 номера"). Chudinov: it is JVL's support, not the location's. Pavel: "это контакт" — "Короче его пробрасывать, верно?" — "Да."
- **The SAS flag.** He took "пробрасывать" to mean the server — "Для меня это было сервер" — and was corrected: the toggle is per port on the Flex IQ set-up; "окей, хорошо". He or Chudinov carries it in the PIN-code task. See [[wiki/decisions/2026-10-01-sas-or-no-sas-is-set-per-flex-port-on-the-flex-iq-set-up-screen-and-sent-at-registration-with-the-pin-code.md]].
- **The email.** "мне пришло письмо на мыло… что у меня [парент] то уже закрыты, а эти нереализованные… на [FP-85]… Владимир создал. Это story, я думал мы всё работаем в рамках фичи… [story] была создана после Того, как я закрыл вот эту задачу". Later: "а что описывать, если проблема в виде стори?" — Irina: no bug while developing, so a story; "Это не они решат это [Клод]… решают. Я так понимаю" on which feature a problem falls under. See [[wiki/decisions/2026-10-01-completed-is-the-developers-last-step-and-a-found-problem-sends-the-feature-from-completed-back-to-to-do-as-a-story.md]].

## Open commitments (Oct 1 2026)

- [ ] Sergey Tsymanov — forward the location's contact phone from location set-up to the e-wallet ticket as its support number — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
- [ ] Sergey Tsymanov — finish the new e-wallet-ticket template in the printer library, to be tested on all printers — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]] — *Oct 2 2026: "закончил вчера с тикетом новым на на печать" — the new print ticket is done (the e-wallet template by context — inference); testing on all printers not mentioned* — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]

## Oct 2 2026 — the new print ticket done, three of Vladimir's stories fixed, the reopened feature's stale date, Val's note about a GitHub branch, prose, and the weekend

At the [[wiki/meetings/2026-10-02-daily-standup-sas-log-collection-policy-and-new-arm-boards.md|Oct-2 Minsk stand-up]] (Russian; label "Sergey Tsimanov") [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]:

- **The red tasks.** Pavel: "вот эти вот красные таски, которые просроченные… с 15 сентября 29 сентября 1 октября." Tsymanov: "это не просроченное это закрыть надо. Я просто брал вчера задачу. На неё Владимир создал [story]. Вот и я их фиксел. Получается мне переоткрыли эту фичу… но дату не поменяли." Pavel: "Давай поменяем." Vladimir: "я их не назначал на исполнителя, ты их сам себе забрал" — "Да." Irina's rule: whoever takes a feature into work updates its schedule with Pavel or her. See [[wiki/decisions/2026-10-01-completed-is-the-developers-last-step-and-a-found-problem-sends-the-feature-from-completed-back-to-to-do-as-a-story.md]] (Oct-2 update).
- **Status.** "закончил вчера с тикетом новым на на печать. Потом пофиксовал проблемы 3 человек вечером подходил… Позволял там кэша делать, если… На самом деле локация заблокирована, допустим. Вот там было 3 истории от Владимира… по ним и фикс делал. Ну и прозы параллельно вёл. Сейчас вот прозы заканчиваю." Chudinov: the transactional repositories are split between the two of them ("Разделили с Сергеем… на пополам"). See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 2, 4:50 AM) and [[wiki/decisions/2026-09-04-point-claude-at-the-standards-repository-first.md]] (Oct-2 update).
- **Val's note.** "[Вал] пишет, что у меня есть какие то фича в гетхабе, а это не соответствует. Связанным… Ты где фичь? У нас должны быть [Jira] или в гетхабе"; "ему не не нравится, что клод, когда создал бранч, скорее всего… к фичи приотачивал этот бранч. А ими не соответствует какимто этого бранча" — not settled; Pavel: watch Claude. See [[wiki/topics/ai-assisted-development.md]] (Oct 2).
- **Weekend.** "Да планирую" (to work). His Oct-1 support-phone commitment above was not mentioned.

## Open commitments (Oct 2 2026)

- [ ] Sergey Tsymanov — update the dates on the feature reopened by Vladimir's stories — due Oct 2 2026 — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]

## Oct 5 2026 — "ещё один стенд… типа как наш [дев стейджинг]", reprint at card issue, and the Flex IQ tests in five minutes

At the [[wiki/meetings/2026-10-05-daily-standup-autotest-stand-debate-and-jira-reopen-rules.md|Oct-5 Minsk stand-up]] (Russian; label "Sergey Tsimanov") [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]:

- **The stand.** "Или ещё один стенд?"; could test cards be generated — "у него есть какойто реестр этих карточек там нельзя сгенерировать какието по принципу свой… даже для песочницы" (Chudinov: no); "Еще один стенд, какойто нужен для тестов. Наверное, вот типа как наш [дев стейджинг] только"; a fixed version stack "который нельзя менять… Только под определенные тесты… Это будет само проще просто Андрею отдать… там слишком много зависимостей"; an InComm emulator "с какимито определёнными сценариями там зависания"; and "стенд, на котором они будут запускаться, должен быть максимально приближен к продуктовому… не так, что на машине… на моей над [диминой]." Ruling: [[wiki/decisions/2026-10-05-the-payment-hub-autotest-stand-is-not-mvp1-and-a-separate-meeting-with-andrei-designs-it.md]].
- **Status.** "по каким [капабилити] на выходных не скажу, точно сделал. Сейчас занимаюсь репринтом для при выпуске карточки. И тут задача тоже ещё вот. Владимира. [—] занимается" (garbled); "уменьшил тесты время тестов за. [Flex IQ]. 5 минут выполнять" — Pavel: "Зачем?" Chudinov: the transactional repositories are split with him (Oct 2); Pavel will take him into the Port-tasks triage. Irina: "Сергей можешь подойти ко мне по[сле] митингу?" — "Да." See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] and [[wiki/topics/test-automation-strategy.md]] (Oct 5). His Oct-1 and Oct-2 commitments above were not mentioned.

**§15.8:** clear. **§15 #9:** none.

## Oct 6 2026 — Flex IQ alerts, and a terminal that ran out of memory after an update

At the [[wiki/meetings/2026-10-06-daily-standup-ris-georgia-branch-and-critical-error-text.md|Oct-6 Minsk stand-up]] (Russian; speaker label) [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]:

- He took feature 55: alerts on the Flex IQ screens.
- After an update that day a terminal ran out of memory and came up badly. Cause: log sizes are set differently per log type and can reach "почти до 2 гигабайт", while the partition used for updates is "по моему 3 и 9 гигабайт". It can happen again. He will write a feature; who does it, he or "дима", is not decided.
- Irina asked him to link FIX-135 to the right feature.

### Open commitments (Oct 6 2026)

- [ ] Sergey Tsymanov — write the feature for the log-size / update-partition memory problem, and link FIX-135 — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]

### Open questions (Oct 6 2026)

- Who carries out the memory-problem feature — Tsymanov or "дима"? — [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]

## Oct 7 2026 — a capability for the Flex memory problems; printer statuses today

At the [[wiki/meetings/2026-10-07-daily-standup-test-coverage-first-and-ai-task-numbers.md|Oct-7 Minsk stand-up]] (Russian; label "Sergey Tsimanov") [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]: "разбирался с проблемами по памяти на флик, там создал каппобилити пару фич под них" — a capability and a couple of features for the memory problems on Flex. Today he finishes the printer statuses, then "перейду наверное к этому, который вчера создал" — the new work he created. This answers the Oct-6 "write the feature" item and, by his own words, suggests he takes the work himself (**inference**). See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 7).

### Open commitments (Oct 7 2026)

- [ ] Sergey Tsymanov — finish the printer statuses, then the Flex memory features — due Oct 7 2026 for the printer statuses — [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]

## Oct 8 2026 — printer statuses, log memory after the incident, and FIQ-140

At the [[wiki/meetings/2026-10-08-daily-standup-lease-expiry-scenarios-and-flex-signal-quality.md|Oct-8 Minsk stand-up]] (Russian; label "Sergey Tsimanov") [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]: the printer-status task (ticket printing through the port, with a record if it cannot print); log-memory optimisation after the incident "Позавчера"; now the Flex memory leak, FIQ-140 — [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 8).

### Open commitments (Oct 8 2026)

- [ ] Sergey Tsymanov — fix the Flex memory leak (FIQ-140) — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]

## Oct 9 2026 — memory work done; fatal errors go out of service with a clear message; the urgent lease-code task; how to spot a test machine

At the [[wiki/meetings/2026-10-09-daily-standup-weekend-service-rollout-and-stats-blocking.md|Oct-9 stand-up]]: memory optimisation finished, with a separate process reporting remaining memory; last task: fatal cases show a clear critical error with a description in the statistics and go out of service — [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 9, 4:46 AM). Pavel gave him the lease-code task as urgent for the middle of next week — [[wiki/decisions/2026-10-06-the-ris-mvp1-changes-are-built-for-georgia-only-on-the-1-14-svn-line-with-nothing-else-added.md]] (Oct-9 update). On the blocked statistics host he asked how to tell a registered test machine, and warned the resend chain is "не такая простая" — [[wiki/decisions/2026-10-09-one-machines-bad-statistics-must-stop-blocking-the-statistics-host-and-a-task-is-opened.md]] [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].

## Oct 12 2026 — port 118 moved itself to In Progress; tasks 118–122 on him; location billing API

At the [[wiki/meetings/2026-10-12-daily-standup-flexport-emulator-and-jira-auto-progress-rule.md|Oct-12 stand-up]]: he asked why port task 118 went to In Progress without him — [[wiki/decisions/2026-10-05-a-capability-moves-itself-to-request-review-when-all-its-features-are-completed-and-a-new-story-sends-feature-and-capability-back-to-to-do.md]] (Oct-12 update); four Claude-reviewed tasks (about 118–122) sit on him to review and rewrite clearly — [[wiki/topics/test-automation-strategy.md]] (Oct 12); he asked whether Nathan added the location-billing API — [[wiki/decisions/2026-10-09-all-web-services-go-to-production-before-the-weekend-instead-of-waiting-for-georgia.md]] (Oct-12 update); he is finishing the STG deploy with the CMS changes [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]].

## Oct 13 2026 — SMS/lease tasks and about five port telemetry tasks done; the evening task needs its own meeting

At the [[wiki/meetings/2026-10-13-daily-standup-video-decode-memory-and-release-task-type.md|Oct-13 stand-up]]: he finished "задачи по смски с лизами" and closed about five port tasks with telemetry problems ("наверное, штук 5"). He took the task discussed the evening before, which needs a separate meeting, and asked why "RIS" is involved — [[wiki/decisions/2026-10-06-the-ris-mvp1-changes-are-built-for-georgia-only-on-the-1-14-svn-line-with-nothing-else-added.md]] (Oct-13 update). He questioned why release work cannot use a release branch — [[wiki/decisions/2026-10-05-a-capability-moves-itself-to-request-review-when-all-its-features-are-completed-and-a-new-story-sends-feature-and-capability-back-to-to-do.md]] (Oct-13 update) [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]].

## Oct 14 2026 — remote RIS for old machines; a plan for his task; the release branch

At the [[wiki/meetings/2026-10-14-daily-standup-mvp1-extension-and-rk3576-game-library.md|Oct-14 stand-up]] he said remote RIS by the new scheme works for new machines but not old ones, and asked why the machine protocol must change if all goes through the host — [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 14). He studied a task heard as "бип 35 22"; a plan for it must be discussed — [[wiki/topics/test-automation-strategy.md]] (Oct 14). Kovalchuk said he was right about a release branch — [[wiki/decisions/2026-10-05-a-capability-moves-itself-to-request-review-when-all-its-features-are-completed-and-a-new-story-sends-feature-and-capability-back-to-to-do.md]] (Oct-14 update) [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]].

## Oct 15 2026 — the server answer for a machine with no RIS; BB 3520–3522; the ticket contact number

At the [[wiki/meetings/2026-10-15-daily-standup-offline-ris-fallback-and-nova-game-conversion.md|Oct-15 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]: he works on "BB 35 22" and will rewrite 3521 for a machine with no RIS pulling its RIS and bank configuration; if the machine's software does not match the last installation, the server refuses "как было реализовано ранее" — [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 15). On the e-wallet ticket, the contact number comes from the customer location service; only the customer can change it after set-up, and "Кому звонить, если чтото не то стикет не нам же" — [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 15).

## Oct 15 2026 (11:04 AM, in absentia) — he built part of the role-based access

At the [[wiki/meetings/2026-10-15-wi-fi-router-switch-power-loss-battery-and-mvp2-scope.md|Oct-15 11:04 AM Wi-Fi meeting]] (Russian) Bosik: "Сергей ци[м]онов же это уже частично реализовал" — RBAC — and Bosik and "Дима" put it into production two days earlier — [[wiki/decisions/2026-10-15-service-diagnostics-go-to-the-cloud-with-role-based-access-not-to-the-local-screen.md]] [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

## Oct 16 2026 — rework, the RIS task, three reports; the Stripe experiment waits

At the [[wiki/meetings/2026-10-16-daily-standup-mvp2-wi-fi-scope-and-modem-mac-rollback.md|Oct-16 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]] he finishes his first rework task, then the RIS update/retrieval task, then three report tasks (one fires on an event, one gives statistics over N days). His Stripe card-payment experiment for the payment hub is to be built later, with UI questions open (one unpaid invoice, a list, part-payment); Pavel: RIS first, then Claude-drawn screens to show Val and Andrei — [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 16), [[wiki/decisions/2026-10-15-mvp2-is-flex-iq-wi-fi-remote-update-diagnostics-and-galaxy-reporting-and-flex-pay-moves-to-mvp3.md]] (Oct-16 update). He told Seregin that alerts show only on certain screens, Home by the requirements.

## Oct 19 2026 — lease work on STG; the passport task

At the [[wiki/meetings/2026-10-19-daily-standup-clover-fortune-on-nova-and-encrypted-settings-qr.md|Oct-19 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]] he finished the lease implementation with the soft-install handling (the notes: "LISA"; lease is likely — **inference**) and put it on STG for testing; he works on the passport task now, a separate check in the same chain, and will move its Claude-set Oct 30 due date earlier (Irina: Oct 21–22 at most) — [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 19).

At the [[wiki/meetings/2026-10-20-daily-standup-io-board-firmware-via-github-and-vp9-video-decode.md|Oct-20 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]] he works on the passport task and adds permissions to the update authorization service — [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 20). The AI PM had assigned him its duplicate of the settings-QR spike (created for Location Manager); it stays on him — [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] (Oct-20 update). He starts that day a printer-service task: a problem that came up several times with the "950" printer (model as heard) with our template loaded, which he thinks is in the printer rather than our software, and for which he sees a quick fix; Irina asked him to set a start date, and Pavel will stretch the end date he had set to the 22nd [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]] [[raw/Meeting_Notes_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]].

## Oct 21 2026 — the passport task, software-update roles, the printer task; the mode switch "worked when I built it"

At the [[wiki/meetings/2026-10-21-daily-standup-flex-port-mode-switch-and-sas-crc-fix.md|Oct-21 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]] he said he finishes the passport task that day (last scenarios on the stand, commit planned), also the roles for software updates, and closes the printer task, whose problems were on epic 950 — [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 21). On the Flex-Port mode switch he said it worked when he built and tested it locally, "может сломалось" — [[wiki/decisions/2026-10-20-machines-without-working-aft-connect-by-bill-validator-emulation-and-pulses-in-mvp1-and-the-port-mode-is-set-per-port.md]] (Oct-21 update).

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]

- [[raw/Meeting_Notes_Legacy_CMS_Documentation_Progress_Check-April-15-2026.md]]
- [[raw/Meeting_Transcript_data_access_strategy_and_cms_cloud_migration-March-23-2026.md]]
- [[raw/Payment HUB_ACH module specification_10.11.25.md]]
- [[raw/schedule_review_omni-june-12-2025.md]]
- [[raw/architecture_sql_olap_visualization_1_2025-03-29.md]]
- [[raw/architecture_sql_olap_visualization_2_2025-03-29.md]]
- [[raw/cms_persona_requirements-march-23-2025.md]]
- [[raw/minsk_staff_roster_2025_names-only.md]]
- [[raw/cms_requirements_development-dzima-sergei-andrei.md]]
- [[raw/cms_svn_github-april-14-2025.md]]
- [[raw/cms_github_svn-apr-15-2025.md]]
- [[raw/Meeting_Notes_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]
- [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]]
