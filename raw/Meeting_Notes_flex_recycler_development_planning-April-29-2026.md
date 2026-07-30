# Meeting Summary — Plan Work for Flex-Recycler Development

- **Date:** 2026-04-29 (12:33 local)
- **Source recording:** `Plan work for Flex-Recycler development-20260429_123306-Meeting Recording.txt`
- **Duration:** ~1 h 22 min
- **Topic:** Planning the work for the new product **Flex-Recycler** (IP-1059)

---

## 1. Executive Summary

### Key decisions

1. **Flex-Recycler is established as a separate product** (IP-1059), split from IP-1014 Flex-Cash Dispenser. Owner: Andrei Klimovich. Rationale: separate repository, separate infrastructure, distinct software stack.
2. **Variant B (Cash Recycler) was moved under IP-1059** — Features FP-527 and FP-534 now sit there.
3. **FP-527 was split by audience** — separate stories for player workflow and for operator/service screens (Anton plus a co-owner).
4. **Product concept:** *"the same as Flex-Pay, but the Bill Validator + Card Dispenser pair is replaced by a single Cash Recycler, and the card payout is replaced by direct cash payout."* Card-based redemption is excluded from MVP (to be confirmed with Val).
5. **Key requirements finding:** REQ-1019..1027 and REQ-1037 cover form factor, display, GPS, GLI, and audit print — but they **do not describe the recycler's core business behaviour** (cassettes, denominations, service workflow). Those requirements still need to be authored.
6. **The team walked through every REQ one-by-one,** discussed feasibility for each, and immediately drafted the Feature list under IP-1059.
7. **Work starts now** — Repository Infrastructure begins next week (Alexander Biratko); HAL integration ~2 days after; Cash Recycler work from week-2 of May; finalization of error scenarios on real hardware in early June.

---

## 2. Requirements Discussed (with team commentary)

### 2.1. Existing REQs (REQ-1019..1027, REQ-1037)

- **REQ-1019** (≤ 11.5″ width) — physical requirement owned by Genadi Peri (HW); does not directly affect software but locks in the slim form factor.
- **REQ-1020** (smooth front panel, three apertures only) — physical requirement owned by Genadi Peri. Software implication: UI must not reference non-existent physical controls.
- **REQ-1021** (≤ 15″ flush touchscreen, anti-vandal glass) — physical requirement. **Open question:** what is the resolution and aspect ratio? Genadi Peri mentioned 1388×768, but the team plans Full HD 1920×1080 16:9 (with scaling) for cross-product consistency. **To be confirmed.**
- **REQ-1022** (no physical controls on the front) — *"not interesting for us"* — already covered by current designs. Accepted without further discussion.
- **REQ-1023** (24-hour battery for GPS/IMU) — technical discussion: GPS likely runs independently of the modem and writes its last position into its own memory; the main processor pulls that position when power returns and uploads it when network comes online. **To be verified with Genadi Peri** that the chosen modem supports this mode.
- **REQ-1024** (cellular modem + GPS/IMU mandatory in every unit) — **feasibility concerns:** the current Chinese LTE module on the RK3568 board lacks GPS, and there is no schematic for it. Full-feature modules are *"big bricks with antennas and a battery."* Open discussion with Genadi Peri required.
- **REQ-1025** (cabinet door monitoring across all power states) — accepted. **Implementation refinement:** during a power-off period only the *last* door event is captured (if the door is opened ten times without power, only the last close event will be visible). *"That's good enough; what matters is that we know it was opened."* Reuses existing IO Board API.
- **REQ-1026** (audit/report printing via TiTo printer) — implementable. **Open for Val:** is this MVP or post-MVP? The team envisions a summary report of bill counts by denomination accepted/dispensed over a period (~8 fields).
- **REQ-1027** (all service access from the front) — physical requirement owned by Genadi Peri. Software implication: the service menu must cover **every** service operation through the touchscreen.
- **REQ-1037** (GUI Performance) — platform-level requirement; no separate Feature on Flex-Recycler is needed; FP-527 carries the linkage.

### 2.2. Requirements gaps surfaced during the meeting

The team explicitly flagged that these REQs **do not yet exist** and need to be authored (or AI-generated from the meeting notes):

- **Recycler business logic** — minimum two cassettes, two denominations per cassette (four total); only configured denominations accepted; payout from cassettes; device error/state tracking.
- **Accepted denomination configuration** — which notes are accepted is set in configuration ahead of time; must be displayed to the player.
- **Service workflow for replenishment** — operator opens the door, recounts notes, on close enters how many notes of each denomination are in each cassette; counts are then maintained on the fly.
- **GPS purpose** — what data, sent to whom, at which lifecycle stage.
- **Telemetry over LTE** — what is published: audit, low-cash, full-cassette, error states. Priority order: errors → low cash → overflow. Destination: new microservices stack (like Flex-POS), not legacy CMS. Critical events delivered to operator email/phone.
- **Diagnostics / log retrieval** — network primary (~99% of cases) + USB fallback for poor-connectivity venues. Possibly a separate condensed "important events" log.
- **LED effects** — which events trigger which colours and animations, at what time.
- **Sound effects** — analogous to LEDs; tied to user workflow events (browser-side).
- **Monitor resolution and aspect ratio** — to be confirmed with Genadi Peri (Full HD 16:9 vs native).
- **Repository infrastructure standard** — universal across products: what the repo contains (code, CI-CD, requirements, ADRs, manuals, test cases), how it builds, what artifacts are produced.
- **Player-UI denomination disclosure** — informing the player which denominations the device currently accepts (depends on cassette configuration).

### 2.3. Deferred to business review

- **Card-based payout** — paying winnings to a credit card. Non-trivial because it is disbursement onto third-party cards (not Income Cards). **Likely not MVP**; defer to Val.

---

## 3. Tasks to Create (Features and Stories)

### 3.1. Already done in IP-1059 (status at end of meeting)

- **IP-1059** Flex-Recycler — Product (created)
- **FP-527** — repurposed under the new scope: *"Flex-Recycler — Player GUI and Cash Recycler Workflow"*
- **FP-530** — refocused as *"Cash Recycler Workflow & GUI API"*
- **FP-534** — Cash Redemption and Acceptance via Cash Recycler (with FP-535 / FP-536 / FP-537)

### 3.2. Features to be created under IP-1059

- **Repository Infrastructure / CI-CD**
  Move the repository, mix components from Flex-POS + Flex-Pay, set up CI-CD: jar (backend + GUI) → encrypted updater artifact → full OS image (Linux + bootloader + HAL lib). Release step that tags the commit.
  - Owner: Alexander Biratko
  - Timing: starts next week, ~1 week of work

- **HAL Library Integration (Door / Tamper / Power-state monitoring)**
  Use the HFM-442 (RK3568 HAL) library. Door-open events, tamper, power-down timestamps.
  - Owner: Pavel
  - Timing: ~2 days after CI-CD lands

- **IO Board HAL API Integration — LED Control & Animation**
  Drive the RGB strip; two sides — HAL-side (in HFM) + application-side (in FP). Depends on a future LED-effects requirement.
  - Owner: TBD
  - Timing: after HAL Library Integration

- **(possibly) Sound Control**
  Analogous to LED. Decision in the meeting: **do not split into a separate Feature**, treat it as part of the Player Workflow.

- **Cellular Modem & GPS/IMU Backend Integration**
  Telemetry over LTE: audit reports, low-cash, full-cassette, errors. Connects to the new microservices stack (not CMS). Email/phone notification on critical events.
  - Owner: TBD
  - Timing: depends on modem selection

- **Diagnostic Log Retrieval**
  Network log retrieval + USB fallback. Possibly a dedicated "important events" log.
  - Owner: TBD

### 3.3. Stories to add under existing Features

#### Under FP-527 (Player GUI and Cash Recycler Workflow)

- **Split FP-528 into two stories:** one *"Player Workflow GUI Setup"* (Pavel/Anton) and one *"Operator/Service Menu GUI Setup"* (Anton — fulfill assets, check statuses, etc.). Performed live in Jira during the meeting.
- **Designer story for Igor** — Recycler screen designs (separate story, assigned to Igor).
- **Player UI: accepted-denomination disclosure** — UI must show the player which denominations can be inserted (1/5/10/20 or 5/10/20/50, depending on cassette config).
- **(possibly) 3G-connectivity setup screen** — only if a corresponding requirement is authored.

#### Under FP-534 (Cash Redemption and Acceptance via Cash Recycler)

FP-535 / FP-536 / FP-537 already exist. The meeting added:

- **New story:** *"Finalize positive and negative scenarios of accepting and dispensing with real device"* — finalize on real hardware, ~early June, after device delivery. Basic error handling against library codes can be done earlier.

#### Under FP-530 (Cash Recycler Workflow & GUI API)

- **Cassette replenishment service workflow** — operator-declared denomination/count on close, transition back to operational. Two stories: API level + GUI level.
- **On-the-fly cassette state tracking** — counts maintained in memory, updated on every accept/dispense.
- **Tilt / error-state tracking** — validator-head removal etc. → tilt screen on UI.

### 3.4. Parallel work in HFM

- **CI-CD for the HAL library itself** (HFM-442 / RK3568) — separate task in HFM so the artifact is reusable and not locally built per developer.

### 3.5. Open action items

**Talk to Val:**
- Is audit print (REQ-1026) MVP?
- Is card payout in scope?
- Clarify GPS purpose and data model.

**Talk to Genadi Peri:**
- Is a modem with GPS feasible? Which actual modules are available?
- Bump platform RAM from 2 GB to 4 GB?
- Native monitor resolution and aspect ratio?
- Can GPS run independently of the modem (writing last position to its own memory without main processor power)?

**Generate new REQs** for the 11 gaps from §2.2 — recycler business logic, telemetry, diagnostics, LED, sound, denomination disclosure, monitor resolution, repository standard.

---

## 4. Roadmap (as discussed)

- **Now (April 29):** IP-1059 / FP-527 / FP-530 structure ready.
- **Week of May 4:** Repository Infrastructure starts (Alexander Biratko).
- **Week of May 11:** HAL Integration (Pavel, ~2 days); in parallel, Cash Recycler dispense work begins (FP-535).
- **Late May:** Acceptance work (FP-536) + basic error handling.
- **Early June:** Real device delivered; finalize positive/negative scenarios on hardware.

---

# Plan-vs-Jira Reality Check (Gap Analysis)

Comparison between the meeting plan above and the actual state of IP-1059 in Jira at the time of writing.

**Status legend:** ✅ done · ⚠️ partial / needs verification · ❌ missing · ⚪ deliberately not created

## Features under IP-1059

| Planned in meeting | Jira issue | Status | Notes |
|---|---|---|---|
| Repository Infrastructure / CI-CD | **FP-864** Repository infrastructure | ✅ | |
| HAL Library Integration (Door / Tamper / Power-state) | **FP-866** IO board HAL API integration to monitor Doors, Tampers, Power on/off | ✅ | |
| IO Board HAL API — LED Control & Animation | **FP-865** IO board HAL API integration to control LED animation | ✅ | |
| Cash Redemption and Acceptance via Cash Recycler | **FP-534** | ✅ | Pre-existing; moved under IP-1059 |
| Player GUI and Cash Recycler Workflow | **FP-527** | ✅ | Rewritten this session |
| Cellular Modem & GPS/IMU Backend Integration | — | ❌ | Not created yet |
| Diagnostic Log Retrieval (network primary + USB fallback) | — | ❌ | Not created yet |
| Sound Control | — | ⚪ | Decision in meeting: not a separate Feature; lives in Player Workflow |

## Stories under FP-527 (Player GUI and Cash Recycler Workflow)

| Planned in meeting | Jira issue | Status | Notes |
|---|---|---|---|
| Split FP-528 into player vs. operator | **FP-528** Flex-Recycler setup screens GUI (operator/setup) + **FP-531** Cash Recycler GUI Workflow player view | ✅ | Split was performed live |
| Designer story for Igor | **FP-532** Cash Recycler GUI screens Design for Player presentation and Setup screens | ⚠️ | Exists; assignee currently inherits FP-527 owner — verify it is reassigned to Igor |
| Cash Recycler Workflow & GUI API | **FP-530** | ✅ | Rewritten this session |
| Backend Configuration | **FP-529** Backend Configuration for Variant B Hardware Set | ✅ | Title still says "Variant B" — candidate rename |
| Player UI: accepted-denomination disclosure | — | ❌ | No dedicated story |
| 3G-connectivity setup screen | — | ❌ | Skip until a requirement exists |

## Stories under FP-534 (Cash Redemption and Acceptance)

| Planned in meeting | Jira issue | Status | Notes |
|---|---|---|---|
| Dispense library | **FP-535** Cash Recycler Dispense Communication Java Library | ✅ | |
| Acceptance library | **FP-536** Cash Recycler Acceptance Communication Java Library | ✅ | |
| Error handling | **FP-537** Implement Error Handling for Cash Recycler Operations | ✅ | |
| Finalize scenarios on real device | **FP-867** Finalize positive and negative scenarios of Bill accepting and dispensing with real device | ✅ | Created post-meeting; targeted for ~early June |

## Workflow / orchestration stories planned under FP-530

These were discussed as separate stories but are currently embedded inside FP-530's description rather than tracked individually. Choice: either spin them out as stories under FP-527, or leave them as acceptance criteria inside FP-530.

| Planned in meeting | Jira issue | Status | Notes |
|---|---|---|---|
| Cassette replenishment service workflow (operator-declared count entry) | — | ❌ | Mentioned in FP-530 description; not a tracked story |
| On-the-fly cassette state tracking | — | ⚠️ | Inside FP-530 description; not tracked separately |
| Tilt / error-state tracking (validator-head removal → tilt screen) | — | ❌ | No story |

## HFM project

| Planned in meeting | Jira issue | Status | Notes |
|---|---|---|---|
| CI-CD for the HAL library (HFM-442 / RK3568) | — | ❌ | Belongs in HFM project, not IP-1059 |

## Non-Jira action items

| Planned in meeting | Status |
|---|---|
| Talk to Val — audit-print MVP, card payout, GPS purpose | ⏳ Pending |
| Talk to Genadi Peri — modem with GPS, 4 GB RAM, monitor resolution, GPS-independent operation | ⏳ Pending |
| Author new REQs for the 11 gaps in §2.2 | ⏳ Pending |

## Summary

| Area | Total planned | Done | Missing |
|---|---:|---:|---:|
| Features under IP-1059 | 7 (+ 1 deliberately skipped) | 5 | 2 |
| Stories under FP-527 | 6 | 4 | 2 |
| Stories under FP-534 | 4 | 4 | 0 |
| Stories under FP-530 | 3 | 0 | 3 (currently embedded) |
| HFM parallel work | 1 | 0 | 1 |
| Non-Jira action items | 3 | 0 | 3 |

**Net:** Two missing Features (Cellular/GPS Backend, Diagnostic Logs); four uncovered Stories (denomination disclosure UI; cassette replenishment workflow; cassette state tracking; tilt/error-state tracking); one verification needed (FP-532 assignee = Igor); one HFM parallel task; three external action items still open.
