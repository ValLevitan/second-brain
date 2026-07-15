---
tags:
  - SMIB
  - TITO
  - protocol
  - technical
  - hardware
  - flex-pay
---

# SMIB and FlexPay Integration Meeting Summary
**Date: April 2, 2025**

## Overview
This meeting focused on discussing the technical requirements and implementation strategies for developing a SMIB (Slot Machine Interface Board) solution that would enable TITO (Ticket In, Ticket Out) functionality across both modern and legacy gaming machines. The team explored various technical approaches, connectivity options, and hardware considerations.

## Key Discussion Points

### Protocol Considerations
- G2S protocol was discussed but deemed not viable as it requires GSA membership
- SAS protocol (version 603) was identified as the preferred communication protocol
- The team has access to SAS 603 documentation and the differences between 602 and 603 versions

### SMIB Hardware Requirements
- Two scenarios were discussed:
  1. Modern machines with two SAS ports: SMIB would connect to the secondary SAS port
  2. Legacy machines with only one SAS port: Would require a Y-splitter solution or pulse monitoring

- For legacy machines, the SMIB would need:
  - Connector for printer
  - Connector for bill acceptor
  - Connector for GLC primary SAS output
  - Network connector for WSS protocol to communicate with FlexPay

- Display considerations:
  - Permanent display not necessary for basic SMIB functionality
  - Setup could be done via external portable device or through FlexPay
  - For legacy machines with limited error handling, a display might be necessary

### Implementation Approaches
- Two firmware versions could be supported on FlexPort devices:
  1. For older machines: Emulate bill acceptor and use pulses
  2. For newer machines: Work exclusively with SAS

- FlexPay would support both types of SMIB boards simultaneously in a single location

### QR Code vs. TITO Solution
- The team compared their existing QR code solution with the proposed TITO implementation
- QR solution offers cost savings on printer hardware and ticket paper
- TITO solution provides a more familiar experience for players

### Concerns and Challenges
- Physical installation of printers in legacy machines that weren't designed for them
- Power supply considerations for the SMIB board
- Error handling on legacy machines without built-in printer support
- Asset number verification between SMIB and GLC
- Market readiness and operator interest in kiosk solutions

## Business Considerations
- The team noted a lack of urgency from operators to purchase kiosks
- Speculation that operators may be developing alternative approaches to comply with legislation
- Need to consult with Income to understand market dynamics and regulatory interpretations
