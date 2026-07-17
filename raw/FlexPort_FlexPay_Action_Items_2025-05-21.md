---
tags:
  - firmware
  - github-repository
  - industrial-boards
  - flex-pay
  - flex-port
  - hardware
---

# Flex-Port & Flex-Pay Hardware Development Action Items
**Follow-up Date: May 21, 2025**  
**Source Meeting: May 20, 2025 Hardware Development Meeting**

---

## 🚨 IMMEDIATE ITEMS TO CHECK

### 1. **Evgeny Yavorsky - FlexPort Firmware Version**
- **STATUS**: Was supposed to send updated version to Minsk yesterday evening (May 20)
- **ACTION**: Confirm version was sent containing:
  - ✅ SAS protocol implementation for ticket validation
  - ✅ Logging command functionality (60-byte stub)
- **FOLLOW-UP**: Get confirmation from Minsk team they received it
- **PRIORITY**: CRITICAL - Blocking Minsk testing

### 2. **Evgeny Alexeev - USB Implementation** 
- **STATUS**: First phase complete (USB detection, file reading)
- **DUE DATE**: May 25 for second phase (memory writing, verification, program switching)
- **ACTION**: Confirm he's switching to help Yavorsky with SAS packet preparation
- **DELIVERABLE**: Packed SAS packets for logging functionality

### 3. **Remote Firmware Update**
- **STATUS**: Starting today (May 21)
- **ACTION**: Confirm Chudinov and Yavorsky connected and began collaboration
- **CRITICAL TEST**: First test accepting 64KB packets via WSS protocol
- **FALLBACK**: If 64KB fails, try 16KB packets

---

## 📦 HARDWARE ORDERS TO VERIFY

### 4. **Gennady Peari - Industrial Boards**
- **ACTION**: Confirm order placed for:
  - 2 boards to JVL Minsk  
  - 4 boards to JVL Toronto
  - Sample boards for testing ($120-130 each)
- **SPECS**: 3.5" x 5" fanless industrial board
- **PURPOSE**: TITO server, Income API, JVL accounting host

### 5. **Gennady - Dispenser Units**
- **ACTION**: Confirm order for cheaper dispenser model
- **QUANTITIES**:
  - 2 units to Minsk
  - 4 units to Toronto
- **REQUIREMENTS**:
  - ✅ 450-card minimum capacity
  - ✅ $320 vs $375 (50% cheaper)
  - ✅ Better capacity than current model

### 6. **iVision Harness**
- **DUE DATE**: May 23, 2025
- **RESPONSIBLE**: Gennady
- **ACTION**: Check progress on manual assembly

---

## 📝 DOCUMENTATION & REPOSITORY

### 7. **GitHub Repositories**
- **COMPLETED**: SMIB repository created during meeting
- **ACTION**: Verify Alexeev and Yavorsky have:
  - ✅ Access to repository
  - ✅ Pushed initial code
  - ✅ Set up proper versioning
- **PENDING**: 
  - FlexPay repository (due June 15)
  - Migration from Bitbucket

### 8. **Test Cards from Incomm**
- **STATUS**: In process, explanation provided to Incomm
- **ACTION**: Push Incomm for delivery timeline
- **DESTINATIONS**:
  - 📍 Minsk
  - 📍 Toronto
  - 📍 Georgia
  - 📍 Miami

---

## 🔧 TECHNICAL CLARIFICATIONS

### 9. **SAS Logging Requirements**
- **REQUIREMENT**: Log ALL SAS commands (except pings)
- **ACTION**: 
  - Confirm implementation with development team
  - Ensure sufficient memory allocated for logs
  - Verify both machine→FlexPort and FlexPort→machine logging
- **PURPOSE**: Debug machine behavior differences

### 10. **Receipt & Jackpot Tickets**
- **DECISION MADE**: Must support printing both ticket types
- **CLARIFICATION**: 
  - These tickets are for Cage processing
  - Will be validated in future POS hardware (not kiosk)
- **ACTION**: Ensure team understands expanded protocol requirements

---

## 📊 TRACKING ITEMS

### Hardware Inventory Status
- **Current FlexPort Units**: ~40 total
  - Some deployed to Georgia office (2-3 units)
  - Some sent to Minsk (2-3 units)
  - 1 unit in Val's office
- **New Production**: 20 additional units to be ordered

### Firmware Versions
- **SMIB Firmware**: Version number to be provided by Alexeev
- **FlexPort Firmware**: Confirm if changed from last month's version

---

## 📅 NEXT MEETING
- **Date**: Monday, May 26, 2025
- **Preparation Required**:
  - Firmware version numbers for both SMIB and FlexPort
  - Status update on all action items
  - Protocol for handling simultaneous Wallet/TITO connections (Chudinov)

---

## 🎯 CRITICAL PATH ITEMS

1. **Minsk Firmware** - Team needs working firmware TODAY to continue testing
2. **Remote Firmware Update** - Must start immediately, blocking other progress
3. **USB Implementation** - May 25 deadline is critical for next development phase
4. **GitHub Repository Access** - Developers need proper access to push code

---

## 📞 CONTACTS TO FOLLOW UP

- **Evgeny Yavorsky** - Firmware delivery confirmation
- **Evgeny Alexeev** - USB progress and SAS packet support
- **Pavel Frolov** - Repository management and FlexPay migration
- **Dmitry Chudinov** - Remote firmware update collaboration
- **Gennady Peari** - Hardware orders and iVision harness
- **Incomm** - Test card delivery status

---

*Document Generated: May 21, 2025*  
*Next Review: May 26, 2025*