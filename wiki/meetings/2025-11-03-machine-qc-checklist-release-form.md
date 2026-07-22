---
type: meeting
title: Machine QC checklist & release form — closing the final-assembly gap (Nov 3 2025)
date: 2025-11-03
aliases: [machine QC checklist Nov 3, release form meeting, final machine checkup, Georgia production QC]
source-count: 1
open-commitments: 2
---

# Machine QC checklist & release form — closing the final-assembly gap (Nov 3 2025)

**Date:** 2025-11-03 (10:31 AM) · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/genadi-peari.md|Genadi Peari]], [[wiki/people/irina-shishko.md|Irina Shishko]]. Russian.

Val called this meeting after machines shipped to Georgia arrived with basic things unverified (loudspeakers not screwed into the cabinet), exposing that JVL has **no final whole-machine QC step / release form** now that manufacturing has moved from Toronto to Georgia. Substance on [[wiki/topics/slot-machine-production-test-procedure.md]] (Nov-3 section); ties to the manufacturing move ([[wiki/decisions/2025-06-24-move-manufacturing-from-canada-to-georgia.md]]) and the earlier final-assembled-sign-off ruling ([[wiki/decisions/2025-03-07-final-signoff-on-assembled-machines.md]]).

Durable points (single source):
- **What went wrong.** When tariffs on Canada loomed, JVL **mass-shipped 335 machines to Georgia** in varying states of readiness — some assembled in Toronto, some just parts loaded — "as fast as possible." On arrival, loudspeakers were found **not screwed into the machine**: the sub-assemblies were fine on the bench, but nothing caught it at the final machine. [[wiki/people/elizabeth.md|Elizabeth]] had personally checked the ~10 machines sent to one location (lights, screen, video), but the speakers sit hidden behind the front panel and no one thought to look.
- **The gap Genadi named.** Sub-assembly build instructions all exist on the server (Elizabeth works to them); what is **missing is a final full-machine checkup instruction** — power up, verify sound / that speakers don't rattle, touchscreen, all monitors, boot from auto, serial ports — "this is a hole we need to fill."
- **Port-testing tooling gap.** JVL used to test ~21–22 ports; the new machines have only **4 ports (2 SAS, printer, one extra)** and there is **no test tool** for them — a loopback test exists in principle (insert the loopback, press the port test, the signal loops back on transmit) but JVL has no diagnostic for SAS-2, so a dead second SAS could ship unnoticed.
- **Genadi's proposal: revive the per-machine QC checklist / release form.** A printed sheet that travels with each released machine, each item inspected and signed (touchscreens, speakers screwed, etc.) — JVL "used to do this" (a checklist went out with every machine). Val agreed the list should be part of the final tech inspection and go out with every machine, while noting even it might have missed this speaker case.
- **Root cause — lost tribal knowledge in the Toronto→Georgia handoff.** The late **Oleg (Hmyrov)** used to check every machine by hand; the assemblers he trained kept doing so, but no one trained **[[wiki/people/arkady-batson.md|Arkady]]**, who "never checks anything himself." Elizabeth — a degreed engineer who treats this as a career — approaches it seriously and is now preparing to **assemble 100 machines**.

Undertakings ([[wiki/topics/slot-machine-production-test-procedure.md#nov-3-2025--the-final-machine-qc-checklist--release-form-gap]]):
- Genadi + Irina to co-own a **circulating document** listing every missing step / document / instrument for reliable checks and reporting, laid out by process stage (during assembly / post-assembly / troubleshooting), each stage naming who does it and what tool is needed — so JVL can then decide what specialists and tools (via [[wiki/people/pavel.md|Pavel]]) are required.
- Genadi to **travel to Georgia (~2 weeks)** to work hands-on with Elizabeth on all problem sub-assemblies — after the ~Dec-20 release "tuning," so late Nov / early Dec; a work station to be prepared for him (Sergei to set up a computer), and he must cross the border **as a tourist** (no laptop/tools/equipment or he'll be stopped). JVL is closed Dec 22.

**§15.8:** no named-person compensation in this source — production-process content only.

## Sources

- [[raw/Machine Quality Control Checklist and a Release form.md]]
