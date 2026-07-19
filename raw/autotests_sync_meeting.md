---
tags:
  - test-configuration
  - implementation-approach
  - testing-challenges
  - pavel
  - strategy
  - technical
---

# Autotests Sync Meeting Transcript

**Date:** July 10, 2025, 2:24 PM  
**Transcription started by:** Pavel Frolov

## Participants
- Evgeny Kharetski
- Anton Leshkevich
- Irina Shishko
- Pavel Frolov
- Alexey Khamin
- Vladislav Gurin
- Ivan Shpak

## Meeting Summary

### Main Topics Discussed

#### 1. Test Environment Configuration (0:03 - 8:06)

**Evgeny Kharetski** outlined the need for flexible test configuration:
- Build large JSON objects using sectors for testing purposes
- Enable on-the-fly race resubscription without restarting the data center
- Test various error scenarios and different versions dynamically
- Create configurable passport settings that can be saved to and read from files

**Key challenges discussed:**
- Machine testing works with real devices, making virtual device substitution difficult
- Need to implement file-based passport storage for persistence across restarts
- Requirement for a test environment where both real and virtual devices are available

#### 2. Implementation Approach (8:06 - 11:48)

**Pavel Frolov** proposed the implementation strategy:
- Ability to connect to machines via SSH to execute commands
- Replace configuration files before test execution
- Create hooks in LGS for test framework integration

**Anton Leshkevich** clarified current test framework limitations:
- Tests currently assume environment is already set up
- No automated environment configuration functionality exists yet
- Need to add pre-test setup capabilities

**Evgeny Kharetski** emphasized:
- Configuration changes should be done at the test level
- Tests should know exactly which files they're working with
- Default states can be maintained in tests

#### 3. LISA Testing Challenges (4:04 - 6:19)

**Evgeny Kharetski** raised concerns about LISA testing:
- LISA is created for specific machines and versions
- Creating LISA for each specific test is not ideal for automation
- Need a solution to regulate LISA from tests

**Irina Shishko** noted:
- On tabachny version, LISA falls and is ignored
- Only etap is applied
- This is a temporary workaround until proper testing is implemented

#### 4. Incremental Development Approach (12:17 - 16:36)

**Irina Shishko** suggested starting with simple configurations:
- Begin with a machine without devices and one RIS setting
- Test basic functionality first before adding complexity
- Gradually add more settings once basic implementation works

**Evgeny Kharetski** disagreed with the incremental approach:
- Wants to provide proper tools from the start
- Concerned about having to rewrite tests later
- Emphasizes need for unified approach using proper tools

#### 5. RIS Implementation Plan (17:15 - 21:04)

**Evgeny Kharetski** outlined the RIS implementation:
- Provide JSON structure to Anton
- Anton creates builders for the JSON
- Evgeny provides endpoint for submitting RIS
- Tests will interact primarily through UI, using API only for configuration

**Technical details:**
- Need to handle multiple RIS submissions properly
- Ensure conflicts are avoided
- Provide methods to verify RIS application status

#### 6. Task Estimates and Next Steps (18:21 - 28:50)

**Time estimates discussed:**
- JSON builders: 2-3 hours (Anton)
- Endpoint implementation: Less than a week (Evgeny)
- Need to decompose tasks into subtasks

**Immediate actions:**
- Evgeny to provide list of DC requests with responses
- Anton to work on JSON builders once specification is ready
- Use machine environment for initial tests
- Team to continue discussions in shared chat

### Key Decisions

1. **Architecture**: Tests will interact with UI for user actions, API for configuration only
2. **Priority**: Focus on RIS implementation first before tackling virtualization
3. **Communication**: Continue collaboration through shared chat for questions and ideas
4. **Testing approach**: Start with simple machine configurations before adding complexity

### Action Items

1. **Evgeny Kharetski**:
   - Provide JSON structure specification to Anton
   - Create endpoint for RIS submission
   - Provide list of DC requests and responses

2. **Anton Leshkevich**:
   - Implement JSON builders based on Evgeny's specification
   - Add pre-test setup capabilities to test framework

3. **Team**:
   - Use machine environment for initial testing
   - Continue discussions on implementation details
   - Document any issues or questions that arise

## Meeting End
**Time:** Approximately 28:50  
**Transcription stopped by:** Pavel Frolov