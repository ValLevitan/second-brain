---
tags:
  - E-Wallet
  - FlexPay
  - action-plan
  - strategy
  - technical
  - github
---

# E-Wallet/FlexPay Implementation Summary & Action Plan
*Based on May 29, 2025 Meeting - For June 2, 2025 Review*

## Key Achievements Since Last Meeting

### Evgeny Yavorski (E-Wallet/FlexPort Development)
**Completed:**
- Money in/money out functionality tested and update sent to Minsk (May 20)
- Identified and documented specific fixes needed post-testing

**In Progress:**
- Fixing credit field issue (switching from 'amount' to 'minor units' field)
- Replacing device number stub with real SAS protocol response
- Command logging implementation (60 bytes for TITO, working with real data from Alexeev)

### Evgeny Alexeev (Hardware/Firmware)
**Completed:**
- USB implementation Phase 2: file encoding, memory writing, integrity verification, firmware transition
- SAS command packet preparation (60-byte format for WSS transmission)
- LED status documentation uploaded to GitHub (May 21)
- Received 10 SMIB boards (May 26)

**In Progress:**
- Testing and porting software to cost-optimized processor (fewer pins)
- Creating new firmware project for production SMIB boards

### Dmitry Chudinov (FlexPay Backend)
**Completed:**
- Partial redemption implementation and API provision for Igor Khrebkov
- Feature sent for beta testing

**Critical Issue Resolved:**
- Packet size reduced from 64KB to 8KB to prevent system freezing during E-Wallet updates

### Pavel Frolov (Infrastructure)
**Completed:**
- GitHub repositories established for SMIB and FlexPort
- Access and permissions configured

**Pending:**
- FlexPay migration from Bitbucket to GitHub (moved from June 15 to June 7 target)
- CI/CD pipeline setup requiring coordination with Chudinov

## Critical Technical Decisions Made

### Architecture Clarification
- **TITO Architecture**: Used for SMIB boards, simpler logging (60 bytes)
- **E-Wallet Architecture**: More complex, requires firmware updates via WSS protocol

### Packet Size Optimization
- **Problem**: 64KB packets caused system freezing
- **Solution**: Reduced to 8KB packets for stable transmission
- **Impact**: Requires protocol modifications but eliminates stability issues

## Action Items for Today's Review

### High Priority (Weekend/Immediate)

#### Evgeny Yavorski
- [ ] **Due: Sunday Evening** - Deliver E-Wallet update with 8KB packet support
- [ ] Complete real SAS protocol device number implementation
- [ ] Finalize command logging with real data (not stubs)
- [ ] Test negative scenarios that previously failed

#### Dmitry Chudinov  
- [ ] **Due: ASAP** - Modify packet transmission from 64KB to 8KB
- [ ] Implement sequential 8KB packet transmission with acknowledgments
- [ ] Coordinate with Yavorski for testing protocol
- [ ] Ensure version excludes card dispenser and validator for testing

#### Evgeny Alexeev
- [ ] **Due: Sunday** - Complete firmware port to cost-optimized SMIB boards
- [ ] Test and validate 10 production boards received
- [ ] Fix any hardware routing issues discovered
- [ ] Document any problems found with board layout

### Medium Priority (This Week)

#### Pavel Frolov
- [ ] Complete FlexPay migration to GitHub by June 7
- [ ] Set up CI/CD pipelines for all repositories
- [ ] Ensure all documentation is in Markdown format in repositories
- [ ] Convert PDF documentation to Markdown (offered converter tool)

#### Documentation & Version Control
- [ ] Establish clear versioning scheme (version.subversion format)
- [ ] Separate test and production folders in repositories
- [ ] Implement proper build numbering system
- [ ] All team members to use GitHub repositories for documentation

### Planning Items (Next Phase)

#### Genadi Peari
- [ ] Wait for Alexeev availability to discuss future hardware platforms
- [ ] Plan FlexTower and POS next steps
- [ ] Evaluate FlexPort platform updates vs. new development

#### System Architecture
- [ ] Plan full SAS protocol implementation for future versions
- [ ] Ensure current architecture supports full protocol when needed
- [ ] Verify bandwidth and timing requirements for full implementation

## Key Questions for Today's Meeting

1. **Testing Status**: Did weekend work proceed as planned?
2. **8KB Implementation**: Is the packet size change working correctly?
3. **Hardware Validation**: Any issues found with the 10 SMIB boards?
4. **Integration Testing**: Are Yavorski and Chudinov's components working together?
5. **Timeline Adherence**: Are we on track for planned deliverables?

## Technical Dependencies

- **Yavorski** depends on **Chudinov's** 8KB packet implementation
- **Alexeev** working independently on hardware/firmware port
- **Frolov** needs **Chudinov** coordination for CI/CD setup
- All development should use GitHub repositories for version control

## Next Meeting
**Scheduled**: Monday, June 2, 2025 at 7:00 AM

---
*Meeting attendees: Irina Shishko, Dmitry Chudinov, Pavel Frolov, Evgeny Alexeev, Evgeny Yavorski, Genadi Peari*