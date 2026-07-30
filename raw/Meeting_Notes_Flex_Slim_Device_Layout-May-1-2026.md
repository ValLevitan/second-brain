# Meeting Summary — Flex-Slim Device Layout
**Date:** May 1, 2026, 2:01 PM Eastern
**Duration:** ~43 minutes
**Attendees:** Val Levitan, Genadi Peari (industrial design), Andrei Klimovich (ergonomics / external commenter)

## Summary

This was a working session to finalize the front-panel device layout for the **Flex-Slim paystation** — a new slim-form-factor variant of JVL's existing paystation. The slim is roughly 11.5" wide (just under a foot), built around a single full-width touchscreen, with all customer-facing devices stacked vertically on the front: scanner, ticket printer, and bill validator/recycler. Genadi opened the call asking for a decision on the stack order so he could finalize internal mounting brackets — the geometry of every internal mechanism depends on which device sits where.

**Initial proposal vs. ergonomic challenge.** Genadi had been mocking up: printer on top, scanner under it, bill validator/recycler at the bottom — mirroring how competitors arrange "non-slim" kiosks. Andrei pushed back on first principles: the most-frequent and most-critical customer actions are (1) inserting cash into the bill validator/recycler and (2) scanning a QR code. Both must be at a height comfortable for an average ~1.75–1.78 m adult, without bending over. Receiving a ticket from the printer is a third-priority action — the customer will tolerate it being slightly inconvenient. Andrei said he didn't have hard numbers yet but the principle was firm: don't make people bend.

**Stack order — decided.** After working through it, the group agreed the recycler/bill validator must be lifted as high as possible (to the upper-middle area where the hand naturally rests), with the **scanner above it at the very top**, and the **printer mounted between** them — pushed up as high as the printer geometry allows. Genadi noted the printer has the largest physical envelope and slides out forward to allow paper reloading, so it dictates a lot of the stack. Competitors don't sell "slim" kiosks of this type — slim payment kiosks are a JVL-specific play; existing slim references (e.g., BallyVile's Sailbar) keep printer-on-top because they don't include a scanner.

**Width and dispenser constraint.** Total slim width is 11.5" (~12 cm internal printer width, ~6"). The group confirmed that **two cash dispensers will not fit** in this form factor — would require roughly 18" wide, which negates the "slim" concept. Val ruled that two-dispenser configurations stay on the existing full-size paystation. The slim variant is single-dispenser only.

**Profile aesthetics — speed-to-market wins.** Val voiced that he doesn't like the side profile of the current design (rear hump from the printer depth). Andrei pointed out that in real deployment the unit will almost always be sandwiched between adjacent machines, so the profile is mostly invisible. Val acknowledged this ("I'm an only child, I'm selfish, only I matter") but then reversed himself and explicitly endorsed shipping with the current profile: **using the existing paystation screen-angle molds saves ~2 months on speed-to-market**, and "we can always make another model." He noted JVL has built-in differentiation that's still visible head-on regardless of profile: full-width edge-to-edge touchscreen, and **programmable RGB GoFlash light bands** along the product perimeter that can run any light choreography even when units are side-by-side.

**Screen and glass construction.** Val drilled into how the top-front bezel meets the touchscreen. Genadi confirmed it's a single-piece molded top (one piece, no seam at the back/top junction) with Gorilla glass mounted on a recessed plastic shelf via double-sided tape. The plastic recess is field-replaceable — if the glass gets scratched, the entire plastic+glass sub-assembly comes off and a fresh one drops in. The touchscreen below is decoupled (no optical bonding), so the LCD itself stays put. Val noted this is commercially attractive: JVL can sell replacement bezel-glass kits "for pennies" and make margin on the swap.

**Water/spill drainage — open issue.** Val raised that customers will inevitably spill water or Coke onto the top surface where the recessed glass sits. The perimeter seam between the recess and the housing currently has no drainage. Genadi confirmed there's no drain channel yet; he'll add one and route the runoff somewhere (destination TBD — he hasn't designed it).

**Recycler compatibility — open.** Val flagged that the slim must accept multiple recycler models — not just GSM, but also MEI. MEI's bill path goes downward while GSM's runs flat with a stacker on top, meaning the layout must reserve clearance above the recycler for either profile. Genadi will verify the GSM fits the new arrangement and confirm the MEI clearance.

**Side hinging direction.** Genadi showed the cabinet door hinging; Val initially questioned the swing direction, but Genadi argued most users are right-handed and the current swing works. No change required.

**Closing.** Andrei asked Genadi to send him exact floor-to-device heights (floor → bill validator, floor → scanner) once he sketches the new layout, posted to the meeting's Teams chat. Andrei will independently research ergonomic best practices for average-human standing reach and post that back to the same chat. They'll review the next iteration together. Andrei attempted to start an annotation session at the very end to suggest a profile tweak; Val cut him off ("don't waste time on this") and ended the call.

## Decisions Made

- **Flex-Slim front-panel stack order:** Scanner at top → Printer in middle → Bill validator/recycler raised as high as possible. Final. (Decided by Val, with Genadi and Andrei in agreement.)
- **Reuse existing paystation screen-angle molds** for the Flex-Slim rather than designing a new screen angle. Rationale: ~2 months faster to market. Val explicit. (Decided by Val.)
- **Single dispenser only for Flex-Slim.** Two-dispenser configurations remain on the full-size paystation. (Decided by Val.)
- **Touchscreen bezel-glass sub-assembly stays field-replaceable** (double-sided tape mount, no optical bonding). Profitable as a service/replacement SKU. (Endorsed by Val.)
- **Profile aesthetics are deprioritized vs. ship date.** Acceptable to ship current profile; redesign can come in a future model. (Decided by Val.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi Peari | Mock up the new device stack (scanner top / printer middle / bill validator raised) and post floor-to-bill-validator and floor-to-scanner heights to the meeting's Teams chat for Andrei | TBD (next iteration) | High | Blocks internal bracket design and printer mounting; whole design waits on this layout |
| 2 | Genadi Peari | Verify GSM and MEI cash recyclers both fit the new vertical layout — MEI goes down while GSM has top stack; ensure clearance above the recycler accommodates both | TBD | High | Recycler compatibility is a hard product requirement; wrong-sized clearance forces a respin |
| 3 | Genadi Peari | Design a water/liquid drainage channel along the perimeter where the recessed glass meets the top housing; decide where runoff exits | TBD | Normal | Customers will spill drinks on the top surface — Val explicitly flagged this; must be addressed before tooling |
| 4 | Andrei Klimovich | Research ergonomic best practices for device heights based on average-human standing reach (1.75–1.78 m baseline) and post findings to the meeting's Teams chat | TBD | Normal | Validates the proposed stack heights before Genadi commits to brackets |
| 5 | Genadi Peari & Andrei Klimovich | Re-review the proposed layout together once Genadi posts heights and Andrei posts ergonomic norms | TBD | Normal | Closes the loop on stack-order decision before fabrication |

## Engineering Signals

### Confirmed Signals

- **ADR — Flex-Slim front-panel stack order (top-to-bottom: scanner / printer / bill validator-recycler):** Departs from competitor convention (printer-on-top) because the slim form factor newly includes a scanner; the bill validator must be at a comfortable hand-height per ergonomic priority. Decided in-meeting.
- **ADR — Reuse existing paystation screen-angle molds for Flex-Slim:** Trade-off explicitly weighed (~2 months speed-to-market vs. accepting a side-profile Val finds aesthetically suboptimal). Speed wins. Val: "We can always make another model."
- **REQ — Flex-Slim maximum width <12" (~11.5"):** Defines the "slim" form factor; any wider variant rolls back to existing paystation.
- **REQ — Flex-Slim supports single cash dispenser only:** Two-dispenser configurations route to existing full-size paystation.
- **REQ — Flex-Slim recycler bay must accept both MEI (downward feed) and GSM (flat feed + top stacker):** Customer-side-agnostic cash hardware support.
- **CAP — Programmable RGB GoFlash perimeter light bands on Flex-Slim:** Differentiator visible even when units are sandwiched; supports arbitrary light choreography (addressable LEDs implied).
- **Engineering solution — Field-replaceable touchscreen bezel-glass sub-assembly:** Plastic recess + Gorilla glass bonded by double-sided tape, no optical bonding on the LCD. Enables cheap replacement SKU; LCD survives glass damage. Val noted the margin opportunity on aftermarket bezel kits.

### Suspected Signals

- **Possible REQ — Top-surface liquid drainage channel:** Val raised the spill scenario forcefully ("they'll spill Coke 100%"); Genadi accepted the action item. May warrant a formal requirement entry rather than living only as an action item.
- **Possible ADR — Cabinet door hinge direction (right-side swing for right-handed users):** Briefly debated and resolved in-meeting; arguably worth recording as a deliberate decision rather than letting it sit only in the transcript.

## Open Questions

- Where does the perimeter-drain runoff exit the cabinet? (Genadi has not designed the routing.)
- What are the actual proposed heights (floor-to-bill-validator, floor-to-scanner) in the new layout? (Genadi to measure and post.)
- What is the ergonomic-norm height range that Andrei will recommend? (Pending his research.)

---
*Processed from Teams transcript on May 24, 2026*
*Source meeting: Flex-Slim_devices-May-1-2026 (Teams recording)*
