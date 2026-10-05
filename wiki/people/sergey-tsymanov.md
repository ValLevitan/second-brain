---
type: person
title: Sergey Tsymanov
date: 2026-07-14
aliases: [Sergey Tsymanov, Siarhei Tsymanau, Sergey Tsimanov, Tsymanau, Tsimanov, Sergei Tsyganov, Tsyganov, Цыганов, Sergei, Sergey]
source-count: 21
open-commitments: 9
disambiguation: "Minsk engineer who drafts CMS requirements with the backend 'Dima' (Chudinov). OWNER-CONFIRMED 2026-07-14 = the payroll 'Siarhei Tsymanau' (Belarusian) and the IT-records 'Sergey Tsimanov' — same person; Tsymanov canonical, Tsymanau/Tsimanov aliases. Distinct from other 'Sergei/Sergey' names (e.g. Sergei Novitsky the advanced-setup technician; Sergey Vysotsky the outside digital-growth specialist, wiki/people/sergey-vysotsky.md); resolve by context."
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

- [ ] Sergey Tsymanov — close one capability-158 (zero balance) task and take the next; drop the ones that no longer apply while wallets stay on the terminal — due Sept 30 2026 — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]

## Sources
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
