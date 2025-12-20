# Project Planning & Requirements Template

**Version**: v1.2 – Universal Planning Standard  
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
6. [Localization & Internationalization](#6-localization--internationalization)
7. [UI/UX Planning](#7-uiux-planning)
8. [Architecture Planning](#8-architecture-planning)
9. [Technology Selection](#9-technology-selection)
10. [Data & Storage](#10-data--storage)
11. [Integration Points](#11-integration-points)
12. [Security Considerations](#12-security-considerations)
13. [Legal & Compliance](#13-legal--compliance)
14. [Deployment & Distribution](#14-deployment--distribution)
15. [Operations, Maintenance & Incident Response](#15-operations-maintenance--incident-response)
16. [Monitoring & Observability](#16-monitoring--observability)
17. [Documentation & Knowledge Transfer](#17-documentation--knowledge-transfer)
18. [Testing Strategy](#18-testing-strategy)
19. [Success Metrics](#19-success-metrics)
20. [Risks & Mitigations](#20-risks--mitigations)
21. [Known Unknowns](#21-known-unknowns)
22. [External Dependencies & Blockers](#22-external-dependencies--blockers)
23. [Decision Log](#23-decision-log)
24. [Exit Criteria](#24-exit-criteria)
25. [Communication Plan](#25-communication-plan)
26. [Timeline & Phases](#26-timeline--phases)
27. [Open Questions](#27-open-questions)
28. [Approval Checklist](#28-approval-checklist)

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

## 6. Localization & Internationalization

> Internationalization (i18n) is painful to retrofit. Decide upfront.

```
[ ] Single language only: ___
[ ] Multiple languages planned:
    - v1.0: [Language(s)]
    - Future: [Language(s)]
[ ] RTL (right-to-left) support needed
[ ] Date/time format localization
[ ] Currency format localization
[ ] N/A for this project
```

---

## 7. UI/UX Planning

### 7.1 Design Philosophy

| Aspect | Choice |
|--------|--------|
| Visual Style | Minimal / Modern / Playful / Corporate / Glassmorphism / Other: ___ |
| Color Scheme | Dark / Light / Auto / User-selectable |
| Typography | System fonts / Custom fonts: ___ |
| Animation Level | None / Subtle / Rich |

### 7.2 Failure Philosophy

> How the system handles and communicates errors.

| Aspect | Choice |
|--------|--------|
| Failure Mode | Fail fast / Fail safe / Fail silent |
| Error Visibility | User-actionable / System-only / Logged only |
| Recovery Strategy | Auto-retry / Manual retry / Graceful degradation |

### 7.3 Key Screens/Views

| Screen | Purpose | Priority |
|--------|---------|----------|
| [Screen 1] | [What user does here] | MVP / Post-MVP |
| [Screen 2] | [What user does here] | MVP / Post-MVP |
| [Screen 3] | [What user does here] | MVP / Post-MVP |

### 7.4 UI Mockups Required

| Mockup | Status | Notes |
|--------|--------|-------|
| [Screen/Component 1] | [ ] Pending  [ ] Generated  [ ] Approved | [Link or notes] |
| [Screen/Component 2] | [ ] Pending  [ ] Generated  [ ] Approved | [Link or notes] |

### 7.5 User Flows

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

### 7.6 Responsive/Adaptive Design

```
[ ] Single fixed size
[ ] Resizable window (min: ___x___, max: ___x___)
[ ] Responsive (adapts to screen size)
[ ] Multiple layouts (desktop/tablet/mobile)
```

---

## 8. Architecture Planning

### 8.1 High-Level Architecture

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

### 8.2 Component Breakdown

| Component | Responsibility | Depends On |
|-----------|----------------|------------|
| [Component 1] | [What it does] | [Dependencies] |
| [Component 2] | [What it does] | [Dependencies] |

### 8.3 Plugin/Extension Architecture

```
[ ] Not applicable (monolithic)
[ ] Plugin-based architecture
    - Plugin contract defined: [ ] Yes [ ] No
    - Plugin discovery method: ___
    - Plugin isolation: [ ] Full [ ] Partial [ ] None
```

### 8.4 Architectural Patterns

```
[ ] MVC / MVP / MVVM
[ ] Clean Architecture
[ ] Microservices
[ ] Monolith
[ ] Event-driven
[ ] CQRS
[ ] Other: ___
```

### 8.5 ADRs (Architectural Decision Records)

| ADR # | Decision | Status |
|-------|----------|--------|
| 001 | [Major decision 1] | Proposed / Accepted / Superseded |
| 002 | [Major decision 2] | Proposed / Accepted / Superseded |

### 8.6 Change & Versioning Strategy

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

## 9. Technology Selection

### 9.1 Technology Comparison

| Option | Pros | Cons | Verdict |
|--------|------|------|---------|
| [Tech 1] | [Advantages] | [Disadvantages] | ✅ Selected / ❌ Rejected |
| [Tech 2] | [Advantages] | [Disadvantages] | ✅ Selected / ❌ Rejected |

### 9.2 Final Stack

| Layer | Technology | Version | Justification |
|-------|------------|---------|---------------|
| Frontend | [Tech] | [Version] | [Why chosen] |
| Backend | [Tech] | [Version] | [Why chosen] |
| Database | [Tech] | [Version] | [Why chosen] |
| Build/Package | [Tech] | [Version] | [Why chosen] |

### 9.3 Dependencies

| Dependency | Purpose | License | Risk |
|------------|---------|---------|------|
| [Library 1] | [What it provides] | MIT / Apache / GPL / Other | Low / Medium / High |
| [Library 2] | [What it provides] | [License] | [Risk level] |

---

## 10. Data & Storage

### 10.1 Data Model Overview

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

### 10.2 Storage Strategy

| Data Type | Storage Location | Format | Persistence |
|-----------|------------------|--------|-------------|
| User preferences | Local file | JSON | Persistent |
| Cache | Memory | In-memory | Session |
| [Other data] | [Location] | [Format] | [Duration] |

### 10.3 Data Privacy

```
[ ] No personal data collected
[ ] Personal data collected (list below):
    - [Data type 1]: [Purpose]
    - [Data type 2]: [Purpose]
[ ] GDPR compliance required
[ ] Data encryption required: [ ] At rest [ ] In transit
```

---

## 11. Integration Points

### 11.1 External APIs

| API | Purpose | Auth Method | Rate Limits |
|-----|---------|-------------|-------------|
| [API 1] | [What it provides] | API Key / OAuth / None | [Limits] |
| [API 2] | [What it provides] | [Auth] | [Limits] |

### 11.2 System Integrations

| System | Integration Type | Notes |
|--------|------------------|-------|
| Windows Registry | Read/Write | For auto-start |
| File System | Read/Write | For config storage |
| [Other] | [Type] | [Notes] |

### 11.3 Third-Party Services

```
[ ] No third-party services
[ ] Services used:
    - [Service 1]: [Purpose]
    - [Service 2]: [Purpose]
```

---

## 12. Security Considerations

### 12.1 Threat Model

| Threat | Likelihood | Impact | Mitigation |
|--------|------------|--------|------------|
| [Threat 1] | Low / Medium / High | Low / Medium / High | [How to prevent] |
| [Threat 2] | [Likelihood] | [Impact] | [Mitigation] |

### 12.2 Security Checklist

```
[ ] Input validation on all external data
[ ] No hardcoded secrets
[ ] Secrets stored securely (env vars, keyring)
[ ] Dependencies audited for vulnerabilities
[ ] Principle of least privilege applied
[ ] Sensitive data encrypted
[ ] Logging excludes sensitive data
[ ] Secure defaults enabled
[ ] Unsafe/destructive actions require explicit confirmation
```

### 12.3 Permissions Required

| Permission | Why Needed | User Consent |
|------------|------------|--------------|
| [Permission 1] | [Reason] | Implicit / Explicit prompt |
| [Permission 2] | [Reason] | [Consent type] |

---

## 13. Legal & Compliance

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

## 14. Deployment & Distribution

### 14.1 Distribution Method

```
[ ] Direct download (website)
[ ] App store (Microsoft Store / Mac App Store / etc.)
[ ] Package manager (npm / brew / winget / etc.)
[ ] Enterprise deployment (MDM / SCCM)
[ ] Source only (build yourself)
```

### 14.2 Installer Requirements

| Requirement | Details |
|-------------|---------|
| Installer format | .exe / .msi / .dmg / .deb / .AppImage / Other: ___ |
| Installer size target | < ___ MB |
| Silent install support | [ ] Yes [ ] No |
| Uninstaller provided | [ ] Yes [ ] No |
| Upgrade path | [ ] In-app update [ ] Manual reinstall [ ] Auto-update |

### 14.3 User Notifications During Install

```
[ ] License agreement
[ ] Installation location choice
[ ] Desktop shortcut option
[ ] Start menu entry option
[ ] Auto-start option (with clear disclosure)
[ ] Privacy policy / data collection notice
```

---

## 15. Operations, Maintenance & Incident Response

> How the system will be operated, maintained, and recovered post-launch.

### 15.1 Logging & Diagnostics

| Aspect | Details |
|--------|---------|
| Log storage location | [Path or service] |
| Log rotation policy | [e.g., "7 days, 100 MB max"] |
| Debug vs release verbosity | [Levels available] |
| Crash report collection | [ ] None [ ] Opt-in [ ] Automatic |

### 15.2 Failure Handling

| Scenario | Expected Behavior |
|----------|-------------------|
| Startup failure | [e.g., "Show actionable error with log path"] |
| Corrupt config | [e.g., "Auto-reset to defaults + warn user"] |
| Missing dependency | [e.g., "Graceful degradation with message"] |
| Network unavailable | [e.g., "Offline mode with sync later"] |

### 15.3 Incident Response

| Aspect | Details |
|--------|---------|
| Severity levels defined | [ ] P0 (critical) [ ] P1 [ ] P2 [ ] P3 |
| Escalation path | [Who handles what severity?] |
| Rollback procedure | [How to revert a bad release?] |
| Post-mortem process | [ ] Required for P0 [ ] Required for P0-P1 [ ] Optional |

### 15.4 Support Model

| Aspect | Details |
|--------|---------|
| User support channel | [Email / Forum / Discord / etc.] |
| SLA expectations | [Response time, resolution time] |
| Issue triage process | [How bugs are prioritized] |
| On-call rotation | [ ] N/A [ ] Defined: ___ |

---

## 16. Monitoring & Observability

> Different from logging—this is about proactive system health visibility.

### 16.1 Health Indicators

| Metric | What It Measures | Alert Threshold |
|--------|------------------|-----------------|
| [Metric 1] | [Description] | [When to alert] |
| [Metric 2] | [Description] | [When to alert] |

### 16.2 Observability Tools

```
[ ] No monitoring (desktop app / offline)
[ ] Error tracking: [Tool, e.g., Sentry]
[ ] Analytics: [Tool, e.g., Mixpanel]
[ ] APM: [Tool, e.g., Datadog]
[ ] Custom dashboard: [Tool]
```

### 16.3 User Consent for Telemetry

```
[ ] No telemetry collected
[ ] Opt-in telemetry
[ ] Opt-out telemetry (default on)
[ ] Anonymous usage stats only
```

---

## 17. Documentation & Knowledge Transfer

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

## 18. Testing Strategy

### 18.1 Test Types

| Test Type | Coverage Target | Tools |
|-----------|-----------------|-------|
| Unit tests | __% of core logic | [Framework] |
| Integration tests | Critical paths | [Framework] |
| E2E tests | Main user flows | [Framework] |
| Manual testing | Edge cases | Checklist |

### 18.2 Test Environments

```
[ ] Local development
[ ] CI/CD pipeline
[ ] Staging environment
[ ] Production monitoring
```

### 18.3 Acceptance Criteria Template

```
Given: [Initial state]
When: [Action taken]
Then: [Expected result]
```

---

## 19. Success Metrics

### 19.1 Launch Criteria

| Metric | Target | Current |
|--------|--------|---------|
| All MVP features complete | 100% | __% |
| Critical bugs | 0 | __ |
| Test coverage | > __% | __% |
| Performance targets met | Yes | [ ] |

### 19.2 Post-Launch Metrics

| Metric | Target | Measurement |
|--------|--------|-------------|
| User adoption | __ users in __ days | Analytics |
| Crash rate | < __% | Error tracking |
| User satisfaction | > __ / 5 | Survey / reviews |
| [Custom metric] | [Target] | [Method] |

---

## 20. Risks & Mitigations

> Known risks with known mitigations.

| Risk | Probability | Impact | Mitigation | Owner |
|------|-------------|--------|------------|-------|
| [Risk 1] | Low / Medium / High | Low / Medium / High | [Plan] | [Who handles] |
| [Risk 2] | [Prob] | [Impact] | [Plan] | [Owner] |
| [Risk 3] | [Prob] | [Impact] | [Plan] | [Owner] |

---

## 21. Known Unknowns

> We know we don't know these things yet. Different from risks—these are **uncertainty**, not **threat**.

| Area | Unknown | Impact if Large | Plan to Resolve |
|------|---------|-----------------|-----------------|
| [Area 1] | [What we don't know] | High / Medium / Low | [How to find out] |
| [Area 2] | [What we don't know] | [Impact] | [Plan] |
| [Area 3] | [What we don't know] | [Impact] | [Plan] |

---

## 22. External Dependencies & Blockers

> Things outside your control that could delay or derail the project.

| Dependency | Owner | Status | Impact if Delayed | Mitigation |
|------------|-------|--------|-------------------|------------|
| [Dependency 1] | [External party] | [ ] Confirmed [ ] Pending [ ] At risk | [What breaks] | [Backup plan] |
| [Dependency 2] | [External party] | [Status] | [Impact] | [Mitigation] |

---

## 23. Decision Log

> Non-architectural decisions that should be recorded for future reference.

| Date | Decision | Alternatives Considered | Reason Rejected | Owner |
|------|----------|-------------------------|-----------------|-------|
| YYYY-MM-DD | [What was decided] | [Alt 1, Alt 2] | [Why not those] | [Name] |
| YYYY-MM-DD | [Decision] | [Alternatives] | [Reason] | [Name] |

---

## 24. Exit Criteria

> Under what conditions do we abandon, pause, or pivot this project?

> [!CAUTION]
> This is uncomfortable to discuss upfront, but prevents sunk cost fallacy later.

### 24.1 Kill Switch Conditions

```
[ ] Timeline exceeds ___ by ___% (e.g., "Timeline exceeds estimate by 200%")
[ ] Core assumption proves false (specify which): ___
[ ] Key dependency becomes unavailable: ___
[ ] Market conditions change: ___
[ ] [Custom condition]: ___
```

### 24.2 Pivot Triggers

```
If [condition], we will pivot to [alternative approach]:
- If [condition 1] → [Pivot option 1]
- If [condition 2] → [Pivot option 2]
```

---

## 25. Communication Plan

> How stakeholders stay informed.

| Audience | Update Frequency | Channel | Owner |
|----------|------------------|---------|-------|
| [Stakeholder group 1] | [Daily / Weekly / Milestone] | [Email / Slack / Meeting] | [Name] |
| [Stakeholder group 2] | [Frequency] | [Channel] | [Name] |

### 25.1 Status Report Template

```
**Project**: [Name]
**Period**: [Date range]
**Status**: 🟢 On Track / 🟡 At Risk / 🔴 Blocked

**Completed**:
- [Item 1]

**In Progress**:
- [Item 2]

**Blockers**:
- [Issue if any]

**Next Steps**:
- [Upcoming work]
```

---

## 26. Timeline & Phases

### 26.1 Phase Breakdown

| Phase | Description | Duration | Deliverables |
|-------|-------------|----------|--------------|
| Phase 1: Planning | Requirements, design | __ days | This document, mockups |
| Phase 2: Foundation | Project setup, core infra | __ days | Scaffold, CI/CD |
| Phase 3: Core Features | MVP implementation | __ days | Working MVP |
| Phase 4: Polish | Testing, bug fixes | __ days | Release candidate |
| Phase 5: Launch | Distribution, docs | __ days | v1.0 release |

### 26.2 Milestones

| Milestone | Target Date | Status |
|-----------|-------------|--------|
| Planning complete | [Date] | [ ] Not started [ ] In progress [ ] Done |
| MVP complete | [Date] | [ ] Not started [ ] In progress [ ] Done |
| Beta release | [Date] | [ ] Not started [ ] In progress [ ] Done |
| v1.0 release | [Date] | [ ] Not started [ ] In progress [ ] Done |

---

## 27. Open Questions

> [!CAUTION]
> These questions must be resolved before implementation:

| # | Question | Proposed Answer | Status |
|---|----------|-----------------|--------|
| 1 | [Question 1] | [Tentative answer] | [ ] Open [ ] Resolved |
| 2 | [Question 2] | [Tentative answer] | [ ] Open [ ] Resolved |
| 3 | [Question 3] | [Tentative answer] | [ ] Open [ ] Resolved |

---

## 28. Approval Checklist

Before moving to implementation, confirm:

### Planning Completeness

- [ ] Problem statement is clear and validated
- [ ] Assumptions and constraints are documented
- [ ] Target users are defined
- [ ] MVP features are prioritized
- [ ] Non-goals are explicit
- [ ] Out-of-scope items are explicit
- [ ] Non-functional requirements have targets
- [ ] Localization strategy decided
- [ ] UI mockups are approved
- [ ] Architecture is documented
- [ ] Change/versioning strategy defined
- [ ] Technology is selected and justified
- [ ] Security considerations addressed
- [ ] Legal/compliance reviewed
- [ ] Deployment method chosen
- [ ] Operations/incident response plan exists
- [ ] Monitoring strategy defined
- [ ] Documentation ownership assigned
- [ ] Known unknowns identified with resolution plans
- [ ] External dependencies confirmed
- [ ] Exit criteria defined
- [ ] Communication plan established

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
│   ✓ Exit criteria before sunk costs  ✓ Communication before conflict        │
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
