# Meeting Summary — Val/Juan Alignment (Flex S Cabinet Direction + Georgia RIS Issue)
**Date:** April 21, 2026, 9:29 PM Eastern
**Duration:** ~13 minutes 45 seconds
**Attendees:** Val Levitan, Juan Martinez (Inna Levitan briefly at end)

## Summary

A short evening alignment between Val and Juan covering two distinct subjects: the unresolved Georgia serial-number / RIS issue, and Val's redirection of the recently-developed Flex C cabinet design toward becoming the next evolution of Flex S.

### Georgia serial-number issue (parked)

Juan reported that the recent serial-number cleanup at the Georgia operation appears to have worked for most machines but left at least one machine that still won't connect. The site uses multiple devices and a single shared generic CMS login, which prevents tracing the issue to a specific employee or device. Elizabeth (on the customer side) ran two test sessions earlier in the prior week that Irina confirmed were OK. As an interim measure, the operator will use a tablet only — not anyone's phone — to remove device variability. Juan plans a follow-up conversation with Minsk when they're back to dig into the cause.

The team currently knows that one of the ten machines in the latest batch failed to connect after the swap; the other nine have not been individually verified. When the previous batch had the same issue, Juan rebuilt the RIS, and that batch then ran flawlessly. Juan asked Minsk whether the serial can be wiped clean from the failing machine and rebuilt from scratch; reply expected the next day.

Val pushed back on the workaround approach — moving on to the next machine each time without isolating the cause is not a solution. He explicitly asked Juan to keep the failing serial in place for diagnostic purposes rather than erase it, so the team can find a reproducible repro and root-cause it. Val also speculated that an environmental change might be relevant: Canadian sites are predominantly iPhone-based, while Georgia is predominantly Android, which could affect QR-code handling. He also flagged that he doesn't know whether JVL uses a standard QR code from a specific tool or a generic one. Val handed full ownership back to Juan and parked the topic.

### Flex C → Flex S evolution (the real subject)

Val announced he is redirecting the Flex C cabinet design that the team recently developed. Because JVL is not currently focused on the casino market, Val no longer considers the design "good enough for Flex C" but believes it is good enough as the next-revision Flex S. The intent is to use it as an "evolution of design" for Flex S rather than holding it for a future Flex C launch.

The redirected cabinet will incorporate the new CPU, an embedded mobile/cellular modem, GPS, and OMNI 2. **OMNI 1 has been scrapped** — Val said explicitly he is not going forward with it and is moving directly to OMNI 2.

Aesthetic direction: move away from chrome to brushed aluminum and gunmetal. Val wants to push for "bleeding edge" on the V-deck, find a screen for it, and produce considerably thinner monitor edges so the monitors look like bleeding-edge displays. Open question on perimeter lights — possibly cheap, possibly antiquated.

Juan added a market-driven preference: customers (excluding Light & Wonder) increasingly want main monitors that physically touch between adjacent machines to create a video-wall / seamless transition look. Today the V-deck is wider than the monitor and prevents the touch. Two ways to enable it: larger monitors, or a smaller V-deck. Val noted that if the V-deck "bleeds" on the edges, the same nominal V-deck size could shrink in apparent footprint.

Slim buttons: Juan said keeping the slim buttons is very important. The pain point: replacing one currently requires disassembling the V-deck because the button can't be removed from the top (per Sebastian and Denis — Juan flagged he wants to confirm). Val raised the option of integrating the button into the glass with a custom glass piece, but acknowledged that would be unnecessarily expensive. Juan's preference is an easy user-replaceable button — replaceable from the top. Val asked whether Juan would prefer a smaller V-deck; Juan said "a couple of inches" and noted that even tightening the current design's spacing toward the V-deck might accomplish the same monitor-touch goal without changing V-deck size.

### Plan and tempo

Val directed Juan to take a week to re-discover/revisit the requirements for this new cabinet, then start a regular meeting cadence on the subject. Target: have the cabinet come together by **March 2027 for the AMOA show**. Val expects JVL to have "a killer show" by then — Texas, Nebraska, Georgia operations all running, a strong skill-game product line, and transactional equipment, alongside the new cabinet.

Val told Juan to start engaging Andrei on this — Andrei is "a good asset" but needs to accelerate; "too much philosophy" was the explicit complaint. Both agreed the business cannot operate at that pace.

Genadi is going full-force on Flex Slim this week and needs uninterrupted focus. After this week, the Flex S requirements re-discovery begins with regular meetings.

### Closing items (Juan)

Juan recapped a pending operational item: Denis has to drive back to Rapid City to reload the RIS that changed after DEMA found the bad serial number. MG Oil cannot install the Rapid City games yet, but they're starting on the Aberdeen units. Juan plans to push by Friday for payment on the shipment that's already ready. Val approved.

## Decisions Made

- **Repurpose the recently-developed Flex C cabinet design as the next evolution of Flex S** — JVL is not focused on casinos right now, and the design isn't strong enough to launch as Flex C anyway. (Decided by Val.)
- **Scrap OMNI 1; go directly to OMNI 2** for the new cabinet platform. (Decided by Val.)
- **Aesthetic direction: brushed aluminum and gunmetal**, away from chrome; pursue bleeding-edge V-deck and thin-bezel monitors. (Decided by Val.)
- **Park the Georgia single-serial RIS failure** as Juan's responsibility — keep the failing serial in place for diagnostics rather than erasing it; do not adopt the "swap to next machine" workaround as a solution. (Decided by Val.)
- **One week of uninterrupted focus for Genadi on Flex Slim**, then begin Flex S requirements re-discovery with a regular meeting cadence. (Decided by Val.)
- **Target AMOA March 2027** as the showcase event for the new cabinet alongside Texas/Nebraska/Georgia, the skill-game line, and transactional equipment. (Decided by Val.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Juan Martinez | Have a follow-up conversation with Minsk on the Georgia single-serial failure to understand what changed and find a reproducible repro; keep the failing serial in place rather than erasing it | This week | High | Val rejected the "move to next machine" workaround; needs root cause |
| 2 | Juan Martinez | Confirm with Sebastian and Denis whether the slim button truly can't be removed from the V-deck top (vs needs full V-deck disassembly) | TBD | Normal | Drives decision on replaceable-button design path |
| 3 | Juan Martinez | Re-discover/revisit cabinet requirements for the next-revision Flex S based on the Flex C design as starting point | One week (by ~April 28, 2026) | High | Gates the start of regular Flex S design meetings |
| 4 | Juan Martinez | Start engaging Andrei on the Flex S re-discovery work; push him to accelerate (less philosophy) | Once requirements re-discovery starts | Normal | Andrei is an asset but tempo needs to match the business |
| 5 | Juan Martinez | Push MG Oil for payment on the shipment that's ready, by Friday | Friday April 24, 2026 | Normal | Ready-to-ship hardware sitting on AR |
| 6 | Denis (via Juan) | Drive back to Rapid City to reload RIS post-DEMA serial cleanup | This week | High | Unblocks MG Oil's Rapid City installation |
| 7 | Val Levitan | Find a screen suitable for "bleeding edge" V-deck on the new cabinet | TBD | Normal | Aesthetic / industrial-design direction for the new cabinet |

## Engineering Signals

### Confirmed Signals

- **CAP — Cellular modem with GPS for the next Flex S cabinet:** Val confirmed the new cabinet platform will integrate a cellular phone module and GPS alongside the new CPU and OMNI 2. This aligns with the existing requirement document `Products/Flex-Pay and Port/cell_GPS_capability-March-2-2026.docx` (cellular modem with battery-backed GPS/IMU for Flex-Pay and Flex-S).
- **ADR — OMNI 1 deprecated; OMNI 2 is the platform forward:** Val: *"I scrapped only one, it's I'm not gonna go with it... So we, I'm moving it to only two."* Architectural decision affecting all new cabinet work.
- **ADR — Flex C cabinet design repurposed as Flex S evolution:** *"We created Flex C, but I don't think it's good enough for Flex-C. But I think it's good enough for a next revision of Flex S. ... we should use this design for Flex S."* Strategic/architectural redirection of an in-flight design effort, driven by JVL's current non-casino focus.

### Suspected Signals

- **Possible REQ — Adjacent monitors must physically touch (video-wall look):** Juan: *"the preference would be if the machines, the main monitors could actually touch... that's what prevents the machines from actually touching today, is the V deck is wider than the monitor."* Customer/market-driven requirement on the new cabinet form factor — does this warrant a formal requirement? *(Val — REQ candidate?)*
- **Possible REQ — User-replaceable slim button from top of V-deck:** Juan: *"the preference would be an easy user replaceable button. Right now, replacing that button is a big pain... you've got to disassemble a V-deck."* Service / serviceability requirement. *(Val — REQ candidate?)*
- **Possible CAP — Bleeding-edge V-deck screen + thin monitor bezels:** Aesthetic / industrial-design capability, not yet a hard requirement. *(Val — CAP candidate or just a design north star?)*

## Open Questions

- What changed in Georgia between the prior serial cleanup (which worked flawlessly) and this latest batch where one machine still fails? Hypothesis raised: device platform difference (Android-heavy in Georgia vs iPhone-heavy in Canada) and/or QR code source (standard tool vs generic). Juan to investigate with Minsk.
- Does JVL currently use a standard QR code generated from a specific tool, or a generic one? (Raised by Val; not answered.)
- Perimeter lights on the new monitors — keep (cheap) or drop (looks antiquated)? Open.
- Is the slim button genuinely unable to be removed from the top, or is that a misunderstanding? Juan to confirm with Sebastian and Denis.
- Should the V-deck shrink (a couple of inches) or should the monitors grow, to enable adjacent-monitor touching? Both options on the table.

---
*Processed from Teams transcript on 2026-04-25*
*Source meeting: Alignment-April-21-2026 (Teams recording)*
*Stale-meeting processing — no email drafts, no calendar reminders, no follow-up actions dispatched per Val's standing feedback (Apr 21 → Apr 25 = 4 days).*
