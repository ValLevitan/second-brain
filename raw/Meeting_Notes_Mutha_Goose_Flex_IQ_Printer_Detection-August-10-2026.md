# Meeting Summary — Detecting the Mutha Goose–printer link under Flex-IQ (relay fix)

**Date:** August 10, 2026, 5:00 PM Eastern (Russian conversation, English rendering)
**Duration:** approximately 17 minutes
**Attendees:** Val Levitan and the engineering team (Genadi Peari and colleagues; a second voice, "Ben" in the raw diarization, is likely a mis-label). Outlook attendees for the paired event: Pavel Frolov, Val, Andrei Klimovich, Genadi Peari.
**Raw transcript:** [[Meeting_Transcript_Mutha_Goose_Flex_IQ_Printer_Detection-August-10-2026]]
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Calendar pairing:** Outlook event "Mutha Goose - Flex-IQ - Printer : detect connections", 5:00 PM ET, organiser Pavel Frolov. Confirmed by content.

## Summary

An engineering problem from the new wiring: JVL now connects the Mutha Goose device in parallel with the printer, instead of chaining through Flex-IQ and the printer. Because the Mutha Goose is a standalone device, JVL cannot reliably tell when it is connected — it only catches signals. On a power loss the Mutha Goose boots much faster than Flex-IQ, so it sends the printer a signal and a small ticket prints before Flex-IQ is up to catch it. There is no reliable way to detect the connection short of turning the motor off and on again — fine for a trade-show demo (just restart it), but not for long-term field use.

The proposed fix: connect with two cables in a **split, not parallel** arrangement, using **relays** on the three lines. While Flex-IQ is not loaded, the relays pass the signal straight through to the printer (so it behaves as if Flex-IQ is not there). Once the application loads, JVL sends a signal, the relays switch the lines over, and Flex-IQ takes control — it can then print the tickets it currently cannot, capture packets off the network, and reconnect cleanly after a dropped connection. The team accepted this as the direction; the practical hurdle is process time (convening, sign-off) — roughly a month before it reaches them, which was deemed acceptable.

The tail of the recording drifts into a separate operational thread about connecting to a location/operator and signing directly with an operator who does not want to sign anything — Val insisting on a direct contract with JVL rather than depending on the operator, and a plan to call Philip about what is needed from the "masters" to get a certificate before signing anything.

## Decisions Made
- Adopt the **relay-based split-line design** to detect and control the Mutha Goose–printer link under Flex-IQ. (Val + engineering)
- Demo/exhibition use can rely on a simple restart; the relay fix is for long-term field reliability.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Engineering | Build and test the relay split-line approach on Flex-IQ | ~1 month | Normal | Reliable detection without motor restart |
| 2 | Val / team | Call Philip re: what the operator/"masters" need to issue the certificate before any contract | Days | Normal | Certificate gates the deal |

## Possible mis-transcriptions
- "mutabus" / "Mutha Goose" — the Mutha Goose device; "FlexIO / LexisNexis / FlexiQ / flexi" — **Flex-IQ**; "FPE" — unclear; "IKEA" — unclear (garble). "Ben" — likely a mis-labelled speaker.

## Dispatch Log

---
*Processed from Plaud recording on September 25, 2026 (backlog batch 7). Source: 08-10 Relay-Based Printer Fix (Plaud).*
