# Meeting Summary — Recycler Requirements, Scope, Acceptance

**Date:** April 28, 2026, 1:04 PM Eastern
**Duration:** ~1h 12m
**Attendees:** Val Levitan, Pavel Frolov, Alexander Biratko, Genadi Peari, Irina Shishko

## Summary

Val opened by framing the meeting around the new bill recycler product (Flex_Recycler) running on the Rockchip RK3568 platform. His original intent was to discuss giving an integration contract to Evgeny Alekseev on the assumption that Alekseev knows the recycler's byte-level protocol "inside and out" because he previously implemented (but never tested) the same protocol for FlexPay. Val asked the team how to brief Alekseev properly: how to write acceptance criteria, where to seat his repository, how to control his pull requests, and how to test the work he hands back.

Pavel responded by laying out the existing transaction-product architecture, which he proposed should not change for the new platform: a Linux machine running a Java backend application that drives all workflow logic and operator/player communication, with a browser-based GUI on top of the backend communicating over a known IP. Pavel suggested taking FlexPOS as the reference implementation and adapting the backend with minimal changes. Alexander Biratko corrected this to "augment, not rewrite": keep the architecture and graphical screens as-is, change only the parts specific to recycler operation.

Genadi Peari interjected with a critical observation that reshaped the meeting: he was almost certain the recycler vendor (which the team identified as the same firm behind the MEI bill validator they already use, with connections, harness, and library "absolutely identical") supplies a ready-made Java library. He pointed Pavel to the vendor's GitHub. The team navigated to the vendor's repository on the Microsoft Teams call and confirmed Genadi's hypothesis live: a 2025-vintage Java library exists for the recycler, with API, demo, console demo, and integration toolkit. Alexander pulled the library and confirmed "the additional methods are a bunch, but it's their library, and it's fresh, 2025 vintage." Their existing MEI library is from 2016 and was decompiled and repacked to fix bugs over the years.

This single discovery flipped the staffing decision. Once the team confirmed that no byte-level protocol implementation was needed, only a higher-level integration on top of a vendor-supplied Java library, Val concluded that **Alekseev is no longer needed for this work.** The remaining work is integration into JVL's existing application stack (Java backend, UI, workflow), which the in-house team handles with Claude Code.

The team then shifted to architecture and repository structure. Pavel and Alexander aligned on creating a **new repository for Flex_Recycler** rather than forking FlexPOS. Val pushed back against forking on the grounds that forks drag in dead code: code paths nobody touches that accumulate and pollute. Alexander acknowledged dead code is technically acceptable in Java (it doesn't compile if unloaded), but agreed it interferes with Claude Code by inflating context. The agreed approach: assemble the new product from selected parts of FlexPay and FlexDispenser, then use Claude Code to clean unneeded services and calls. The Linux base (RK3568 root) is consumed as a build artifact from its existing repo, not copied. A third repository may exist for IO board libraries.

Pavel proposed reusing the **IO Board from the gaming machines** for door sensors, switch monitoring, and LED controller functionality. Val initially objected on cost grounds ("it's very expensive"), but Genadi clarified that the board's high price comes almost entirely from 1.5MB of FRAM memory required for transactions. For this use case, depopulating the FRAM (via no-populate of six chips, leaving one) drops the price by roughly $30 and produces a cheap, already-tested, already-designed board. A small 16-kilobit FRAM remains for minor needs.

A debate then opened on the firmware language. Val wants to move JVL "categorically away from C++", including library layers in the operating system, and toward **Rust**, citing his self-education on the topic. Pavel pushed back: he is "skeptical" about Rust for STM32 firmware specifically; he believes the firmware for the STM32 (in IO board context) will remain C. Alexander defended Rust's cross-compilation capability ("it does intermediate compilation first, then targets any platform; you can write under any platform with Rust"), noting only minor performance trade-offs versus hand-tuned C. Pavel said the OS-level library layer could be rewritten in Rust, but resisted committing for STM32 firmware. Genadi resolved the timing question: the **FP7 product** in the near future will require swapping the IO board processor to a high-speed USB version because the current processor is becoming obsolete. That, Genadi argued, is the natural moment to reconsider the firmware language and bring in a younger engineer who routes via AI tooling. Val explicitly did not want Alekseev doing this work, not because of anything against him, but because Val wants the work driven by AI-augmented routing/firmware development, ideally with a 5-years-post-grad engineer.

The team then worked through the **GVL API** (the Java interface that JVL's application calls into). Alexander explained the pattern: a Java interface file lives in the Flex_Recycler repo with a stub implementation returning "not implemented" for every method. The interface declares methods like `dispenseBill`, `acceptBill`, `getStatus`, `loadCassette`. Tests can be written against the interface before any implementation exists. The interface cannot exist in a vacuum; it must live alongside an entry-point application, so the team will start by copying FlexPOS as a base. Pavel pushed back on the FlexPOS label, clarifying that the workflow being mirrored is FlexDispenser's, not FlexPOS's, since the customer/player flow is "almost one-for-one" with the dispenser, only the bill acceptor is replaced.

On hardware logistics, Val confirmed that **two recycler samples** were paid for (Genadi initially thought one). One unit is going to Georgia (Pavel/Alexander confirmed). The second should be shipped to **Minsk** so Alexander can perform the integration with the physical device. The team agreed real hardware is needed because, as Alexander noted from the dispenser experience, "many bugs are only found with the physical device that you simply can't see otherwise." Genadi estimates roughly five weeks from China to Belarus (three weeks China to Toronto + delivery onward). Val also noted that Chinese import taxes paid through intermediaries are non-recoverable.

The team established the immediate work plan around Pavel's vacation. Pavel's last working day is Thursday, April 30; Friday May 1 is Labor Day (holiday). Pavel and Alexander will spend tomorrow morning (April 29) building out a Jira sketch, described as roughly two weeks of described work for Alexander. A working meeting is scheduled at 10:00 AM Wednesday April 29 (Val + Pavel + Alexander) to walk through the Jira sketch and Pavel's Figma user-flow link. On Monday May 4 (with Pavel away), Val will meet with Alexander, Juan Martinez (Product Owner, to refine requirements per Bella since Juan's existing requirements are sparse), and Andrei Klimovich (a new Belarusian-origin engineer Val is bringing in to handle requirements work, a former Minsk resident with engineering education, currently working under Juan and being driven productive on this product).

Val explicitly stated that **unit tests are now largely obsolete** in the Claude Code era. Alexander affirmed that integration tests and acceptance tests are now where effort focuses, since Claude Code itself produces a great deal of working code. The infrastructure to be built must include CI/CD from day one alongside acceptance criteria definition, because as branches start landing into main, things will break unless tested.

On the UI side, the new platform is **slim with a vertical screen orientation**. Igor Gribko will need to redo the screens for the vertical layout, but Pavel cautioned it is premature to hand him work until requirements and constraints are documented. Alexander noted the existing FlexBox layouts may stretch acceptably to the vertical orientation in many cases. Some recycler-specific screens (configuration, registration, servicing, error display, error blocking, error storage) still need to be designed.

Andrei Bosik will build a "checker" for base metrics during this period, supporting the requirements-first workflow Alexander described: feed Claude requirements first, and code generation follows naturally.

## Decisions Made

- **Do not engage Evgeny Alekseev for the Recycler integration.** Reason: vendor supplies a 2025 Java library handling the protocol; no byte-level work needed. The remaining integration is in-house Java/UI work. (Decided by Val, supported by Pavel, Alexander, Genadi)
- **Architecture for Flex_Recycler mirrors existing kiosk stack:** Linux on RK3568 + Java backend + browser-based GUI. (Endorsed by Pavel, Alexander)
- **New repository for Flex_Recycler**, assembled from selected parts of FlexPay/FlexDispenser; do not fork. Use Claude Code to remove dead services/calls during assembly. (Decided by Val, agreed by Alexander, Pavel)
- **Reuse the gaming-machine IO Board with FRAM depopulated** (one chip kept, six removed), saving ~$30 per unit. Add LED controller functionality. (Decided by Val, proposed by Pavel + Genadi)
- **Defer firmware-language change** (C → Rust) for STM32 IO board firmware to the FP7 product window, when the board's processor needs swapping to high-speed USB anyway. (Decided by Val on Genadi's recommendation; Pavel skeptical of Rust on STM32 specifically)
- **Java interface (GVL API) lives in the Flex_Recycler repo**, with a stub implementation returning "not implemented" until filled in. Interface tests can be written before implementation. (Endorsed by Alexander, Pavel)
- **Ship one recycler sample to Minsk** for Alexander's physical-hardware integration testing.
- **Andrei Klimovich is the requirements lead** alongside Juan Martinez. (Decided by Val)
- **CI/CD and acceptance criteria are defined at infrastructure setup time**, not retrofitted. Integration and acceptance tests replace unit tests as the primary quality gate. (Decided by Val, agreed by Alexander)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel + Alexander | Build out the Jira sketch with ~2 weeks of described work for Alexander, including tasks for the GVL API design and recycler integration, plus requirements-discovery tasks | Apr 29, 2026 (morning) | High | Pavel leaves on vacation Apr 30 |
| 2 | Pavel | Send Alexander the Figma link showing the user-flow thinking for the recycler/dispenser screens | Apr 29, 2026 | Normal | Alexander needs this to scope screen work |
| 3 | Pavel | Attend 10:00 AM Apr 29 meeting with Val + Alexander to walk through the Jira sketch | Apr 29, 2026, 10:00 AM | High | Last sync before Pavel's vacation |
| 4 | Genadi | Arrange shipment of one recycler sample to Minsk for Alexander's integration work | Soon, ~5 weeks delivery | High | Alexander cannot do final integration without physical hardware |
| 5 | Pavel | Investigate the vendor's Java library; confirm coverage of deposit and dispense use cases and identify any gaps | After Apr 29 sketch session | Normal | Library is the keystone assumption that eliminated Alekseev's role |
| 6 | Alexander | Lead the build of the Flex_Recycler architecture: new repo, GVL API stub, CI/CD, acceptance criteria scaffolding; prep for hands-off Claude programming once requirements arrive | Ongoing | High | Core deliverable Val explicitly assigned at meeting close |
| 7 | Andrei Bosik | Build the "checker" for base metrics on the new architecture | Ongoing during recycler buildout | Normal | Supports requirements-first workflow |
| 8 | Val | Hold Monday May 4 meeting with Alexander, Juan Martinez, Andrei Klimovich, Irina Shishko (8:00 AM ET) to drill into requirements | May 4, 2026 | High | Primary requirements-gathering session |
| 9 | Juan Martinez | Prepare to expand requirements coverage; produce REQ + CAP entries in JIRA in advance of May 4 | May 4, 2026 | High | Alexander expects gaps in current requirements |
| 10 | Andrei Klimovich | Take first pass at personas, use cases, and JIRA REQ/CAP entries; 120% focus this week | May 4, 2026 | High | Val ramping Andrei as production requirements lead under Juan |
| 11 | Igor Gribko (deferred) | Redesign UI screens for vertical (slim) screen orientation; do not start until requirements are locked | TBD (after May 4 lock) | Low (deferred) | Layout follows use cases, not the other way around |

## Engineering Signals

### Confirmed Signals

- **ADR — Use vendor's 2025 Java library for recycler protocol; do not implement byte-level protocol in-house.**
- **ADR — Flex_Recycler architecture mirrors existing kiosk stack:** Linux on RK3568 + Java backend + browser GUI.
- **ADR — Build Flex_Recycler in a new repo by assembling parts from FlexPay/FlexDispenser, not by forking.**
- **ADR — Reuse the gaming-machine IO Board (with FRAM depopulated) instead of designing a new one.**
- **ADR — Java GVL API interface lives in the Flex_Recycler repo with stub implementation.**
- **REQ — Recycler must support both deposit (accept money) and dispense (return on ticket presentation).**
- **REQ — Vertical screen orientation on slim platform.**
- **CAP — Operator-facing capabilities required:** recycler configuration, registration, servicing, error display, error blocking, error storage.
- **Engineering Solution — Requirements-first development with Claude Code.**
- **Engineering Solution — Integration tests and acceptance tests replace unit tests as primary quality gate.**

### Suspected Signals

- **Possible ADR — Migrate firmware/library layers from C/C++ to Rust** (deferred to FP7 window).
- **Possible ADR — Hardware integration must be performed against physical device, not simulated.**
- **Possible CAP — Mock/stub layer for unavailable hardware.**
- **Possible REQ — JVL-specific GVL API abstraction layer over vendor library.**

## Open Questions

- Vendor Java library coverage gaps: does it cover all error scenarios, cassette management, and status reporting JVL needs? Investigation pending (Pavel).
- Existing Juan Martinez requirements completeness: Alexander expects gaps; May 4 working session to surface them.
- Vertical screen layout: whether existing FlexBox layouts will stretch acceptably or whether Igor Gribko needs a full redesign of every screen.
- FP7 IO board firmware language: the Rust-vs-C debate is deferred but not closed.
- Andrei Klimovich's onboarding pace.

---
*Processed from Teams transcript on 2026-04-29*
*Source meeting: Recycler Requirements, Scope, Acceptance*
