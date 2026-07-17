---
tags:
  - e-wallet
  - release-planning
  - flexport-flexpay
  - planning
  - technical
  - github
---

# E-Wallet Architecture Release Planning Meeting Summary
**Date:** May 27, 2025  
**Duration:** 30:54  
**Project:** FlexPort and FlexPay E-Wallet Architecture Release

## Executive Summary
This was a critical planning meeting for releasing the e-wallet payment architecture for FlexPort and FlexPay systems. The team faces a hard deadline of November 2025, with the project leader emphasizing that missing this deadline would mean complete failure of 1.5 years of work. The meeting focused on defining a minimal viable product (MVP) approach to ensure timely delivery.

## Technical Architecture Overview

### E-Wallet System Components
- **FlexPort**: Device installed in gaming machines' bill acceptor slot (no SAS protocol)
- **FlexPay**: Kiosk system that communicates with FlexPort over network
- **Communication Protocol**: WSS (WebSocket)
- **Key Functions**: Temporary wallet creation, money transactions, card issuance

### Current Implementation Status

#### ✅ Completed Features
- Money transactions to Temporary Wallet (FlexPort side)
- Money transactions to Temporary Wallet (FlexPay side)
- Money acceptance functionality
- Temporary Wallet issuance calculation
- Temporary Wallet validation
- InComm card issuance data generation
- USB firmware update capability

#### ❌ Pending Features
- Firmware Update support on FlexPort
- Logging from FlexPort to FlexPay
- Full TITO functionality with complete SAS implementation
- Support for additional bill validators (currently only JCM UBA)

## Critical Decisions Made

1. **Version Control**: Freeze version 17b as final release with proper naming convention
2. **Feature Scope**: Focus on MVP features only for Georgia QAM market
3. **Bill Validators**: Use only JCM UBA validators for initial release
4. **Repository Migration**: Move from Bitbucket to GitHub within 1 week
5. **Testing Approach**: Two-phase testing (debug and production environments)
6. **Meeting Cadence**: Increase to twice-weekly meetings due to critical timeline

## Action Items

### Immediate Actions (This Week)

| Task | Owner | Due Date | Status |
|------|-------|----------|--------|
| Complete partial redemption feature | Dmitry Chudinov | May 28, 2025 | In Progress |
| Implement proper version naming (stop using "17b") | Evgeny's team | Immediate | Pending |
| Coordinate InComm in-house test setup | Pavel Frolov (via Juan) | This week | High Priority |
| Send updated card requests to InComm | Pavel Frolov | Already sent | Completed |

### Short-term Actions (1 Week)

| Task | Owner | Timeline | Dependencies |
|------|-------|----------|--------------|
| Develop comprehensive test suites | Irina Shishko / QA Team | 1 week | Final FlexPay version |
| Migrate repositories to GitHub | Pavel's team | 1 week | - |
| Create release images with versioning | Pavel's team | 1 week | GitHub migration |
| Implement ticket report functionality | Tim/Dmitry | 1 week | - |
| Prepare test procedure documentation | Irina Shishko | 1 week | - |

### Hardware Preparation

| Item | Quantity | Specifications | Responsible |
|------|----------|----------------|-------------|
| FlexPay Units | 2 | Complete configuration with UBA validator, scanner, printer, Linetech card dispenser | Gennady |
| FlexPort Units | 5 | 3 active (2 non-JVL brands, 1 JVL), 2 spares | Gennady |
| Brackets & Harnesses | As needed | Specific types TBD | Gennady |
| InComm Cards | TBD | Both debug and production types | Via Juan |

## Testing Strategy

### Phase 1: Debug Environment
- Use resettable debug cards from InComm
- Test core functionality and transaction flows
- Identify and fix critical issues

### Phase 2: Production Environment
- Use production cards from InComm
- Full financial cycle verification
- Validate money flow through InComm Bank and JVL Bank
- Complete end-to-end testing

### Test Coverage
- Positive and negative test cases
- Money deposit to Temporary Wallet
- Temporary Wallet issuance and redemption
- Partial redemption functionality
- Card issuance procedures
- Complete financial transaction flow

### Timeline
- Maximum 1 month for complete testing cycle
- Parallel testing in Minsk (JVL) and Georgia (Philip's office)

## Risk Management

### Identified Risks
1. **Market Viability**: E-wallet architecture may not be long-term solution
2. **Timeline Pressure**: November 2025 deadline is non-negotiable
3. **Integration Complexity**: InComm integration requires special permissions
4. **Hardware Availability**: All equipment must be ready before testing

### Mitigation Strategies
- Financial transaction cycle will be reusable for future TITO implementation
- MVP approach to reduce scope and complexity
- Proactive communication with InComm through established contacts
- Spare hardware units to prevent testing delays

## Critical Success Factors

1. **Proactive Communication**: Maintain close coordination with Juan for InComm integration
2. **Version Control**: Implement proper release management immediately
3. **Scope Management**: Resist feature creep; focus on MVP only
4. **Testing Discipline**: Follow structured test procedures and documentation
5. **Clear Ownership**: Each deliverable has single responsible owner

## Next Steps

1. All team members to proceed with assigned action items
2. Pavel Frolov to maintain daily communication with Juan
3. QA team to begin test case documentation immediately
4. Hardware team to prepare shipment list for Georgia
5. Next meeting scheduled for Thursday (2 days) to review progress

## Notes

- The e-wallet architecture is acknowledged as potentially short-lived in the market
- However, the payment processing infrastructure being built will support future TITO architecture
- Georgia location has been approved by InComm for special in-house testing (unusual permission)
- All development must be committed to repositories going forward (no more informal version sharing)

---
*Meeting Transcript Available: release_e-wallet_flex-pay_flex-port-may-27-2025.md*
