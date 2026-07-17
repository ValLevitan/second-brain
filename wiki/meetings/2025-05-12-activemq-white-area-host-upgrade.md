---
type: meeting
title: ActiveMQ / White Area Host security-upgrade planning
date: 2025-05-12
aliases: [ActiveMQ upgrade meeting, CASWH upgrade, White Area Host botnet]
source-count: 1
---

# ActiveMQ / White Area Host security-upgrade planning

**May 12 2025** (~85 min; Russian; audio transcribed 2025-05-13). [[wiki/people/val-levitan.md|Val]] with [[wiki/people/dmitri-chudinov.md|Dima Chudinov]], [[wiki/people/pavel.md|Pavel]] and [[wiki/people/andrey-bosik.md|Andrei Bosik]] plan how to close a botnet-exploitable **ActiveMQ** vulnerability in JVL's **White Area Host** (CASWH) machine-messaging application, and clean up the related Jira product hierarchy. Internally duplicated transcript (the discussion replays, with stuck "OK"/"try my best" loops at the end) — facts taken once (§12).

The ruling (upgrade + split ActiveMQ out; Docker/3-hour-restart fallback), the three options, the Jira feature/VAHV-0.23 release, and the unresolved "Sergei Sandriev" engineer are on [[wiki/decisions/2025-05-12-upgrade-activemq-split-from-white-area-host.md]]. The vulnerability/system context is on [[wiki/topics/infosec-and-server-infrastructure.md]] and the CASWH glossary entry on [[wiki/topics/jvl-machine-lineup.md]].

## Sources

- [[raw/activeMQ_upgrade-may-12-2025.md]]
