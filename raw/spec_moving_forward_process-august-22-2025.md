# Specification-Driven Development Process
## With JIRA-GitHub Integration

**Date**: August 22, 2025  
**Participants**: Val Levitan, Pavel Frolov, Irina Shishko  
**Version**: 2.0 (Simplified)

---

## Core Philosophy

> "No code without specification, no specification without requirements"

We're making implicit developer knowledge explicit by:
1. Documenting specifications in the code repository
2. Using JIRA for business requirements, GitHub for technical implementation
3. Having QA validate both business and technical aspects
4. Writing AI-interpretable specifications for automated assistance

---

## The Simple Flow

### JIRA (Business Layer)
```
Value Stream → Initiative → Product → Capability (CAP-XXX)
                                            ↓
                                    [Create Branch Button]
                                            ↓
```

### GitHub (Engineering Layer)
```
                                    feature/CAP-XXX branch
                                            ↓
                            Specification (/specifications/CAP-XXX.md)
                                            ↓
                                    Implementation + Tests
```

---

## What Lives Where

### JIRA Owns
- **Capabilities** (CAP-XXX): Business requirements and acceptance criteria
- **Features**: Sub-tasks under Capabilities
- **Status Tracking**: Automatic via GitHub integration
- **Defect Management**: Business-level bugs

### GitHub Repository Owns
- **Specifications**: Technical interpretation in `/specifications/`
- **Code**: Implementation in `/src/`
- **Tests**: Test cases in `/tests/`
- **Documentation**: Technical docs

### The Bridge
- JIRA creates GitHub branches directly: `feature/CAP-XXX`
- Commits reference JIRA IDs for automatic tracking
- Pull requests link back to JIRA Capabilities

---

## Repository Structure

```
project-root/
├── specifications/            # Technical specs (AI-interpretable)
│   └── CAP-XXX.md            # One per JIRA Capability
├── src/                      # Implementation code
├── tests/
│   ├── unit/                 # Developer tests
│   ├── integration/          # Shared Dev/QA tests
│   └── e2e/                  # QA end-to-end tests
└── .github/
    └── pull_request_template.md  # Includes QA checklist
```

---

## Specification Template (Simplified)

```markdown
# Specification: CAP-XXX - [Title]
JIRA: https://company.atlassian.net/browse/CAP-XXX

## Technical Requirements
- [Converted from JIRA acceptance criteria]
- [Performance requirements]
- [Security requirements]

## Implementation
```yaml
inputs:
  - name: [parameter]
    type: [type]
    validation: [rules]

process:
  - step: [what happens]
  - step: [next step]

outputs:
  - name: [result]
    type: [type]
```

## Test Scenarios (QA-provided)
- Functional: [test case linking to JIRA acceptance criteria]
- Edge cases: [boundary conditions]
- Regression: [previous bugs to check]

## Status
- [ ] Specification approved
- [ ] Code implemented
- [ ] Tests passing
- [ ] QA approved
```

---

## The Workflow

### Phase 1: Business Definition (JIRA)
1. Product Manager creates Capability (CAP-XXX)
2. Defines acceptance criteria
3. QA reviews for testability
4. Marks "Ready for Development"

### Phase 2: Technical Planning (Bridge)
1. Click "Create Branch" in JIRA → `feature/CAP-XXX` in GitHub
2. Engineer writes `/specifications/CAP-XXX.md`
3. QA adds test scenarios
4. Team approves specification

### Phase 3: Implementation (GitHub)
1. Developers code in the feature branch
2. QA writes tests in parallel (not after)
3. Commits reference CAP-XXX for tracking
4. JIRA automatically shows progress

### Phase 4: Validation (Both)
1. Pull request requires QA approval
2. Tests validate specification
3. QA validates JIRA acceptance criteria
4. Merge updates JIRA status automatically

---

## Roles (Simplified)

### Business Product Manager (Juan Martinez) - JIRA
- Creates Capabilities with business requirements
- Defines acceptance criteria from customer perspective
- Monitors business value delivery

### Technical Product Manager (Nathan Carver, Will Jones) - Bridge
- Nathan Carver: Overall technical product strategy
- Will Jones: Architecture product management with Pavel
- Translate business Capabilities to technical approach

### Director of Engineering (Pavel Frolov) - Architecture Approval
- Reviews and approves all architectural decisions
- Works with Will Jones on architecture strategy
- Ensures technical feasibility of Capabilities

### Developers (Sasha Biratka) - GitHub
- Write specifications from Capabilities
- Implement code following specifications
- Commit with JIRA references

### QA (Irina, Evgeny Kharetski) - Both
- Review Capabilities for testability (JIRA)
- Add test scenarios to specifications (GitHub)
- Write tests in parallel with development
- Approve pull requests before merge

---

## Implementation Phases

### Month 1-3: Foundation
- Set up JIRA-GitHub integration
- Create first 5 specifications from existing Capabilities
- Train team on workflow

### Month 4-6: Adoption
- All new Capabilities get specifications
- 30% of code has specifications
- QA gates established

### Year 2: Maturity
- 80% specification coverage
- AI assists with spec writing
- Automated test generation from specs

---

## Success Metrics

### Short-term (3 months)
- [ ] JIRA-GitHub integration working
- [ ] 10% specification coverage
- [ ] QA reviewing all new specs

### Long-term (2 years)
- [ ] 80% specification coverage
- [ ] AI pair-programming from specs
- [ ] Full traceability: JIRA → Spec → Code → Tests

---

## Common Questions

**Q: Why both JIRA and GitHub?**
A: JIRA for business, GitHub for code. Native integration eliminates duplication.

**Q: Won't specifications get outdated?**
A: They live with code in the same repository and branch. Update together.

**Q: How does AI help?**
A: AI reads specifications to generate code, tests, and documentation.

---

## Next Steps

1. **Week 1**: Enable JIRA-GitHub integration
2. **Week 2**: Create first specification from current Capability
3. **Week 3**: Run pilot with one team
4. **Week 4**: Refine based on feedback

---

*This is a living document. Updates tracked in Git.*