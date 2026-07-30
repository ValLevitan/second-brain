---
type: meeting
title: CI Architecture — Payment Platform (Apr 17 2026)
date: 2026-04-17
aliases: [CI Architecture Payment Platform, Continuous Integration Architecture Payment Platform, meta repository, Zero Trust model, data contracts from code, integration repo scope, back-end to front-end ordering, version pinning]
source-count: 2
---

# CI Architecture — Payment Platform (Apr 17 2026)

**Date:** 17 April 2026, 12:10pm Eastern (§11 recording header); ~2h 19m.
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/aaron.md|Aaron Bockelie]], [[wiki/people/andrey-bosik.md|Andrei Bosik]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] (transcribed "Biratko"/"Sasha"), [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] (the meta-repo docs were built by [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]], transcribed "Dmitriy Chudzinau"/"Jima").

The **first session of a "CI Architecture" series** on the continuous-integration / build-and-deploy architecture for JVL's payment platform — walking Andrei's new "meta repository" (links, not git submodules, to the service repos), then Aaron's push for a **Zero Trust** model where each service owns its own generated **data contract** (Swagger/Javadoc/rustdoc, not hand-written central `.md` files), the integration repo scoped to deployment/tests/infrastructure only (no code, no contracts), a back-end→CI→front-end→E2E implementation order, and mandatory version pinning; plus the emerging per-repo Claude-agent pattern and Val's "cash is the only source of truth" pushback against requirements-first process. Team to **reconvene Friday Apr 24** after Aaron publishes the updated CI document. Substance and citations live on [[wiki/topics/github-release-management-pipeline.md]] (Apr 17 2026 section), which sequences the series (continues the Apr-13 v2→v3 repo-standard thread); the per-repo Claude pattern is on [[wiki/topics/ai-assisted-development.md]] and the payment-platform product context on [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/Meeting_Notes_CI_Architecture_Payment_Platform-April-17-2026.md]]

## Sources
- [[raw/Meeting_Transcript_CI_architecture_payment_platform-April-17-2026.md]]
- [[raw/Meeting_Notes_CI_Architecture_Payment_Platform-April-17-2026.md]]
