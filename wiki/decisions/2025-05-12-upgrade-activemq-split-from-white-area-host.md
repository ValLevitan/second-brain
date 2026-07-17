---
type: decision
title: Upgrade ActiveMQ and split it out of the White Area Host application to close the botnet vulnerability
date: 2025-05-12
aliases: [ActiveMQ upgrade, CASWH, White Area Host, WAH, VAHV, CasinoLock, ActiveMQ vulnerability, botnet vulnerability]
source-count: 1
status: active
open-questions: 1
---

# Upgrade ActiveMQ and split it out of the White Area Host application to close the botnet vulnerability

**Decision (Val, worked out with [[wiki/people/dmitri-chudinov.md|Dima]] (Chudinov), [[wiki/people/pavel.md|Pavel]] and [[wiki/people/andrey-bosik.md|Andrei]] (Bosik) on the May 12 2025 call):** start with **step 1** — research/find an **ActiveMQ version** that both closes the known vulnerability **and** stays compatible with JVL's fielded machines, then **separate ActiveMQ into its own application** apart from the JVL Java app (the "White Area Host" / **CASWH**). If no vulnerability-free version proves machine-compatible, fall back to **step 2** — run today's version inside a **Docker container** restarted every ~3 hours to limit exposure. Step 3 was explicitly deferred/undiscussed. [[raw/activeMQ_upgrade-may-12-2025.md]]

## The problem

- The White Area Host application (called "**освах**"/"**косвах**" / **CASWH** in the transcript; the JVL server app machines talk to, still living on **SVN**) uses an old **ActiveMQ** message broker with a known **software vulnerability**. It does **not** give an attacker the filesystem or deeper system access (Dima says he "cut off everything possible" last time), but it lets them **load and execute a file in RAM** — enough to make JVL's machines part of a **botnet** generating "parasitic timing." [[raw/activeMQ_upgrade-may-12-2025.md]]
- ActiveMQ is currently **bundled together with the JVL business-logic app in one place**; the proposal is to make **two separate applications** — one for JVL's business logic, one standalone ActiveMQ — that run together. [[raw/activeMQ_upgrade-may-12-2025.md]]
- Constraint: the **client (machine) side of ActiveMQ cannot be changed** — it is fixed on every machine already shipped and every machine currently going out — so the server-side version must be raised only as far as the machines can still connect (protocol compatibility). This can be checked quickly in the lab by connecting one machine to successive ActiveMQ versions. [[raw/activeMQ_upgrade-may-12-2025.md]]

## The three options laid out

1. **Upgrade the ActiveMQ version + split it into its own application** (minimal steps). Newer versions are claimed to close the vulnerability; JVL can only observe afterward whether that holds. Estimated **~1 week / ~5 working days ("tilde" = up-to)** — mainly **Sergei** (transcribed "Сергей Сандриев" — a JVL engineer; identity unresolved, see below), with [[wiki/people/andrey-bosik.md|Andrei]]'s help on the OS layer. [[wiki/people/dmitri-chudinov.md|Dima]] (Chudinov) owns the Java-app side and scoped the work. [[raw/activeMQ_upgrade-may-12-2025.md]]
2. **Same, plus greater isolation via Docker containers** (possibly on separate servers) so a compromised ActiveMQ stays confined to its container. More capable/manageable but **more work — "one to two sprints" (~a month)** because the current 10-year-old project isn't Docker-ready (DB paths, migration). [[raw/activeMQ_upgrade-may-12-2025.md]]
3. **Not discussed** on this call ("давайте пока про третий шаг не будем говорить"). [[raw/activeMQ_upgrade-may-12-2025.md]]

Val's reasoning against Docker-for-Docker's-sake: containerizing the **whole** app without splitting ActiveMQ out doesn't remove the vulnerability (it still faces the outside world) — so the value is only in first **separating** the lightweight ActiveMQ, which is then easy to containerize later. Docker was noted as a candidate only "for future convenience," and only worthwhile "if the project will live in the future." [[raw/activeMQ_upgrade-may-12-2025.md]]

## Jira artifacts created on the call

- A feature to **"Update ActiveMQ version for CasinoLock"** ("Updating ActiveMQ") was created live; the team reorganized the Jira product hierarchy at the same time (deleting/moving stale items — RGS moved to hang in empty space rather than under a wrong product; **White Area Host** deleted rather than force it into an ill-fitting product). [[raw/activeMQ_upgrade-may-12-2025.md]]
- **Acceptance criteria:** (1) a machine of any supported version can connect to CASWH and pass data; (2) the vulnerability is closed (Dima: closing the vulnerability is really the first criterion — "without closing the vulnerability there's no point upgrading"). Caveat: the vulnerability **can't be reproduced in the test environment**. [[raw/activeMQ_upgrade-may-12-2025.md]]
- Release: CASWH releases independently of the server releases; a **new release VAHV 0.23** was created for it. Work starts "tomorrow." The current mitigation already in place: CASWH runs only ~**3 hours/day** (started ~20:00, off ~23:00 Peru time — the same window as JVL's daily "Jewel/JVL Replication"), and the exploited protocols were blocked (though attackers can trivially change the port). [[raw/activeMQ_upgrade-may-12-2025.md]]

## Open questions

- Which JVL engineer is "**Сергей Сандриев**" tasked with the ActiveMQ/OS work (with an "Ilya" helping update the software)? Not clearly [[wiki/people/sergei-novitsky.md|Sergei Novitsky]] (field/hardware) nor [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (CMS); left unresolved and queued. — [[raw/activeMQ_upgrade-may-12-2025.md]]

## Sources

- [[raw/activeMQ_upgrade-may-12-2025.md]]
