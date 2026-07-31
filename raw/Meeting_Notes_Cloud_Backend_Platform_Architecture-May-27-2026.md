# Meeting Summary — Cloud Back-end Platform — Architecture Working Session

**Date:** 27 May 2026, 12:35 PM Eastern
**Duration:** ~1h 44m
**Attendees:** Val Levitan, Dzmitry Chudzinau, Andrei Bosik, Pavel Frolov, Sergey Tsimanov, Irina Shishko, Igor Metelski, Alexander Biratko, Anton Leshkevich, Evgeny Kharetski

## Summary

Dzmitry walked the team through his proposed list of cloud services for the new land-based machine platform. He named about 15 services and explained what each one does.

The main pieces:
- A gateway that routes all incoming requests.
- Keycloak-based login.
- A user management service for roles and permissions.
- An operator management service that pulls operator and jurisdiction data from an upstream source (Dzmitry proposed Business Central; Val pushed back — see decisions).
- Machine registration (same pattern as the transactional side).
- A new **manifest registry**: each piece of machine software (game, math, theme, framework) publishes its own capabilities, so the server knows what the machine can do without people typing it in.
- An RS configuration service that builds the recommended-settings file from the manifests.
- A QR service for offline machines.
- An event collector that captures data per spin, not just daily totals.
- A progressive service that can run across many locations.
- Financial reporting (replaces today's Palapku Bam + Tableau).
- License management, possibly driven by Business Central.
- Jurisdiction rules.
- The on-machine client (LGS).

**Users — one pool or separate?** Dzmitry asked whether land-based and transactional users will be unified. Val: yes, one pool. Roles separate them. If a product line ever gets sold, that's a one-time "divorce" — don't design for it now.

**One domain or many?** Andrei raised the question. Tentative answer: one umbrella domain for everything (machines, transactional, web services). Val open to buying a neutral marketing name. Not locked.

**Customer registration source.** Dzmitry wanted Business Central as the source of truth for new operators. Val disagreed — wants a neutral identity authority with automated validation (federal license lookups, Google/Microsoft SSO, SMS, etc.). Val will consult external advisors. Keycloak will likely hold the central data.

**Service-to-service protocol.** Pick per case. REST for sync, browser-facing, internal. RabbitMQ for async, encrypted, external. Front-end can only do REST. *(See catalog: actual implementation choice is ActiveMQ self-hosted in EKS.)*

**Health checks.** Kubernetes pings each container's health endpoint. If a container dies, K8s restarts it. At least two copies of each service always run.

**Old machines.** Andrei asked whether old machines can be re-registered into the new system to retire legacy. Dzmitry: registration is easy, but old software has no manifests and old data structures don't fit. Big lift. Possible mass case: Arc Pacific. Otherwise deferred.

**Server-side barcode for machine registration.** Open problem. Dzmitry wants the server to generate the number, but metal plates are ordered before the machine exists, so the number must exist first. No solution today.

**Taxonomy.** Long discussion. Landed on: everything is **JVL Web Services**. Two groups under that name — **Gaming web services** (what Dzmitry just presented, for new land-based machines) and **Transactional web services** (already in development). Financial reporting must be split between the two — different data, independent deployment.

**Sequencing.** Transactional ships next week. Gaming web services planning is next. About 90% of the patterns are shared.

**Product owner for gaming web services.** Open. Andrei Klemyel is busy on transactional. Igor Metelski has the knowledge. [Personal passage removed — owner ruling 2026-09-28: the JVL brain holds JVL matters only. Original kept in the source vault.] Val proposed Alexey Khamin (Lesha). Evgeny Kharetski declined to take more on. Val to decide.

**Data retention.** Andrei flagged for future planning, not for today. Different types (financial vs event) need different keep-periods and possibly aggregation. Not blocking.

## Decisions Made

- **One user pool across land-based and transactional, separated by Keycloak roles.** No pre-engineering for a future sale. (Val)
- **Inter-service communication uses both REST and a message broker, picked per feature** based on sync/async, encryption, and load. (Val, with team agreement)
- **Financial reporting is a separate service per group — gaming and transactional do not share it.** Different data, independent deployment. (Val + team)
- **Naming: "JVL Web Services" is the umbrella. Under it sit Gaming web services and Transactional web services.** (Val)
- **Operator/customer registration will use a neutral identity authority, not Business Central as the primary source.** Direction is automated validation (federal license, SSO, SMS). (Val)
- **Defer the legacy migration question.** No commitment to retire legacy CMS now. (Team)
- **Defer the server-side barcode problem.** Metal plate lead times block it today. (Team)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Dzmitry Chudzinau | Build the capabilities list for gaming web services and bring it back for review | TBD | High | Next planning artifact before implementation |
| 2 | Dzmitry Chudzinau | Produce a diagram showing gaming and transactional web services side by side, with shared parts called out | TBD | Normal | Val asked for the full picture |
| 3 | Val Levitan | Decide product owner for gaming web services (Lesha proposed) | TBD | High | Blocks formal requirements work |
| 4 | Val Levitan | Consult outside advisors on automated customer-identity validation in North America | TBD | Normal | Drives the registration design |
| 5 | Team | Bring data classification, retention, and volume forecast to a future session | TBD | Low | Andrei flagged for the future agenda |
| 6 | Team | Revisit single-domain vs multi-domain once marketing direction is clearer | TBD | Low | One umbrella domain is tentative |

## Open Questions

- Product owner for gaming web services — Val to decide.
- Customer registration source — Val to consult advisors.
- One domain or many for JVL Web Services — not locked.
- Server-side barcode vs metal plate lead time — no answer yet.
- Whether to retire legacy CMS and migrate old machines — deferred.
- Data retention policy — to be tabled in a future session.

## Supporting Documents

- [[new-egm-platform-services-catalog|Services catalog circulated by Dzmitry]] — full 14-service catalog (CMS 2.0 / Landbase cloud platform) with stacks, dependencies, and clickable architecture diagram. Canonical copy lives in `Initiatives/JVL Gaming Web Services/`.

---
*Processed from Teams transcript on 2026-05-27*
*Source meeting: Cloud Back-end Platform — Architecture Working Session*
