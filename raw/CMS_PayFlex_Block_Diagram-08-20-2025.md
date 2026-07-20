**CMS / Flexpay – Meeting Summary**

**Executive Overview**

JVL is aligning its CMS evolution with the Flexpay program for the Georgia market. From **July 1** (next year), Georgia regulations require player cash-outs to be loaded onto **Mastercard gift cards**—no cash handling—so Flexpay devices and the CMS must orchestrate compliant payout flows and remote management.

**Attendees & Roles**

- **Juan Martinez** — VP Product & Distribution (from example doc; role not explicitly stated in this transcript)
- **Pavel Frolov** — Director of Engineering (in charge of engineering).
- **Will Jones** — Consultant (from example doc; title not announced in this transcript)
- **Nathan Carver** — Technical Product Manager (technical product manager focused on documentation/use cases).

If a title isn’t in the transcript, the example’s title is used; otherwise it is noted as **Not Known**.

**1) Goals & Scope (Today → Near Term)**

- **Flexpay compliance for Georgia**: Ensure end-to-end cash-out to Mastercard gift cards (no cash).
- **CMS device management**: Future CMS should provide a **dashboard** for device tracking, administration, and **firmware updates**.
- **Clarify & capture CMS knowledge**: Current CMS documentation is fragmented (“tribal knowledge”); need a consolidated source.

**2) Current State (Legacy CMS + Flexpay)**

- A **Flexpay Manager** tab exists in the legacy CMS showing kiosk records (e.g., MAC, software version, status); two kiosks are currently “online” (Georgia).
- Purpose of this legacy integration: support **remote initial setup** and **remote configuration** (credential updates, settings pushed to kiosks).

**3) Architecture Direction**

- **Separate CMS server** for the next-gen design; first focus is **management of different payment terminals** (mirrors current CMS functions but aligns with new architecture).
- **Remote access today** is limited to an API between the CMS and the on-location master device using a **proprietary WSS protocol**; log retrieval is available.

**4) Decisions / Agreements**

- Proceed with a **separate-server** approach for new CMS capabilities, emphasizing device/payment-terminal management.
- Legacy CMS will continue to host **Flexpay Manager** features to support active pilots/field units until migration.

**5) Open Questions**

1. **Documentation Source of Truth**: Where should comprehensive CMS docs live going forward (vs. scattered/tribal knowledge)?
2. **Remote Ops Scope**: Beyond current WSS/log retrieval, what additional **remote management** functions are required in the new CMS (e.g., firmware orchestration, telemetry dashboards)?
3. **Flexpay Data Model**: Define the canonical data fields and status model for kiosks/devices across legacy and new CMS (seen today in Flexpay Manager).

**6) Action Items & Owners**

- **Pavel Frolov**:
    - Prepare **updated schematics/diagrams** of the current implementation for the next meeting; locate and export prior **Miro board** artifacts.
    - Assess whether to **create a new design from scratch** aligned to the new architecture.
- **Nathan Carver**:
    - Continue compiling **use cases** and capability groupings for **Flex POS/Flex systems** to inform CMS requirements.
- **Juan Martinez**:
    - Outline **dashboard requirements** (device tracking, admin, firmware updates) for the future CMS.
- **Will Jones**:
    - Review compliance workflow implications stemming from **Georgia July 1** Mastercard-only payouts and ensure CMS/Flexpay design covers edge cases.

**7) Risks & Dependencies**

- **Regulatory deadline** (Georgia **July 1**) drives scope/timeline; slippage risks compliance.
- **Documentation gap** could hinder onboarding and cross-team velocity.
- **Legacy → New CMS** migration complexity (device states, configs, remote ops parity).

**8) Next Steps / Timeline**

- **Before next meeting**: Updated diagrams and exported artifacts ready (Pavel).
- **Requirements iteration**: Incorporate Flex POS use cases (Nathan) and dashboard requirements (Juan) into the **separate-server** CMS outline.

_Prepared from the transcript_ **_CMS-Block_Diagram_Arch.md_**_._