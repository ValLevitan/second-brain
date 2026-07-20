# JVL HHR Project - Executive Digest

## Project Overview

JVL Systems is developing Historical Horse Racing (HHR) gaming terminals through a strategic partnership with Ainsworth. The project involves adapting JVL's existing gaming framework to integrate with Ainsworth's proven HHR server infrastructure, which has been operational since 2018.

**Current Status**: Architecture and requirements phase (Q1 2025)  
**Implementation Start**: June/July 2025 (delayed due to Omni platform priorities)  
**Key Challenge**: Reconciling three parallel state machines while maintaining player experience during system failures

---

## How JVL is Approaching HHR

### Strategic Philosophy
JVL is taking a **methodical, player-experience-first approach** that prioritizes fault tolerance over strict protocol adherence. Unlike competitors who immediately lock machines during connection issues, JVL aims to continue gameplay using cached race tickets.

### Technical Approach

#### Core Architecture
1. **Dual-Layer System**
   - Legal compliance layer: Historical horse races determine all outcomes
   - Entertainment layer: Slot-style presentation for player engagement
   - Seamless integration between layers to hide the underlying race mechanics

2. **Intelligent Caching System**
   - 10 race tickets cached per bet level
   - Enables offline play during server outages
   - Graceful degradation (disable individual bet levels, not entire machine)

3. **Communication Management**
   - Asynchronous message handling for non-blocking operations
   - Critical message queue for essential transactions
   - Heartbeat monitoring with configurable timeout tolerances

### Competitive Differentiation
- **Superior fault tolerance**: Continue play during server disconnections
- **Better player experience**: Soft tilts instead of hard locks
- **Flexible configuration**: Adaptable to different jurisdictional requirements

---

## Critical Decision Points Team is Struggling With

### 1. **The State Machine Paradox**
**Core Problem**: Three parallel processes that cannot be elegantly represented in a single state diagram

**Efim's Assessment**:
> *"The problem with trying to make it a nice clean state diagram is that these processes are going in parallel"*

**Impact**: Without clear state definitions, developers cannot implement consistent behavior across edge cases.

### 2. **When Can Players Actually Play?**
**The Question**: What exact conditions must be met for gameplay to be allowed?

**Complexity Revealed**:
> *"This condition where we can play, it's not trivial, it's a lot of conditions"* - Efim

**Unresolved Variables**:
- Server connection status
- Cache availability
- Pending critical messages
- Progressive broadcast status
- Current game state

### 3. **Connection Loss Philosophy**
**Fundamental Disagreement**: How to handle brief disconnections

**Two Camps**:
- **Efim**: *"If you just lost the connection for a minute, do we need to [re-register]?"* (favors continuity)
- **Will**: *"Without going through the same path...we would have a condition where we would be able to come up with and say oh, that doesn't work"* (favors consistency)

### 4. **Extra Winnings Trigger Mechanism**
**The Dilemma**: How to determine when extra winnings are awarded

**Options**:
- Pool-based triggers (risk of manipulation)
- Pattern-based triggers (complex algorithm needed)

**Status**: *"We put a question mark for ourselves"* - Efim

### 5. **Progressive Jackpot Offline Behavior**
**Critical Decision**: What happens when progressive broadcasts stop?

**Juan's Proposal**: Continue until tickets depleted
**Will's Concern**: Need configurable behavior per jurisdiction
**Risk**: Player hitting unvalidatable progressive

### 6. **Critical Message Hierarchy**
**The Challenge**: Not all "critical" messages are equally critical

**Efim's Insight**:
> *"Critical messages of two kinds, one is that allow us to play faster and differently"*

**Unresolved**: How to architect blocking vs. non-blocking critical messages

### 7. **Manual Handicapping Flow**
**Problem**: Manual betting requires synchronous server response in an async system
**Impact**: Potential player-visible delays during manual bet placement

### 8. **Power Loss Recovery**
**Open Question**: How to restore mid-game state after unexpected shutdown?

**Efim's Concern**:
> *"Do we start to play if we have critical messages from previous day?"*

### 9. **Race Ticket Depletion Strategy**
**Decision Point**: When one bet level's tickets are depleted:
- Disable entire machine? (simpler)
- Disable only that bet button? (better UX, more complex)

**Juan's Preference**: Keep other bet levels playable

### 10. **Game History Storage Depth**
**Regulatory Requirement**: Store 50 games
**Technical Challenge**: Multi-stage games could require 2500+ records

**Efim's Warning**:
> *"If you have 50 games and potentially like 50 free spins per game...it might be a lot of stuff to store"*

---

## Architectural Design Points in Limbo

### Not Yet Created
1. **State Machine Definition**
   - Will: *"Where's our state machine?"*
   - Efim: *"Yeah, I think I will [create it]"*

2. **Progressive Translation Layer**
   - Where HHR progressive amounts convert to standard progressive controller format
   - Implementation point undefined

### Cannot Be Properly Designed Yet
1. **Parallel Process Representation**
   - Three concurrent processes resist clean diagramming
   - May require multiple diagrams or new notation

2. **Recovery Architecture**
   - Mid-game state restoration after power loss
   - Pending critical message handling

### Waiting for External Clarification
1. **Reconnection Requirements** (Ainsworth)
   - When is full re-registration required?
   - What triggers "not ready" state?

2. **Extra Winnings Algorithm**
   - Per pool or per prize?
   - Trigger probability calculations

### Explicitly Deferred Decisions
1. **Cache Initialization Timing**
   - Start after server "ready" or after local initialization?

2. **Manual Handicap Architecture**
   - How to handle synchronous requests in async system

---

## Key Corrections & Clarifications

### Lockup Conditions (Corrected)
**Important**: Large win lockups occur when **BOTH** conditions are met:
- Win is $600 or more **AND**
- Win is more than 300x the bet amount

*Not* when either condition is met independently.

### Timeline Reality Check
- **Current**: Requirements and architecture phase
- **June/July 2025**: Implementation start (not immediate)
- **Reason for delay**: Senior developer occupied with Omni platform

### Documentation Approach
**Will's Assessment**:
> *"Within the next 4 weeks, I doubt there will be any more user stories that I should be writing"*

Team is documenting extensively before implementation to minimize development surprises.

---

## Executive Recommendations

### Immediate Actions Needed
1. **Create formal state machine diagram** (Efim committed to this)
2. **Get Ainsworth clarifications** on reconnection protocol
3. **Decide on extra winnings trigger mechanism**

### Risk Mitigation Strategies
1. **Configuration-driven approach** for jurisdictional differences
2. **Extensive documentation** before implementation
3. **Parallel development** of independent components where poss