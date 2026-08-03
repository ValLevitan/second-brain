---
type: teams-chat-capture
participants: [Val Levitan, Pavel Frolov]
date: 2026-07-30
source: Teams 1:1 chat (screenshot ingest)
repo: JVL-Core/platform-sdk-rk3568
related: ["Meeting_Notes_Prose_Repo_Compliance_Rollout-July-15-2026", "Meeting_Notes_RIS_Prose_Documentation_Standard-July-2-2026", "Meeting_Notes_Code_Prose_Storage_Standard-July-2-2026"]
---

# Pavel Frolov — RK environment prose spot check (Teams chat, July 30, 2026)

## Chat (morning of July 30, 2026)

- **Val (earlier):** I know that you have been upgrading the RK environment. Are you properly documenting it? I do not want to see the code run away from us undocumented again as it happened every time in the past.
- **Pavel 07:06:** Yes, most changes done through ADR publishing
- **Val 07:06:** this is fantastic! I love it! / May I please push you gently to produce prose for your repository. / Please refer to the standards published in GitHub under knowledge
- **Pavel 07:11:** Actually https://github.com/JVL-Core/platform-sdk-rk3568 already contains prose generated. I will just check what was changed during rk3588 adjustment to reflect in prose → `platform-sdk-rk3568/docs/prose`
- **Val 07:32:** You need to spot check the prose. Did you?

- **Pavel 11:54:** Not yet
- **Val 12:20:** you should not be committing a Prose without a spot check
- **Val 15:26 (sent via Claude):** Full spot-check report shared in chat; asked Pavel to confirm alignment or flag divergence on the stale-chapter list (00, 02, 09, 10, 12) before he starts the rk3588 prose reconciliation.

- **Pavel 12:23 (ET):** Yes this report describes correctly what prose contains and what is missing
- **Val 12:23 (ET):** Good to know. We are now working with a set of facts

**Checkpoint closed:** Pavel confirmed the spot-check report is accurate. Both sides aligned on the stale-chapter list as the agreed set of facts.

## Claude spot check (July 30, 2026)

`docs/prose/` exists and is substantial: 14 numbered chapters + CAPABILITIES.md + README, each with a Russian twin. Prose was authored July 13–14 (commits e10bb36, d6d7521). Since then only two areas were re-synced: FP-521 USB-update prose (July 28) and the CI/CD chapter (HFM-650, July 28).

**Pavel's own caveat is confirmed — the rk3588 adjustment is NOT yet reflected:**

| Chapter | Status | Gap |
| --- | --- | --- |
| 10-boards-and-hardware | **Stale** | Lists only 3 boards (sz3568-v1.2, sz3568-recycler, dc-a568-v06). No cx3588-a / rk3588s board (PRs #79, #82, #83, July 21–23). |
| 02-kernel-drivers-device-trees | **Stale** | Zero rk3588 mentions. Missing HDMI EDID embed (CONFIG_EXTRA_FIRMWARE), USB OTG/VBUS bringup, new DTBs. |
| 12-observability | **Stale** | No pstore/ramoops or boot-attempt telemetry (FP-1179, ADR-125, July 27–28). |
| 00-overview | **Stale** | Zero rk3588 mentions; still frames the BSP as rk3568-only. |
| 09-network-and-modem | **Partially stale** | No HFM-620 LTE DNS failover fix; no RK3568-6 modemd "never report no-SIM from failed AT read" behavior. |
| 06-ci-cd-and-releases | **Current** | Reflects HFM-650 (installer moved to product repo), cx3588-a bring-up image, SoC-scoped artifacts. |
| USB update (FP-521 areas) | **Current** | Prose synced with contract v1.0.1, verify-then-decrypt order (July 28). |

**Bottom line:** prose exists and the two most recent workstreams (FP-521, HFM-650) were dutifully synced, but everything from the rk3588/cx3588-a bringup window (July 21–23) and FP-1179 observability (July 27–28) is undocumented in prose. Pavel said he would do exactly this reconciliation — as of this check it hasn't landed.

## Open item

- [ ] Pavel to update prose chapters 00, 02, 09, 10, 12 for the rk3588/cx3588-a adjustment, FP-1179 pstore/telemetry, HFM-620, and RK3568-6 (per his 07:11 commitment). Scope confirmed accurate by Pavel on July 30; work itself still outstanding.
