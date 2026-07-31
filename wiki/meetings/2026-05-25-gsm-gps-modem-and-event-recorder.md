---
type: meeting
title: GSM/GPS Modem and Event Recorder (May 25 2026)
date: 2026-05-25
aliases: [GSM GPS modem, LTE modem, cellular modem with GPS, event recorder, black box, machine telemetry, remote connectivity, SIM per machine, FRAM event log]
source-count: 1
---

# GSM/GPS Modem and Event Recorder (May 25 2026)

**Date:** 25 May 2026, 3:30 PM Eastern (§11 recording-header time; the filename stamp `_113031` is UTC ~4h behind — header ET wins). ~43m; Russian (RU/EN garbled transcript).
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/genadi-peari.md|Genadi Peari]].

An exploratory hardware/telemetry planning call on two components for the Flex devices and machines: (1) a **GSM/GPS/LTE modem** for remote connectivity and location, and (2) an **event recorder** ("black box") that captures machine events up to a crash for later diagnosis. Val opened it as a "play ping-pong" session to get to one direction because "everything is up in the air"; no decisions were reached — the call ended on research assignments. This follows the open Flex-Recycler hardware question (a cellular modem with GPS — feasibility + available modules) parked on [[wiki/topics/flexpay-business-architecture-payout-devices.md]], and sits on the ARM/Linux board platform decided in [[wiki/decisions/2025-05-26-arm-linux-platform-flex-devices.md]] (the modem/storage form-factors debated here — motherboard slot vs USB vs PCIe vs SATA — are that board's interfaces).

Substance — the LTE-modem cost/coverage picture (~$10 hardware, ~200 MB/month, cell-tower positioning vs a GPS antenna), the SIM-per-machine vs one-account-per-bank tradeoff, antenna routing out of metal enclosures, the always-on-when-powered-off limit, and the event-recorder feasibility (why a truly external black box duplicates the machine; the FRAM/battery-RAM/SSD storage options; and that GSM largely solves the log-delivery gap) — lives on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (May-25 2026 section). §15.8: hardware/telemetry/carrier-cost economics only; no named-person compensation.

## Sources
- [[raw/Meeting_Transcript_GSM_GPS_Modem_and_Event_Recorder-May-25-2026.md]]
