# Change Management Policy
**XXAXX — Policy #13 (Organizational)**

---

## Document Control

| Field | Value |
|---|---|
| Document Title | Change Management Policy |
| Organization | XXAXX |
| Document Owner | Head of IT Operations / Chief Information Security Officer (CISO) |
| Approved By | Management Body / Board of Directors |
| Classification | Internal |
| Version | 1.0 |
| Effective Date | [DATE] |
| Next Review Date | [DATE + 12 months] |
| Review Cycle | Annual, or upon material change to risk, regulation, or organization |
| Parent Policy | Information Security Policy (Policy #0) |

### Revision History

| Version | Date | Author | Summary of Changes |
|---|---|---|---|
| 1.0 | [DATE] | CISO | Initial version |

---

## Table of Contents

1. [Purpose](#1-purpose)
2. [Scope](#2-scope)
3. [Definitions](#3-definitions)
4. [Policy Statement](#4-policy-statement)
5. [Roles and Responsibilities](#5-roles-and-responsibilities)
6. [Compliance and Enforcement](#6-compliance-and-enforcement)
7. [Exceptions](#7-exceptions)
8. [Review and Update](#8-review-and-update)
9. [Related Documents](#9-related-documents)
10. [Appendix A — Regulatory & Standards Mapping](#appendix-a--regulatory--standards-mapping)

---

## 1. Purpose

This Policy defines how changes to XXAXX's information systems, infrastructure, applications, and configurations are requested, assessed, approved, tested, implemented, and reviewed. Controlled change management prevents unintended service disruption and security weaknesses being introduced through poorly planned, untested, or unauthorized changes — one of the most common root causes of both operational incidents and security incidents alike.

## 2. Scope

This Policy applies to all changes to production (and, where relevant, pre-production) information systems, infrastructure, network configuration, cloud environments, and applications operated by or on behalf of XXAXX, including changes made by third parties/suppliers with access to XXAXX systems. It covers planned changes, standard/pre-approved changes, and emergency changes. It applies to IT Operations, Development, Information Security, and any third party performing changes on XXAXX's behalf.

## 3. Definitions

- **Change**: Any addition, modification, or removal of anything that could affect XXAXX's information systems or services, including infrastructure, applications, configurations, and network components.
- **Request for Change (RFC)**: A formal request to make a change, documenting its nature, justification, risk, and implementation plan.
- **Standard Change**: A pre-approved, well-understood, low-risk change following a documented, repeatable procedure, not requiring case-by-case approval.
- **Normal Change**: A change requiring assessment and approval prior to implementation, following the standard change management process.
- **Emergency Change**: A change required urgently to resolve or prevent a significant incident or major disruption, following an expedited but still-controlled approval process.
- **Change Advisory Board (CAB)**: The individual or group responsible for reviewing and approving Normal and Emergency changes above a defined risk threshold.
- **Rollback Plan**: A documented plan for reversing a change if it fails or causes unintended impact.

## 4. Policy Statement

### 4.1 Change Categories

All changes are categorized as Standard, Normal, or Emergency. Standard changes follow a pre-approved, documented procedure and do not require individual approval each time, provided they remain within their defined parameters. Normal changes require assessment and approval before implementation, proportionate to risk. Emergency changes follow an expedited process reserved for situations requiring immediate action to resolve or prevent significant harm.

### 4.2 Request for Change

All Normal and Emergency changes are documented via a Request for Change, recording: description and business justification, systems/services affected, risk assessment (including security impact), implementation plan, testing performed or planned, rollback plan, and a proposed implementation window. Changes affecting Confidential/Restricted data or critical systems (per the Asset Management Policy and Business Impact Analysis) receive enhanced scrutiny proportionate to their risk.

### 4.3 Risk and Impact Assessment

Each RFC is assessed for risk and potential impact on confidentiality, integrity, and availability, and for its effect on existing security controls. Changes with a security-relevant risk rating (per the Risk Management Policy methodology) above a defined threshold require review and sign-off from Information Security prior to approval.

### 4.4 Approval

Normal changes are approved by the Change Advisory Board or a designated approver proportionate to risk, prior to implementation. Segregation of duties is maintained wherever practicable — the individual implementing a change is not the sole approver of that change, particularly for changes to production systems handling Confidential/Restricted data or supporting critical processes.

### 4.5 Testing

Changes are tested in a non-production environment prior to deployment wherever feasible, consistent with the environment separation requirements in the Secure Development Policy. Test results are documented and reviewed as part of the approval process for Normal changes with meaningful technical risk.

### 4.6 Scheduling and Communication

Changes are scheduled to minimize business disruption, with affected stakeholders notified in advance proportionate to the change's impact. Changes to systems supporting critical processes are coordinated to avoid periods of heightened business sensitivity where feasible, and are logged in a shared change calendar to identify potential conflicts between concurrent changes.

### 4.7 Implementation and Verification

Approved changes are implemented following the documented plan, by authorized personnel, within the approved window. Following implementation, the change is verified as successful (functionally and, where relevant, from a security control perspective) before being considered complete. Unsuccessful changes are rolled back per the documented rollback plan, and the rollback itself is logged and reviewed.

### 4.8 Emergency Changes

Emergency changes may be implemented ahead of full approval where required to resolve or prevent a significant incident or major disruption, following the process defined in the Incident Management Policy. Emergency changes are documented as fully as circumstances allow at the time, and receive full retrospective review and formal approval (or, if warranted, remediation) within a defined short timeframe (e.g., the next business day) following implementation.

### 4.9 Standard/Pre-Approved Changes

Standard changes (e.g., routine patching within an approved maintenance window, defined configuration adjustments) are documented in a pre-approved change catalog, reviewed periodically to confirm continued suitability, and are still logged for traceability even though they do not require individual case-by-case approval.

### 4.10 Post-Implementation Review

Significant changes, and any change that resulted in an unintended incident or required rollback, are subject to a post-implementation review to confirm the change achieved its intended outcome without adverse effects, and to capture lessons learned. Findings that indicate a process gap are fed into the Risk Management Policy and, where relevant, this Policy's periodic review.

### 4.11 Change Records

All RFCs, approvals, test evidence, and post-implementation review outcomes are retained to support audit and to provide a reliable change history for incident investigation and root cause analysis.

## 5. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| Head of IT Operations | Owns this Policy; oversees the change management process and tooling; chairs or delegates the Change Advisory Board. |
| Change Advisory Board (CAB) | Reviews and approves Normal changes above the defined risk threshold; balances risk, business need, and scheduling conflicts. |
| Change Requesters | Submit complete, accurate RFCs including risk assessment, testing, and rollback plans. |
| Change Implementers | Execute approved changes within the approved window and documented plan; verify success; execute rollback if needed. |
| Information Security Team | Reviews and signs off on changes with meaningful security risk; assesses control impact. |
| System / Application Owners | Approve changes affecting their systems; participate in post-implementation review for significant changes. |
| All Employees | Do not make unauthorized changes to production systems outside this process. |

## 6. Compliance and Enforcement

Implementation of a Normal change without required approval, or an Emergency change without required retrospective review, is a breach of this Policy and is escalated to the Head of IT Operations and CISO. Compliance is monitored through change record audits, unauthorized change detection (via configuration monitoring where deployed), and internal audit.

## 7. Exceptions

Exceptions to standard change requirements (e.g., testing genuinely not feasible for a specific change) must be approved by the CAB or designated approver, documented with rationale and compensating measures.

## 8. Review and Update

This Policy, the change categories, and the standard change catalog are reviewed at least annually and upon significant change to XXAXX's technology environment or change management tooling.

## 9. Related Documents

- Information Security Policy (Policy #0)
- Risk Management Policy (Policy #1)
- Asset Management Policy (Policy #2)
- Secure Development Policy (Policy #6)
- Vulnerability Management Policy (Policy #7)
- Incident Management Policy (Policy #8)
- Business Continuity Policy (Policy #10)
- Backup & Disaster Recovery Policy (Policy #11)
- Standard Change Catalog (supporting document)
- Change Records / RFC Log (operational record)

---

## Appendix A — Regulatory & Standards Mapping

| Topic / Section | NIS2 Directive | ISO/IEC 27001:2022 | ISO/IEC 27002:2022 | NIST CSF v2.0 |
|---|---|---|---|---|
| Change management process | Art. 21(2)(a)/(e) | Cl. 8.1 | A.8.32 (change management) | PR.PS-05 |
| Risk & security impact assessment of changes | Art. 21(2)(a) | Cl. 6.1.2, 8.1 | A.8.32 | ID.RA, PR.PS-05 |
| Segregation of duties in change approval | Art. 21(2)(i) | Cl. 8.1 | A.5.3, A.8.32 | PR.AA-05 |
| Testing prior to deployment (cross-ref.) | Art. 21(2)(e) | Cl. 8.1 | A.8.29, A.8.31, A.8.32 | PR.PS-06 |
| Emergency change handling | Art. 21(2)(a)/(b) | Cl. 8.1 | A.8.32 | PR.PS-05, RS.MA |
| Standard/pre-approved changes | Art. 21(2)(a) | Cl. 8.1 | A.8.32 | PR.PS-05 |
| Post-implementation review | Art. 21(2)(f) | Cl. 9.1, 10.1 | A.8.32 | ID.IM |
| Change records & traceability | Art. 21(2)(f) | Cl. 7.5 | A.8.32, A.8.15 | ID.IM, PR.PS-05 |
