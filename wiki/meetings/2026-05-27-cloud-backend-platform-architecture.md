---
type: meeting
title: Cloud Back-end Platform Architecture (May 27 2026)
date: 2026-05-27
aliases: [cloud back-end platform architecture, cloud backend platform, JVL Web Services, gaming web services, transactional web services, land-based cloud platform, gaming web services architecture]
source-count: 1
---

# Cloud Back-end Platform Architecture (May 27 2026)

**Date:** 27 May 2026, 12:35 PM Eastern (§11 recording-header time); ~1h 44m.
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/dmitri-chudinov.md|Dzmitry Chudzinau]], [[wiki/people/andrey-bosik.md|Andrei Bosik]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/sergey-tsymanov.md|Sergey Tsimanov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/igor-metelski.md|Igor Metelski]], [[wiki/people/alexander-biratka.md|Alexander Biratko]], [[wiki/people/anton-leshkevich.md|Anton Leshkevich]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]].

An architecture working session in which Dzmitry walked the team through his proposed catalog of **cloud services for the new land-based machine platform** — the cloud/server tier that pairs with the on-cabinet [[wiki/topics/nova-platform-architecture.md|NOVA]] platform — and the group landed the **"JVL Web Services"** taxonomy (Gaming web services + Transactional web services under one umbrella). This is the dedicated cloud-architecture discussion the [[wiki/meetings/2026-05-13-nova-platform-briefing.md|May-13 NOVA briefing]] had flagged as coming "next week" (former CMS being decomposed under the NOVA umbrella).

The substance — the ~15-service catalog (gateway, Keycloak login, user/operator management, machine registration, the new **manifest registry** and RS-config service, QR service, per-spin event collector, progressive service, financial reporting, license/jurisdiction services, the LGS client); one unified user pool separated by roles; REST-vs-message-broker per case; the operator/customer-registration source dispute (Business Central vs a neutral identity authority); the taxonomy decision and the gaming/transactional split of financial reporting; sequencing (transactional ships next week, gaming web services planning next); and the open product-owner question — lives on [[wiki/topics/nova-platform-architecture.md]] (May-27 2026 cloud-tier section), which cross-links the transactional half on [[wiki/topics/persona-driven-design-and-orchestration-platform.md]]. §15.8: platform/service/module economics only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_Cloud_Backend_Platform_Architecture-May-27-2026.md]]
