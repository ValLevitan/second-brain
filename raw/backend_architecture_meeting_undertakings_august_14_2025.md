# Backend Architecture Meeting - Action Items and Undertakings
**Date:** August 14, 2025  
**Follow-up Meeting:** August 28-29, 2025

## Executive Summary
This meeting established the critical path for delivering Transactional Products MVP for the Georgia market by January 2026, with a phased approach to integrating HHR and CMS modernization. Priority is given to the minimum viable product that enables ACH transactions within a single day of operation.

## Critical Timeline
- **January 2026**: Beta testing/locations in Georgia (MVP DELIVERY)
- **July 1, 2026**: Georgia regulatory deadline for Transactional Products (HARD DEADLINE)
- **August 28-29, 2025**: Architecture review meeting with full team
- **October 15, 2025**: Deep-dive session for CMS modernization
- **November 15, 2025**: Advanced architecture session (HHR, reporting, migrations)

## Primary Undertaking: Architecture Discovery Team

### Team Assignment
**Nathan Carver, Juan Martinez, Will Jones, and Pavel Frolov** are tasked with conducting a series of meetings over the next 10 days to:

1. **Comprehensive Material Review**
   - Sift through all available CMS documentation and codebase
   - Review HHR requirements and integration specifications (80-95% complete)
   - Analyze Transactional Products architecture requirements
   - Assess and develop a course of action for extracting and organizing the tribal knowledge of CMS

2. **Requirements Definition - MVP Focus**
   - **Emphasize the Minimum Deliverable for January 2026:**
     - Method for Flex-POS and table-top card dispenser to validate transactions
     - Transfer funds from locations to JVL Systems within single day via ACH
     - Minimize effort required to set up ACH (automated clearing house) transactions
   - Identify only essential modules for MVP:
     - Payment processing
     - Device authentication
     - Transaction validation
     - ACH integration
     - Basic reporting for reconciliation

3. **Architecture Planning - Achievable Scope**
   - Design minimal viable backend for January 2026 delivery
   - Focus on Transactional Products payment flow
   - Document integration points that can be built incrementally
   - Defer complex CMS migration and HHR integration details to Phase 2

4. **Deliverables for August 28-29 Meeting**
   - MVP architecture diagram for January 2026 delivery
   - ACH transaction flow and validation process
   - Critical path timeline with clear dependencies
   - List of deferred items for October 15 deep-dive
   - Resource requirements for MVP only

## Phased Delivery Approach

### Phase 1: MVP for January 2026
**Focus:** Transactional Products - Payment Processing Only

#### Transactional Products MVP (PRIORITY #1)
**Owner:** Nathan Carver (with Juan Martinez)
- **January 2026 Deliverables:**
  - Basic ACH transaction processing (single-day transfers)
  - Flex-POS and table-top card dispenser validation
  - Simple transaction logging for reconciliation
  - Minimal viable authentication system

#### Minimal CMS Support
**Owner:** Pavel Frolov
- **January 2026 Deliverables:**
  - Device authentication only
  - Location/terminal ID management
  - Daily email reports to operators
  - Defer all legacy migration work

#### HHR Integration
**Owner:** Will Jones  
- **January 2026 Status:** DEFERRED to Phase 2
- Continue requirements gathering only
- No implementation for MVP

### Phase 2: October 15 Deep-Dive Session
**Complex Topics Deferred:**
- Full CMS modernization and Omni migration

### Phase 3: November 15 Session
**Advanced Architecture Topics:**
- HHR server integration architecture
- Advanced reporting and analytics
- Complex permission systems
- Legacy system migration strategies

## MVP Architectural Decisions (January 2026)

1. **Minimal Omni Usage**: Use Omni only where absolutely necessary for MVP
2. **Simple Payment Flow**: Direct ACH integration without complex orchestration
3. **Basic Reporting**: Update operators via daily emails
4. **Defer Complex Features**: No lease management, RIS, or advanced controls for MVP
5. **Rapid Deployment**: Focus on auto-configuration and plug-and-play setup

## MVP Business Requirements

- **Single-day ACH transfers**: Funds must move within 24 hours
- **Minimal setup effort**: Reduce ACH configuration complexity
- **Basic authentication**: Simple device validation without complex permissions
- **Transaction validation**: Flex-POS and card dispenser must validate all transactions
- **Essential reporting**: Daily reconciliation reports only

## Immediate Next Steps (Before August 28-29)

1. **Priority Tasks (Aug 14-21)**:
   - Define exact ACH integration requirements
   - Map minimal CMS touchpoints for device auth
   - Design simplest possible payment flow
   - Identify showstopper risks for January delivery

2. **Preparation Tasks (Aug 21-28)**:
   - Document MVP architecture only
   - Create critical path for January 2026
   - List all deferred items for Phase 2
   - Prepare resource needs for MVP sprint

## Expected Outcomes for August 28-29 Meeting

The team will present:
- **MVP-focused architecture** for January 2026 delivery
- **ACH transaction flow** with single-day processing
- **Critical path timeline** showing dependencies
- **Deferred items list** for October 15 session
- **Resource requirements** for 4-month MVP sprint
- **Risk assessment** for January deadline

## Notes
- **MVP First**: January 2026 MVP delivery takes absolute priority over all other initiatives
- **Phased Approach**: Complex architectural decisions deferred to October 15 deep-dive
- **ACH Focus**: Single-day fund transfers are the core MVP requirement
- **Technical Debt**: Legacy CMS debt will be addressed post-MVP in Phase 2
- **Tribal Knowledge**: Assessment and extraction planning only for now, implementation deferred

---
*This document summarizes the undertakings from the August 14, 2025 Backend Architecture meeting with focus on January 2026 MVP delivery. Please review and confirm your assigned responsibilities. Direct questions to Val Levitan.*