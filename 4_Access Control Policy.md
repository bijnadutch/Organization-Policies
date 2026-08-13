# Access Control Policy
**XXAXX — Policy #4 (Organizational)**

---

## Document Control

| Field | Value |
|---|---|
| Document Title | Access Control Policy |
| Organization | XXAXX |
| Document Owner | Chief Information Security Officer (CISO) |
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

This Policy defines how XXAXX grants, manages, reviews, and revokes access to its information systems, applications, and data. It ensures that access is granted only to authorized individuals, only to the extent necessary for their role, and is removed promptly when no longer required — limiting the impact of compromised credentials and reducing the attack surface across XXAXX's environment.

## 2. Scope

This Policy applies to all access to XXAXX's information systems, applications, networks, and data, whether on-premises or cloud-hosted, by employees, contractors, third parties, and automated system/service accounts. It covers the full access lifecycle: provisioning, authentication, authorization, review, and de-provisioning.

## 3. Definitions

- **Access Control**: The means by which access to systems, applications, and data is restricted to authorized users and processes.
- **Least Privilege**: The principle that users and processes are granted only the minimum access necessary to perform their function.
- **Need-to-Know**: The principle that access to information is granted only where there is a genuine business requirement.
- **Privileged Access**: Access rights that exceed those of a standard user, including administrative, root, or superuser access to systems, networks, or applications.
- **Segregation of Duties**: Dividing critical tasks among multiple individuals to reduce the risk of error or fraud by any single person.
- **Service Account**: A non-human account used by an application, script, or system process to authenticate and access resources.

## 4. Policy Statement

### 4.1 Access Control Principles

Access to XXAXX systems and data is governed by the principles of least privilege and need-to-know. Access rights are role-based wherever practicable, granted through defined access profiles rather than ad hoc individual assignment, and aligned to the data classification of the resource being accessed.

### 4.2 Account Provisioning

Access is granted only following a formal request and approval process. Requests are approved by the relevant Data Owner or System/Application Owner, and provisioning is carried out by IT/Information Security following verification of the requester's identity and authorization. New accounts are created with the minimum access required for the individual's role at onboarding, coordinated with the HR Security Policy.

### 4.3 Authentication

All accounts require unique identification; shared or generic accounts are prohibited except where technically unavoidable, in which case compensating controls (e.g., checkout-based credential vaulting, enhanced logging) are applied. Password requirements, multi-factor authentication requirements, and secure authentication mechanisms are defined in the Multi-Factor Authentication Policy, which applies to all remote access, privileged access, and access to Confidential/Restricted systems as a minimum.

### 4.4 Authorization and Role-Based Access

Access rights are defined through role-based access profiles mapped to job functions. Requests for access beyond a standard role profile require additional, specific approval from the relevant Owner. Segregation of duties is applied to critical functions (e.g., financial transactions, code deployment to production, security control administration) to prevent a single individual from being able to execute and approve/conceal a sensitive action unsupervised.

### 4.5 Privileged Access Management

Privileged access is granted only to individuals whose role requires it, is subject to additional approval, and is used only for tasks that require that level of access — standard business activities (e.g., email, browsing) are performed using non-privileged accounts. Privileged accounts are subject to enhanced controls, including mandatory multi-factor authentication, session logging/monitoring, and more frequent access review. Where feasible, privileged access is granted on a just-in-time or time-bound basis rather than standing.

### 4.6 Access Reviews

Access rights are reviewed on a regular basis (at minimum every six months for standard access, and quarterly for privileged access) by the relevant Owner to confirm continued business need. Access no longer required is revoked promptly following the review. Reviews are documented and evidence retained to support audit.

### 4.7 De-provisioning

Access is revoked promptly upon termination of employment or contract, role change, or extended leave, coordinated with the HR Security Policy and Asset Management Policy. Where immediate revocation is not technically possible, access is suspended within a defined maximum timeframe and revoked as soon as practicable. For role changes, access associated with the previous role is removed, not merely supplemented with new access ("access accumulation" is explicitly prevented).

### 4.8 Service and System Accounts

Service accounts are inventoried, assigned an owner, and granted the minimum privilege necessary for their function. Credentials for service accounts are managed through approved secrets management tooling, rotated periodically or upon suspected compromise, and are not shared across multiple services where avoidable.

### 4.9 Remote and Third-Party Access

Remote access to XXAXX systems is subject to the same access control principles as on-site access, with additional requirements defined in the Remote Working & BYOD Policy. Access granted to third parties (contractors, vendors, support personnel) is time-bound, logged, limited to the specific systems required, and reviewed under the Supplier & Third-Party Security Policy.

### 4.10 Access Logging

Access to systems handling Confidential or Restricted data, and all privileged access, is logged. Logs are managed in accordance with the Logging & Monitoring Policy and are available to support incident investigation and access review.

## 5. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| CISO | Owns this Policy; oversees access governance; approves exceptions for high-risk access scenarios. |
| System / Application / Data Owners | Approve access requests to their systems and data; conduct periodic access reviews; approve de-provisioning exceptions. |
| IT / Information Security Team | Provision and de-provision access; maintain identity and access management (IAM) tooling; manage privileged access solutions. |
| Line Managers | Initiate and confirm access requests for their staff; notify HR/IT promptly of role changes and departures. |
| HR | Notifies IT of joiners, movers, and leavers in a timely manner to trigger access provisioning/de-provisioning. |
| All Users | Use access rights only as authorized; protect authentication credentials; report suspected unauthorized access. |

## 6. Compliance and Enforcement

Sharing of credentials, use of access beyond authorized scope, or failure to report suspected credential compromise is treated as a policy breach and may result in disciplinary action. Compliance is verified through periodic access reviews, audit of provisioning/de-provisioning records, and monitoring of privileged account activity.

## 7. Exceptions

Exceptions to standard access control requirements (e.g., emergency "break-glass" access) must be pre-approved where possible or, in genuine emergencies, approved retrospectively within 24 hours by the CISO, logged, and subject to enhanced post-use review.

## 8. Review and Update

This Policy is reviewed at least annually and upon significant change to XXAXX's IT environment, organizational structure, or applicable regulatory requirements.

## 9. Related Documents

- Information Security Policy (Policy #0)
- Risk Management Policy (Policy #1)
- Asset Management Policy (Policy #2)
- Data Classification & Handling Policy (Policy #3)
- Supplier & Third-Party Security Policy (Policy #5)
- HR Security Policy (Policy #14)
- Remote Working & BYOD Policy (Policy #17)
- Multi-Factor Authentication Policy (Policy #22)
- Logging & Monitoring Policy (Policy #24)

---

## Appendix A — Regulatory & Standards Mapping

| Topic / Section | NIS2 Directive | ISO/IEC 27001:2022 | ISO/IEC 27002:2022 | NIST CSF v2.0 |
|---|---|---|---|---|
| Access control principles (least privilege, need-to-know) | Art. 21(2)(i) | Cl. 8.1 | A.5.15 (access control) | PR.AA-01 |
| Account provisioning / identity lifecycle | Art. 21(2)(i) | Cl. 8.1 | A.5.16 (identity management), A.5.18 (access rights) | PR.AA-01, PR.AA-05 |
| Authentication (cross-ref. MFA) | Art. 21(2)(j) | Cl. 8.1 | A.5.17 (authentication information), A.8.5 (secure authentication) | PR.AA-02, PR.AA-03 |
| Role-based access & segregation of duties | Art. 21(2)(i) | Cl. 8.1 | A.5.18, A.5.3 (segregation of duties) | PR.AA-05 |
| Privileged access management | Art. 21(2)(i)/(j) | Cl. 8.1 | A.8.2 (privileged access rights) | PR.AA-05 |
| Access reviews | Art. 21(2)(f)/(i) | Cl. 9.1, 8.1 | A.5.18 | PR.AA-05, ID.IM |
| De-provisioning / termination | Art. 21(2)(i) | Cl. 8.1 | A.6.5 (responsibilities after termination), A.5.18 | PR.AA-05 |
| Service / system accounts | Art. 21(2)(i) | Cl. 8.1 | A.5.17, A.8.2 | PR.AA-01 |
| Remote & third-party access | Art. 21(2)(i)/(j) | Cl. 8.1 | A.5.15, A.6.7, A.5.19 | PR.AA-05, GV.SC |
| Access logging | Art. 21(2)(b)/(j) | Cl. 8.1 | A.8.15 (logging) | PR.PS-04, DE.CM |
