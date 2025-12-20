# Project Planning & Requirements Template

**Version**: v1.1 – Universal Planning Standard  
**Last Updated**: 2024-12-20 *(Date reflects last structural revision)*

---

## Purpose

This document provides a **reusable checklist and template** for planning any software project. Before writing code, complete each section to ensure clarity, alignment, and a solid foundation.

> [!IMPORTANT]
> Complete planning **before** implementation. Rushing to code without a plan leads to rework, scope creep, and technical debt.

> [!NOTE]
> Not all sections apply to every project. Mark N/A where irrelevant, but consciously decide—don't skip by accident.

---

## Table of Contents

1. [Project Identity](#1-project-identity)
2. [Problem Statement](#2-problem-statement)
3. [Target Users](#3-target-users)
4. [Feature Requirements](#4-feature-requirements)
5. [Non-Functional Requirements](#5-non-functional-requirements)
6. [UI/UX Planning](#6-uiux-planning)
7. [Architecture Planning](#7-architecture-planning)
8. [Technology Selection](#8-technology-selection)
9. [Data & Storage](#9-data--storage)
10. [Integration Points](#10-integration-points)
11. [Security Considerations](#11-security-considerations)
12. [Legal & Compliance](#12-legal--compliance)
13. [Deployment & Distribution](#13-deployment--distribution)
14. [Operations & Maintenance](#14-operations--maintenance)
15. [Documentation & Knowledge Transfer](#15-documentation--knowledge-transfer)
16. [Testing Strategy](#16-testing-strategy)
17. [Success Metrics](#17-success-metrics)
18. [Risks & Mitigations](#18-risks--mitigations)
19. [Timeline & Phases](#19-timeline--phases)
20. [Open Questions](#20-open-questions)
21. [Approval Checklist](#21-approval-checklist)

---

## 1. Project Identity

| Field | Value |
|-------|-------|
| **Project Name** | [Short, memorable name] |
| **Codename** (optional) | [Internal codename if different] |
| **One-Line Description** | [What it does in one sentence] |
| **Project Type** | [ ] Desktop App  [ ] Web App  [ ] Mobile App  [ ] CLI  [ ] Library  [ ] Service/API  [ ] Other: ___ |
| **Target Platform(s)** | [ ] Windows  [ ] macOS  [ ] Linux  [ ] iOS  [ ] Android  [ ] Web  [ ] Cross-platform |

---

## 2. Problem Statement

### 2.1 What Problem Does This Solve?

> Describe the pain point or gap this project addresses. Be specific.

```
[Write 2-3 sentences describing the problem]
```

### 2.2 Who Has This Problem?

```
[Describe the affected users/personas]
```

### 2.3 How Is It Currently Solved?

| Current Solution | Limitations |
|------------------|-------------|
| [Existing tool/method 1] | [Why it's inadequate] |
| [Existing tool/method 2] | [Why it's inadequate] |
| [Manual workaround] | [Why it's painful] |

### 2.4 Why Build This Now?

```
[What makes this the right time? Market need? Technology available?]
```

### 2.5 Assumptions & Constraints

> [!CAUTION]
> Unwritten assumptions cause future conflicts. Document them explicitly.

#### Assumptions

| Assumption | Rationale | Risk if False |
|------------|-----------|---------------|
| [Assumption 1] | [Why we believe this] | [What breaks if wrong] |
| [Assumption 2] | [Why we believe this] | [What breaks if wrong] |
| [Assumption 3] | [Why we believe this] | [What breaks if wrong] |

#### Constraints

| Constraint | Source | Impact |
|------------|--------|--------|
| [Constraint 1] | [Who/what imposed it] | [How it limits design] |
| [Constraint 2] | [Source] | [Impact] |
| [Constraint 3] | [Source] | [Impact] |

---

## 3. Target Users

### 3.1 Primary Users

| Persona | Description | Technical Level | Key Need |
|---------|-------------|-----------------|----------|
| [Persona 1] | [Who they are] | Beginner / Intermediate / Expert | [What they need most] |
| [Persona 2] | [Who they are] | Beginner / Intermediate / Expert | [What they need most] |

### 3.2 Secondary Users

```
[Users who benefit but aren't the primary focus]
```

### 3.3 Anti-Users (Who This Is NOT For)

```
[Explicitly state who this project does NOT target]
```

---

## 4. Feature Requirements

### 4.1 Must-Have (MVP)

| # | Feature | Description | Acceptance Criteria |
|---|---------|-------------|---------------------|
| 1 | [Feature name] | [What it does] | [How to verify it works] |
| 2 | [Feature name] | [What it does] | [How to verify it works] |
| 3 | [Feature name] | [What it does] | [How to verify it works] |

### 4.2 Should-Have (Post-MVP)

| # | Feature | Description | Priority |
|---|---------|-------------|----------|
| 1 | [Feature name] | [What it does] | High / Medium / Low |
| 2 | [Feature name] | [What it does] | High / Medium / Low |

### 4.3 Nice-to-Have (Future)

```
- [Feature idea 1]
- [Feature idea 2]
- [Feature idea 3]
```

### 4.4 Explicitly Out of Scope

> [!WARNING]
> These features are **intentionally excluded** from this version:

```
- [Out of scope item 1] — Reason: [why excluded]
- [Out of scope item 2] — Reason: [why excluded]
```

### 4.5 Non-Goals (Design Intent Boundaries)

> [!IMPORTANT]
> "Out of scope" is tactical. Non-goals are **philosophical**. These protect architecture from scope creep.

This project explicitly does **NOT** aim to:

```
- [Non-goal 1: e.g., "Replace full-fledged enterprise platforms"]
- [Non-goal 2: e.g., "Optimize for non-technical users"]
- [Non-goal 3: e.g., "Provide real-time collaboration in v1"]
- [Non-goal 4: e.g., "Guarantee backward compatibility across major versions"]
```

---

## 5. Non-Functional Requirements

### 5.1 Performance

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| Startup time | < __ seconds | Stopwatch / profiler |
| Memory usage (idle) | < __ MB | Task Manager |
| CPU usage (idle) | < __% | Task Manager |
| Response time | < __ ms | Logs / profiler |
| Concurrent users | __ users | Load testing |

### 5.2 Availability & Reliability

| Requirement | Target |
|-------------|--------|
| Uptime | __% (e.g., 99.9%) |
| Mean Time Between Failures | __ hours/days |
| Data loss tolerance | Zero / Minimal / Acceptable |

### 5.3 Scalability

```
[ ] Single user only
[ ] Multi-user, single machine
[ ] Multi-user, network
[ ] Cloud-scale (thousands of users)
```

### 5.4 Compatibility

| Platform/Version | Support Level |
|------------------|---------------|
| Windows 11 | Full |
| Windows 10 | Full / Partial / None |
| macOS 14+ | Full / Partial / None |
| [Other] | [Level] |

### 5.5 Accessibility

```
[ ] Keyboard navigation
[ ] Screen reader support
[ ] High contrast mode
[ ] Font scaling
[ ] N/A for this project
```

---

## 6. UI/UX Planning

### 6.1 Design Philosophy

| Aspect | Choice |
|--------|--------|
| Visual Style | Minimal / Modern / Playful / Corporate / Glassmorphism / Other: ___ |
| Color Scheme | Dark / Light / Auto / User-selectable |
| Typography | System fonts / Custom fonts: ___ |
| Animation Level | None / Subtle / Rich |

### 6.2 Failure Philosophy

> How the system handles and communicates errors.

| Aspect | Choice |
|--------|--------|
| Failure Mode | Fail fast / Fail safe / Fail silent |
| Error Visibility | User-actionable / System-only / Logged only |
| Recovery Strategy | Auto-retry / Manual retry / Graceful degradation |

### 6.3 Key Screens/Views

| Screen | Purpose | Priority |
|--------|---------|----------|
| [Screen 1] | [What user does here] | MVP / Post-MVP |
| [Screen 2] | [What user does here] | MVP / Post-MVP |
| [Screen 3] | [What user does here] | MVP / Post-MVP |

### 6.4 UI Mockups Required

| Mockup | Status | Notes |
|--------|--------|-------|
| [Screen/Component 1] | [ ] Pending  [ ] Generated  [ ] Approved | [Link or notes] |
| [Screen/Component 2] | [ ] Pending  [ ] Generated  [ ] Approved | [Link or notes] |

### 6.5 User Flows

```
Main Flow:
1. User opens app → 
2. [Step 2] → 
3. [Step 3] → 
4. [Goal achieved]

Error Flow:
1. [Error occurs] → 
2. [User sees message] → 
3. [User can recover by ___]
```

### 6.6 Responsive/Adaptive Design

```
[ ] Single fixed size
[ ] Resizable window (min: ___x___, max: ___x___)
[ ] Responsive (adapts to screen size)
[ ] Multiple layouts (desktop/tablet/mobile)
```

---

## 7. Architecture Planning

### 7.1 High-Level Architecture

```
[Draw ASCII diagram or describe layers]

┌─────────────────────────────────────┐
│           Presentation              │
├─────────────────────────────────────┤
│           Business Logic            │
├─────────────────────────────────────┤
│           Data Access               │
├─────────────────────────────────────┤
│           Infrastructure            │
└─────────────────────────────────────┘
```

### 7.2 Component Breakdown

| Component | Responsibility | Depends On |
|-----------|----------------|------------|
| [Component 1] | [What it does] | [Dependencies] |
| [Component 2] | [What it does] | [Dependencies] |

### 7.3 Plugin/Extension Architecture

```
[ ] Not applicable (monolithic)
[ ] Plugin-based architecture
    - Plugin contract defined: [ ] Yes [ ] No
    - Plugin discovery method: ___
    - Plugin isolation: [ ] Full [ ] Partial [ ] None
```

### 7.4 Architectural Patterns

```
[ ] MVC / MVP / MVVM
[ ] Clean Architecture
[ ] Microservices
[ ] Monolith
[ ] Event-driven
[ ] CQRS
[ ] Other: ___
```

### 7.5 ADRs (Architectural Decision Records)

| ADR # | Decision | Status |
|-------|----------|--------|
| 001 | [Major decision 1] | Proposed / Accepted / Superseded |
| 002 | [Major decision 2] | Proposed / Accepted / Superseded |

### 7.6 Change & Versioning Strategy

#### Versioning

```
[ ] Semantic versioning: MAJOR.MINOR.PATCH
[ ] Calendar versioning: YYYY.MM.PATCH
[ ] Other: ___

Breaking changes allowed only in: [ ] MAJOR releases [ ] Never [ ] Any release
```

#### Change Control

| Change Type | Approval Required |
|-------------|-------------------|
| UI changes | [Who approves] |
| Architecture changes | [Who approves] |
| Security changes | [Who approves] |
| API changes | [Who approves] |

#### Deprecation Policy

```
Minimum supported versions: [e.g., "current + 2 previous"]
Deprecation notice period: [e.g., "1 major version"]
Migration path required: [ ] Yes [ ] No
```

---

## 8. Technology Selection

### 8.1 Technology Comparison

| Option | Pros | Cons | Verdict |
|--------|------|------|---------|
| [Tech 1] | [Advantages] | [Disadvantages] | ✅ Selected / ❌ Rejected |
| [Tech 2] | [Advantages] | [Disadvantages] | ✅ Selected / ❌ Rejected |

### 8.2 Final Stack

| Layer | Technology | Version | Justification |
|-------|------------|---------|---------------|
| Frontend | [Tech] | [Version] | [Why chosen] |
| Backend | [Tech] | [Version] | [Why chosen] |
| Database | [Tech] | [Version] | [Why chosen] |
| Build/Package | [Tech] | [Version] | [Why chosen] |

### 8.3 Dependencies

| Dependency | Purpose | License | Risk |
|------------|---------|---------|------|
| [Library 1] | [What it provides] | MIT / Apache / GPL / Other | Low / Medium / High |
| [Library 2] | [What it provides] | [License] | [Risk level] |

---

## 9. Data & Storage

### 9.1 Data Model Overview

```
[Describe key entities and relationships]

Entity: User
├── id (unique)
├── name
└── preferences → Preferences

Entity: Preferences
├── theme
└── enabled_features[]
```

### 9.2 Storage Strategy

| Data Type | Storage Location | Format | Persistence |
|-----------|------------------|--------|-------------|
| User preferences | Local file | JSON | Persistent |
| Cache | Memory | In-memory | Session |
| [Other data] | [Location] | [Format] | [Duration] |

### 9.3 Data Privacy

```
[ ] No personal data collected
[ ] Personal data collected (list below):
    - [Data type 1]: [Purpose]
    - [Data type 2]: [Purpose]
[ ] GDPR compliance required
[ ] Data encryption required: [ ] At rest [ ] In transit
```

---

## 10. Integration Points

### 10.1 External APIs

| API | Purpose | Auth Method | Rate Limits |
|-----|---------|-------------|-------------|
| [API 1] | [What it provides] | API Key / OAuth / None | [Limits] |
| [API 2] | [What it provides] | [Auth] | [Limits] |

### 10.2 System Integrations

| System | Integration Type | Notes |
|--------|------------------|-------|
| Windows Registry | Read/Write | For auto-start |
| File System | Read/Write | For config storage |
| [Other] | [Type] | [Notes] |

### 10.3 Third-Party Services

```
[ ] No third-party services
[ ] Services used:
    - [Service 1]: [Purpose]
    - [Service 2]: [Purpose]
```

---

## 11. Security Considerations

### 11.1 Threat Model

| Threat | Likelihood | Impact | Mitigation |
|--------|------------|--------|------------|
| [Threat 1] | Low / Medium / High | Low / Medium / High | [How to prevent] |
| [Threat 2] | [Likelihood] | [Impact] | [Mitigation] |

### 11.2 Security Checklist

```
[ ] Input validation on all external data
[ ] No hardcoded secrets
[ ] Secrets stored securely (env vars, keyring)
[ ] Dependencies audited for vulnerabilities
[ ] Principle of least privilege applied
[ ] Sensitive data encrypted
[ ] Logging excludes sensitive data
```

### 11.3 Permissions Required

| Permission | Why Needed | User Consent |
|------------|------------|--------------|
| [Permission 1] | [Reason] | Implicit / Explicit prompt |
| [Permission 2] | [Reason] | [Consent type] |

---

## 12. Legal & Compliance

> Even if "N/A", consciously check each item.

```
[ ] Open-source license obligations reviewed
[ ] Export control concerns evaluated
[ ] Internal policy compliance verified
[ ] Industry-specific regulations (HIPAA, PCI, etc.): [ ] N/A [ ] Applicable: ___
[ ] Terms of service / EULA required
[ ] Privacy policy required
[ ] Data retention policy defined
```

---

## 13. Deployment & Distribution

### 13.1 Distribution Method

```
[ ] Direct download (website)
[ ] App store (Microsoft Store / Mac App Store / etc.)
[ ] Package manager (npm / brew / winget / etc.)
[ ] Enterprise deployment (MDM / SCCM)
[ ] Source only (build yourself)
```

### 13.2 Installer Requirements

| Requirement | Details |
|-------------|---------|
| Installer format | .exe / .msi / .dmg / .deb / .AppImage / Other: ___ |
| Installer size target | < ___ MB |
| Silent install support | [ ] Yes [ ] No |
| Uninstaller provided | [ ] Yes [ ] No |
| Upgrade path | [ ] In-app update [ ] Manual reinstall [ ] Auto-update |

### 13.3 User Notifications During Install

```
[ ] License agreement
[ ] Installation location choice
[ ] Desktop shortcut option
[ ] Start menu entry option
[ ] Auto-start option (with clear disclosure)
[ ] Privacy policy / data collection notice
```

---

## 14. Operations & Maintenance

> How the system will be operated and maintained post-launch.

### 14.1 Logging & Diagnostics

| Aspect | Details |
|--------|---------|
| Log storage location | [Path or service] |
| Log rotation policy | [e.g., "7 days, 100 MB max"] |
| Debug vs release verbosity | [Levels available] |
| Crash report collection | [ ] None [ ] Opt-in [ ] Automatic |

### 14.2 Failure Handling

| Scenario | Expected Behavior |
|----------|-------------------|
| Startup failure | [e.g., "Show actionable error with log path"] |
| Corrupt config | [e.g., "Auto-reset to defaults + warn user"] |
| Missing dependency | [e.g., "Graceful degradation with message"] |
| Network unavailable | [e.g., "Offline mode with sync later"] |

### 14.3 Support Model

| Aspect | Details |
|--------|---------|
| User support channel | [Email / Forum / Discord / etc.] |
| SLA expectations | [Response time, resolution time] |
| Issue triage process | [How bugs are prioritized] |
| On-call rotation | [ ] N/A [ ] Defined: ___ |

---

## 15. Documentation & Knowledge Transfer

> Prevents tribal knowledge decay.

| Artifact | Audience | Owner | Required? |
|----------|----------|-------|-----------|
| Architecture doc | Developers | Tech Lead | [ ] Yes [ ] No |
| User guide | End users | Product | [ ] Yes [ ] No |
| API reference | Integrators | Tech Lead | [ ] Yes [ ] No |
| Threat model | Security | Security Lead | [ ] Yes [ ] No |
| ADR log | Engineers | Team | [ ] Yes [ ] No |
| Runbook | Operations | DevOps | [ ] Yes [ ] No |

> [!NOTE]
> Documentation is considered **DONE** only when updated alongside code changes.

---

## 16. Testing Strategy

### 16.1 Test Types

| Test Type | Coverage Target | Tools |
|-----------|-----------------|-------|
| Unit tests | __% of core logic | [Framework] |
| Integration tests | Critical paths | [Framework] |
| E2E tests | Main user flows | [Framework] |
| Manual testing | Edge cases | Checklist |

### 16.2 Test Environments

```
[ ] Local development
[ ] CI/CD pipeline
[ ] Staging environment
[ ] Production monitoring
```

### 16.3 Acceptance Criteria Template

```
Given: [Initial state]
When: [Action taken]
Then: [Expected result]
```

---

## 17. Success Metrics

### 17.1 Launch Criteria

| Metric | Target | Current |
|--------|--------|---------|
| All MVP features complete | 100% | __% |
| Critical bugs | 0 | __ |
| Test coverage | > __% | __% |
| Performance targets met | Yes | [ ] |

### 17.2 Post-Launch Metrics

| Metric | Target | Measurement |
|--------|--------|-------------|
| User adoption | __ users in __ days | Analytics |
| Crash rate | < __% | Error tracking |
| User satisfaction | > __ / 5 | Survey / reviews |
| [Custom metric] | [Target] | [Method] |

---

## 18. Risks & Mitigations

| Risk | Probability | Impact | Mitigation | Owner |
|------|-------------|--------|------------|-------|
| [Risk 1] | Low / Medium / High | Low / Medium / High | [Plan] | [Who handles] |
| [Risk 2] | [Prob] | [Impact] | [Plan] | [Owner] |
| [Risk 3] | [Prob] | [Impact] | [Plan] | [Owner] |

---

## 19. Timeline & Phases

### 19.1 Phase Breakdown

| Phase | Description | Duration | Deliverables |
|-------|-------------|----------|--------------|
| Phase 1: Planning | Requirements, design | __ days | This document, mockups |
| Phase 2: Foundation | Project setup, core infra | __ days | Scaffold, CI/CD |
| Phase 3: Core Features | MVP implementation | __ days | Working MVP |
| Phase 4: Polish | Testing, bug fixes | __ days | Release candidate |
| Phase 5: Launch | Distribution, docs | __ days | v1.0 release |

### 19.2 Milestones

| Milestone | Target Date | Status |
|-----------|-------------|--------|
| Planning complete | [Date] | [ ] Not started [ ] In progress [ ] Done |
| MVP complete | [Date] | [ ] Not started [ ] In progress [ ] Done |
| Beta release | [Date] | [ ] Not started [ ] In progress [ ] Done |
| v1.0 release | [Date] | [ ] Not started [ ] In progress [ ] Done |

---

## 20. Open Questions

> [!CAUTION]
> These questions must be resolved before implementation:

| # | Question | Proposed Answer | Status |
|---|----------|-----------------|--------|
| 1 | [Question 1] | [Tentative answer] | [ ] Open [ ] Resolved |
| 2 | [Question 2] | [Tentative answer] | [ ] Open [ ] Resolved |
| 3 | [Question 3] | [Tentative answer] | [ ] Open [ ] Resolved |

---

## 21. Approval Checklist

Before moving to implementation, confirm:

### Planning Completeness

- [ ] Problem statement is clear and validated
- [ ] Assumptions and constraints are documented
- [ ] Target users are defined
- [ ] MVP features are prioritized
- [ ] Non-goals are explicit
- [ ] Out-of-scope items are explicit
- [ ] Non-functional requirements have targets
- [ ] UI mockups are approved
- [ ] Architecture is documented
- [ ] Change/versioning strategy defined
- [ ] Technology is selected and justified
- [ ] Security considerations addressed
- [ ] Legal/compliance reviewed
- [ ] Deployment method chosen
- [ ] Operations/maintenance plan exists
- [ ] Documentation ownership assigned

### Stakeholder Approval

| Stakeholder | Role | Approved | Date |
|-------------|------|----------|------|
| [Name/Role] | Decision maker | [ ] | [Date] |
| [Name/Role] | Technical lead | [ ] | [Date] |
| [Name/Role] | Designer | [ ] | [Date] |

---

## Summary Philosophy

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                                                                              │
│   ✓ Clarity before code              ✓ Questions before assumptions         │
│   ✓ Scope before schedule            ✓ Architecture before implementation   │
│   ✓ User needs before features       ✓ Risks before commitments             │
│   ✓ Constraints before creativity    ✓ Operations before launch             │
│                                                                              │
│   Good projects are PLANNED.                                                 │
│   Bad projects are DISCOVERED during implementation.                         │
│                                                                              │
│   We are building the former.                                                │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

**This is not just a template. This is project clarity insurance.**
