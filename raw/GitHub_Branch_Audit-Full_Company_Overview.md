# GitHub Branch Audit — Full Company Overview

**From:** Andrei Bosik \<AndreiB@jvl.ca>
**To:** Val Levitan \<val@jvl.ca>
**Date:** March 13, 2026

---

**Date:** March 12, 2026
**Scope:** JVL-Core (58 repos) + JVL-Games (23 repos) = 81 repos, 116 non-default branches
**Cleanup deadline:** March 20, 2026

---

## Summary

| Metric | JVL-Core | JVL-Games | Total |
|--------|----------|-----------|-------|
| Repos | 58 | 23 | **81** |
| Repos with extra branches | 20 (34%) | 12 (52%) | **32** |
| Clean repos (only main) | 38 (66%) | 11 (48%) | **49** |
| Non-default branches | 78 | 38 | **116** |
| Linked to Jira | 48 (62%) | 25 (66%) | **73 (63%)** |
| No Jira link | 30 (38%) | 13 (34%) | **43 (37%)** |
| Active (<30d) | 33 (42%) | 6 (16%) | **39 (34%)** |
| Stale (30–90d) | 11 (14%) | 6 (16%) | **17 (15%)** |
| Dead (>90d) | 34 (44%) | 26 (68%) | **60 (52%)** |

**Key finding:** Of 73 Jira-linked branches, only 14 (19%) are actually In Progress. 44 branches (60%) are tied to Completed/Closed/Done/Resolved/Published tasks.

---

## 1. Jira task is already Completed or Closed — but the branch is still open (53)

| Author | Repository | Branch | Jira | Jira Status | Last Commit | Days |
|--------|------------|--------|------|-------------|-------------|------|
| Anton Leshkevich | tools-test_360 | CT-5131-VladislavG-LGS-API-Integration-tests | CT-5131 | Closed | 2025-04-25 | **321** |
| Dmitry Chudinov | platform-flex_pay | FP-255-FlexPort-TITO-Server-Integration | FP-255 | Closed | 2025-05-23 | **293** |
| Dmitriy Khandov | platform-omni-assets-calle_ocho | AA-4783-CLO-OMNI-Big-Win | AA-4783 | Closed | 2025-05-28 | **288** |
| Dmitriy Khandov | platform-omni-assets-calle_ocho | AA-4984-CLO-OMNI-Pick-Your-Fortune | AA-4984 | Closed | 2025-05-30 | **286** |
| Dmitriy Khandov | platform-omni-assets-calle_ocho | AA-4964-CLO-OMNI-FreeSpins | AA-4964 | Closed | 2025-05-30 | **286** |
| Dmitriy Khandov | platform-omni-assets | AA-4807-CLO-OMNI-Vdeck | AA-4807 | Done | 2025-06-05 | **280** |
| Dmitriy Khandov | platform-omni-assets | FRAM-744-Tilt-message-assembly | FRAM-744 | Completed | 2025-06-09 | **276** |
| Dmitriy Khandov | platform-omni-assets-fortune_fu_paws | CT-5016-Game-Server-Interface | CT-5016 | Completed | 2025-06-12 | **273** |
| Dmitry Chudinov | infrastructure-casino_management_system-core | BEP-2609-Server-parameters-setup | BEP-2609 | Closed | 2025-06-19 | **266** |
| Dmitriy Khandov | platform-omni-assets | AA-5289-CLO-OMNI-General-Framework-Dialogs | AA-5289 | Done | 2025-07-18 | **237** |
| Sergey Tsimanov | platform-progressive-controller | BEP-2607-Building-GH-action | BEP-2607 | Completed | 2025-07-24 | **231** |
| Irina Shyshko | tools-test_360 | LGS-676_IS_Machine_Configuration | LGS-676 | Published | 2025-07-31 | **224** |
| Dmitriy Khandov | platform-omni-game-fortune_fu_paws | AA-4480-FFP-DT-PS-Variations | AA-4480 | Done | 2025-08-07 | **217** |
| Dmitriy Khandov | platform-omni-assets | FRAM-823-CLO-OMNI-Bonus-scene | FRAM-823 | Completed | 2025-08-14 | **210** |
| Julia Aksamit | platform-omni-assets | AA-5450_adjusting_videos | AA-5450 | Closed | 2025-08-27 | **197** |
| Alexander Biratko | platform-omni-framework-landbase | FRAM-879-Game-Loader-screen | FRAM-879 | Completed | 2025-10-07 | **156** |
| Dmitry Chudinov | infrastructure-orchestration-payment_hub-web_service | BEP-2654-Incomm-API-Integration | BEP-2654 | Completed | 2025-10-10 | **153** |
| Sergey Tsimanov | infrastructure-orchestration-payment_hub-web_service | BEP-2661-Deployment-to-Test-and-Prod | BEP-2661 | Completed | 2025-10-22 | **141** |
| Sergey Tsimanov | platform-flex_pos | FP-449-Swipe-Magnetic-Card-Reader | FP-449 | Completed | 2025-10-29 | **134** |
| Dmitry Chudinov | platform-flex_pos | FP-448-Payment-Hub-Integration | FP-448 | Completed | 2025-11-12 | **120** |
| Sergey Tsimanov | platform-flex_pos | FP-450-Card-Dispensor-Integration | FP-450 | Completed | 2025-11-12 | **120** |
| Dmitry Chudinov | platform-flex_pos | FP-457-Flex-POS-Setup-architecture | FP-457 | Completed | 2025-11-17 | **115** |
| Alexander Biratko | platform-omni-game-calle_ocho | FRAM-959-Vdeck-promo-text-is-lost | FRAM-959 | Closed | 2025-11-24 | **108** |
| Dmitry Chudinov | platform-flex_pos | FP-464-Extend-API-to-send-receipt | FP-464 | Closed | 2025-12-01 | **101** |
| Anton Seregin | platform-flex_pos | FP-465-Multilanguage-support | FP-465 | Closed | 2025-12-02 | **100** |
| Alexander Biratko | platform-omni-game-calle_ocho | FRAM-960-App-UI-Freezes | FRAM-960 | Resolved | 2025-12-03 | **99** |
| Alexander Biratko | platform-omni-game-calle_ocho | FRAM-961-Pick-your-Fortune-dialog | FRAM-961 | Closed | 2025-12-11 | **91** |
| Dmitriy Khandov | platform-omni-assets-calle_ocho | AA-5445-CLO-OMNI-Art-Assets-fine-tuning | AA-5445 | Done | 2025-12-12 | 90 |
| Sergey Tsimanov | platform-flex_pos | FP-420-Flex-POS-Receipt-printing-support | FP-420 | Completed | 2025-12-17 | 85 |
| Pavel Frolov | platform-flex-os-installer | CT-5267-Install-artifacts-to-Azure | CT-5267 | Closed | 2026-01-06 | 65 |
| Dmitriy Khandov | platform-omni-assets | AA-5445-CLO-OMNI-Art-Assets-fine-tuning | AA-5445 | Done | 2026-01-06 | 65 |
| Sergey Tsimanov | infrastructure-orchestration-auth-web_service | BEP-2680-Docker-based-Authentication | BEP-2680 | Completed | 2026-01-08 | 63 |
| Anton Seregin | infrastructure-orchestration-core-frontend | BEP-2695-Frontend-Application-infrastructure | BEP-2695 | Completed | 2026-01-21 | 50 |
| Pavel Frolov | platform-flex-hal | feature/CT-5335-unified-hal-api-pyramid-printers | CT-5335 | Completed | 2026-01-31 | 39 |
| Sergey Tsimanov | infrastructure-orchestration-gateway-web_service | BEP-2688-Flex-POS-registration-cloud | BEP-2688 | Completed | 2026-02-03 | 37 |
| Vladimir Samusenko | platform-local_gaming_server | LGS-183-LGS-192-Data-Center-UI-Gamble-Mode | LGS-183 | Closed | 2026-02-10 | 30 |
| Alexander Biratko | platform-flex_pos | FP-441-Backend-for-GUI-Workflow | FP-441 | Completed | 2026-02-13 | 27 |
| Anton Seregin | infrastructure-orchestration-core-frontend | BEP-2742-Scanner-Application-GUI | BEP-2742 | Completed | 2026-02-18 | 22 |
| Dmitry Chudinov | platform-flex_pos | FP-447-Flex-POS-registration-procedure | FP-447 | Completed | 2026-02-20 | 20 |
| Dmitry Chudinov | platform-flex_pos | CT-5499-github-actions-build-artifacts | CT-5499 | Completed | 2026-02-23 | 17 |
| Sergey Tsimanov | infrastructure-orchestration-terminal_registration-web_service | BEP-2659-secure-transactions | BEP-2659 | Completed | 2026-02-25 | 15 |
| Dmitry Chudinov | infrastructure-orchestration-terminal_hub-web_service | feature/BEP-2659 | BEP-2659 | Completed | 2026-02-26 | 14 |
| Dmitry Chudinov | platform-flex_pos | feature/BEP-2659-secure-terminal-payment-hub | BEP-2659 | Completed | 2026-02-26 | 14 |
| Dmitry Chudinov | infrastructure-casino_management_system-core | LGS-1016-add-keno-product-games-to-stg | LGS-1016 | Completed | 2026-02-26 | 14 |
| Alexander Biratko | platform-local_gaming_server | LGS-224-Data-Center-UI-Meters-Handpay-Report | LGS-224 | Completed | 2026-02-27 | 13 |
| Alexey Khamin | tools-test_360 | AlexeyK-CT-5375-UI-Scroll-Support | CT-5375 | Closed | 2026-02-27 | 13 |
| Dmitry Chudinov | infrastructure-orchestration-payment_hub-web_service | BEP-2659-Secure-transactions | BEP-2659 | Completed | 2026-03-06 | 6 |
| Dmitry Chudinov | infrastructure-orchestration-terminal_hub-web_service | feature/BEP-2762 | BEP-2762 | Completed | 2026-03-06 | 6 |
| Dmitry Chudinov | platform-flex_pos | feature/BEP-2762-simplified-inter-service-communication | BEP-2762 | Completed | 2026-03-06 | 6 |
| Pavel Frolov | platform-flex_pos | HFM-319-Flex-POS-Application-Integration | HFM-319 | Completed | 2026-03-06 | 6 |
| Pavel Frolov | platform-application_updater | FP-519-Flex-POS-software-update | FP-519 | Completed | 2026-03-09 | 3 |
| Dmitry Chudinov | infrastructure-orchestration-payment_hub-web_service | BEP-2733-API-for-ACH | BEP-2733 | Completed | 2026-03-10 | 2 |
| Anton Seregin | infrastructure-orchestration-core-frontend | BEP-2764-Customer-List-Dashboard-GUI | BEP-2764 | Completed | 2026-03-12 | 0 |

---

## 2. No commits for over 90 days — Jira task NOT completed (5)

| Author | Repository | Branch | Jira | Jira Status | Last Commit | Days |
|--------|------------|--------|------|-------------|-------------|------|
| Sergey Tsimanov | infrastructure-flex_pay-communicator | FP-181-Remote-Firmware-update | FP-181 | To Do | 2025-03-04 | **373** |
| Igar Miatselski | platform-omni-core | FRAM-672-Games-Dashboard | FRAM-672 | Request Review | 2025-05-05 | **311** |
| Dmitry Chudinov | infrastructure-orchestration-payment_hub-web_service | BEP-2652-Card-Activation | BEP-2652 | To Do | 2025-10-03 | **160** |
| Igar Miatselski | platform-omni-game-calle_ocho | FRAM-7-Tickers | FRAM-7 | Request Review | 2025-12-09 | **93** |
| Igar Miatselski | platform-omni-framework-landbase | FRAM-7-Tickers | FRAM-7 | Request Review | 2025-12-10 | **92** |

---

## 3. No Jira link at all (52)

| Author | Repository | Branch | Last Commit | Days |
|--------|------------|--------|-------------|------|
| Alexander Biratko | platform-flex_pay | test-flex-port | 2024-08-08 | 581 |
| Alexander Biratko | platform-flex_pay | card-dispenser-protocol | 2024-09-03 | 555 |
| Dmitry Chudinov | platform-flex_pay | transition-to-state-machine-pattern | 2024-09-30 | 528 |
| Evgeny Kharetski | platform-flex_pay | led-effects-api | 2024-10-08 | 520 |
| Dmitry Chudinov | platform-flex_pay | 2-bv-feature | 2025-01-29 | 407 |
| Dmitriy Khandov | platform-omni-game-fortune_fu_paws | test_lfs_branch | 2025-02-18 | 387 |
| Alexander Biratko | platform-omni-game-fortune_fu_paws | fix-workflow-display | 2025-02-26 | 379 |
| Dmitry Chudinov | infrastructure-flex_pay-communicator | chore/initial-setup | 2025-03-10 | 367 |
| Dmitry Chudinov | infrastructure-services-scanner | git-svn | 2025-03-11 | 366 |
| Alexander Biratko | tools-omni-features-examples | dev | 2025-05-06 | 310 |
| Efim Podvoiski | platform-math_configs | ffp | 2025-05-13 | 303 |
| Dmitry Chudinov | platform-flex_pay | Flex-Port-Test-Firmware-Update | 2025-06-17 | 268 |
| Dmitry Chudinov | platform-flex_pay | Fake_Incomm_For_Fellipe | 2025-06-23 | 262 |
| Dmitry Chudinov | platform-flex_pay | dev | 2025-06-25 | 260 |
| Ivan Shpak | tools-test_360 | Integration-tests-IvanS | 2025-06-26 | 259 |
| Alexey Khamin | tools-test_360 | old_main | 2025-07-10 | 245 |
| Dmitry Chudinov | platform-flex_pay | TITO-mode | 2025-08-15 | 209 |
| Alexander Biratko | platform-omni-core | detached | 2025-10-02 | 162 |
| Dmitry Chudinov | platform-flex_pay | move-to-backend | 2025-10-02 | 161 |
| Dmitry Chudinov | infrastructure-orchestration-payment_hub-web_service | main-2654-test | 2025-10-13 | 150 |
| Dmitry Chudinov | infrastructure-casino_management_system-core | taag-47-fix-mobile-scan | 2025-10-31 | 132 |
| Anton Leshkevich | tools-test_360 | revert-49-preset-builder | 2025-11-04 | 128 |
| Alexander Biratko | platform-omni-game-calle_ocho | dev | 2025-11-11 | 121 |
| Alexander Biratko | platform-omni-game-calle_ocho | test | 2025-11-17 | 115 |
| Alexander Biratko | platform-omni-game-calle_ocho | test-merge | 2025-11-19 | 113 |
| Alexander Biratko | platform-sdk-ui_kit | detached | 2025-12-01 | 101 |
| Alexander Biratko | platform-sdk-ui_kit | detached2 | 2025-12-01 | 101 |
| Nathan Carver | infrastructure-orchestration-payment_hub-web_service | requirements/BEP-2692 | 2025-12-12 | 90 |
| Efim Podvoiski | platform-math_engine | keno | 2026-01-15 | 56 |
| Efim Podvoiski | platform-math_engine-api | keno | 2026-01-15 | 56 |
| Dmitry Chudinov | platform-progressive-controller | Multi-product-implementation | 2026-01-15 | 56 |
| Efim Podvoiski | platform-math_engine | documentation | 2026-02-04 | 36 |
| Anton Seregin | platform-sdk-ui_kit | detached3 | 2026-02-04 | 36 |
| Aaron Bockelie | platform-local_gaming_server | docs/documentation-coverage-analysis | 2026-02-06 | 34 |
| Aaron Bockelie | infrastructure-orchestration-core-frontend | chore/ways-alignment | 2026-02-11 | 29 |
| Eugine Yavorsky | platform-flex_port | docs/docstrings-tasksys | 2026-02-16 | 24 |
| Eugine Yavorsky | platform-flex_port | docs/docstrings-taskwss | 2026-02-17 | 23 |
| Evgeny Kharetski | platform-progressive-controller | mariadb | 2026-02-19 | 21 |
| Eugine Yavorsky | platform-flex_port | docs/docstrings-taskpay | 2026-02-21 | 19 |
| Eugine Yavorsky | platform-flex_port | docs/docstrings-taskeeprom | 2026-02-23 | 17 |
| Dmitry Chudinov | platform-flex_pos | adr-backfill-initial-coverage | 2026-02-23 | 17 |
| Eugine Yavorsky | platform-flex_port | docker_build | 2026-02-25 | 15 |
| Pavel Frolov | platform-sdk-rk3568 | refactor/migrate-legacy-adrs | 2026-02-26 | 14 |
| Dmitry Chudinov | infrastructure-orchestration-terminal_hub-web_service | docs/architecture-decision-records | 2026-02-26 | 14 |
| Eugine Yavorsky | platform-flex_port | docs/getting-started | 2026-02-26 | 14 |
| Alexander Biratko | platform-omni-framework-landbase | dev | 2026-02-27 | 13 |
| Alexander Biratko | platform-sdk-sound-fmod_libraries | no-music-in-a-game | 2026-03-04 | 8 |
| Alexander Korochkin | tools-test_360 | dev | 2026-03-06 | 6 |
| Alexander Korochkin | tools-test_360 | korochkin | 2026-03-06 | 6 |
| Efim Podvoiski | platform-math_engine | unit-tests | 2026-03-10 | 2 |
| Eugine Yavorsky | platform-flex_port | feature/consistent-balance-on-cancel-transaction | 2026-03-11 | 1 |
| Evgeny Kharetski | platform-flex_port | docs/glossary | 2026-03-11 | 1 |

---

## Per-Author Summary

| Author | Sec.1 (Jira done) | Sec.2 (Dead >90d) | Sec.3 (No Jira) | Total | Email sent |
|--------|-------------------|-------------------|-----------------|-------|------------|
| Dmitry Chudinov | 15 | 1 | 13 | **29** | Yes |
| Alexander Biratko | 6 | — | 12 | **18** | Yes |
| Dmitriy Khandov | 11 | — | 1 | **12** | Yes |
| Sergey Tsimanov | 8 | 1 | — | **9** | Yes |
| Eugine Yavorsky | — | — | 7 | **7** | No (excluded) |
| Pavel Frolov | 4 | — | 1 | **5** | Yes |
| Anton Seregin | 4 | — | 1 | **5** | Yes |
| Efim Podvoiski | — | — | 5 | **5** | Yes |
| Igar Miatselski | — | 3 | — | **3** | Yes |
| Evgeny Kharetski | — | — | 3 | **3** | Yes |
| Aaron Bockelie | — | — | 2 | **2** | No (excluded) |
| Alexander Korochkin | — | — | 2 | **2** | No (excluded) |
| Anton Leshkevich | 1 | — | 1 | **2** | Yes |
| Alexey Khamin | 1 | — | 1 | **2** | Yes |
| Nathan Carver | — | — | 1 | **1** | No (excluded) |
| Irina Shyshko | 1 | — | — | **1** | Yes |
| Ivan Shpak | — | — | 1 | **1** | Yes |
| Julia Aksamit | 1 | — | — | **1** | Yes |
| Vladimir Samusenko | 1 | — | — | **1** | Yes |

**Total garbage branches:** 110 | **Cleanup emails sent to:** 15 people | **Excluded from emails:** Nathan Carver, Aaron Bockelie, Andrew Khandov, Alexander Korochkin, Eugine Yavorsky

---

Andrei Bosik
Cloud Systems Manager
AndreiB@jvl.ca | www.jvl.ca
