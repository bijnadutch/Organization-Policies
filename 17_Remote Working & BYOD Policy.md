# Remote Working & BYOD Policy
**XXAXX — Policy #17 (People)**

---

## Document Control

| Field | Value |
|---|---|
| Document Title | Remote Working & BYOD Policy |
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

This Policy defines the security requirements for accessing XXAXX's information systems and data from outside XXAXX's managed office environment, including remote/home working, travel, and the use of personally owned devices (Bring Your Own Device, or BYOD). It ensures that flexibility in where and how people work does not come at the cost of XXAXX's security posture.

## 2. Scope

This Policy applies to all employees, contractors, and temporary staff who access XXAXX systems or data remotely, and to any personally owned device (laptop, smartphone, tablet) authorized to access XXAXX systems or data. It applies regardless of location — home, co-working spaces, client sites, or while traveling.

## 3. Definitions

- **Remote Working**: Accessing XXAXX systems or data from a location other than a XXAXX-managed office.
- **BYOD (Bring Your Own Device)**: Use of a personally owned device to access XXAXX systems or data.
- **MDM (Mobile Device Management)**: Software used by XXAXX to enforce security configuration, monitor compliance, and remotely manage (including wipe) devices accessing XXAXX data.
- **Corporate-Managed Device**: A device owned by XXAXX and fully managed by IT, as distinct from a BYOD device.
- **Containerization**: A technique for logically separating business data/applications from personal data/applications on the same device.

## 4. Policy Statement

### 4.1 General Requirements for Remote Access

All remote access to XXAXX systems requires multi-factor authentication per the Multi-Factor Authentication Policy, is conducted over an encrypted connection (e.g., VPN or equivalent secure access technology, or direct access to cloud services requiring MFA), and is subject to the same access control principles (least privilege, need-to-know) as on-site access, per the Access Control Policy.

### 4.2 Corporate-Managed Devices for Remote Work

Where feasible, remote work is performed on corporate-managed devices, configured with baseline security controls (encryption, endpoint protection, patch management, centralized configuration management) equivalent to office-based devices. Corporate devices used remotely remain subject to the same monitoring, patching, and security requirements as when used on-site.

### 4.3 BYOD Eligibility and Enrollment

Use of personally owned devices to access XXAXX systems or data is permitted only where authorized by IT/Information Security and only for defined use cases (e.g., email and calendar access, approved collaboration tools) unless a broader exception is specifically granted. Devices used for BYOD must be enrolled in XXAXX's MDM or equivalent management solution before being granted access, and must meet minimum security baseline requirements: up-to-date operating system, device passcode/biometric lock, device encryption enabled, and no known jailbreak/root modification.

### 4.4 BYOD Data Separation

Where technically feasible, XXAXX uses containerization or equivalent technology to separate business data and applications from personal data on BYOD devices, allowing XXAXX to manage and, where necessary, remotely wipe business data and applications without affecting the user's personal data. Business data should not be stored outside the managed container on a BYOD device (e.g., screenshots or downloads saved to unmanaged personal storage).

### 4.5 Device Loss or Theft

Loss or theft of any device (corporate-managed or BYOD) used to access XXAXX systems or data must be reported to IT/Information Security immediately, following the incident reporting requirements in the Incident Management Policy. IT initiates remote lock/wipe of business data (and, for corporate-managed devices, the full device where appropriate) without delay upon report.

### 4.6 Physical Security While Working Remotely or Traveling

Users are responsible for the physical security of devices used remotely: not leaving devices unattended in public or easily accessible locations, using privacy screens where working on Confidential/Restricted information in public spaces, securing devices when traveling (including compliance with any additional travel security guidance for high-risk destinations), and locking devices when not in active use, consistent with the Clear Desk & Clear Screen Policy.

### 4.7 Network Security While Remote

Users connecting from home or public networks should use trusted, appropriately secured networks (e.g., WPA2/WPA3-secured home Wi-Fi) and avoid conducting XXAXX business over unsecured public Wi-Fi without VPN protection. IT provides guidance on securing home network equipment (e.g., changing default router credentials) as part of onboarding for remote-eligible roles.

### 4.8 Removal from BYOD Program

Business data and application access is removed from a BYOD device promptly upon: termination of employment (per the HR Security Policy), the individual no longer requiring remote access, loss/theft of the device, detection of a security policy violation, or the individual's withdrawal of consent to MDM enrollment (in which case remote/BYOD access is correspondingly withdrawn).

### 4.9 Legal and Privacy Considerations

BYOD enrollment and any associated monitoring or remote wipe capability is implemented in compliance with applicable employment and data protection law, with the scope of XXAXX's access to a personal device (i.e., limited to the managed business container, not personal data) clearly communicated to users before enrollment, and consent obtained where legally required.

## 5. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| CISO | Owns this Policy; defines BYOD eligibility, minimum device baseline, and approved remote access technologies. |
| IT / Information Security Team | Manages MDM enrollment and enforcement; executes remote lock/wipe; provides secure remote access infrastructure (VPN/equivalent). |
| Line Managers | Confirm remote work / BYOD eligibility for their team members in line with role requirements. |
| HR | Coordinates removal of remote/BYOD access as part of the offboarding process. |
| All Remote / BYOD Users | Comply with device baseline requirements; report lost/stolen devices immediately; maintain physical and network security while working remotely. |

## 6. Compliance and Enforcement

Use of an unenrolled or non-compliant personal device to access XXAXX systems or data, or failure to report a lost/stolen device promptly, is a breach of this Policy and may result in immediate revocation of remote access, in addition to the disciplinary process defined in the HR Security Policy. Compliance is monitored through MDM compliance reporting and periodic review.

## 7. Exceptions

Exceptions (e.g., temporary access from an unmanaged device in an emergency) must be approved by IT/Information Security, time-bound, and subject to enhanced monitoring or restricted access scope for the duration of the exception.

## 8. Review and Update

This Policy is reviewed at least annually and upon significant change to XXAXX's remote working arrangements, device management tooling, or applicable law.

## 9. Related Documents

- Information Security Policy (Policy #0)
- Asset Management Policy (Policy #2)
- Access Control Policy (Policy #4)
- HR Security Policy (Policy #14)
- Acceptable Use Policy (Policy #16)
- Clear Desk & Clear Screen Policy (Policy #19)
- Multi-Factor Authentication Policy (Policy #22)
- Incident Management Policy (Policy #8)
- MDM Configuration Standard (supporting document)

---

## Appendix A — Regulatory & Standards Mapping

| Topic / Section | NIS2 Directive | ISO/IEC 27001:2022 | ISO/IEC 27002:2022 | NIST CSF v2.0 |
|---|---|---|---|---|
| Remote working security requirements | Art. 21(2)(i)/(j) | Cl. 8.1 | A.6.7 (remote working) | PR.AA-05, PR.PS |
| Multi-factor authentication for remote access (cross-ref.) | Art. 21(2)(j) | Cl. 8.1 | A.8.5 (secure authentication) | PR.AA-03 |
| Endpoint device configuration & management | Art. 21(2)(a)/(i) | Cl. 8.1 | A.8.1 (user endpoint devices) | PR.PS-01 |
| BYOD enrollment & data separation | Art. 21(2)(i)/(h) | Cl. 8.1 | A.8.1, A.5.10 | PR.PS-01, PR.DS-01 |
| Device loss / theft handling | Art. 21(2)(b)/(i) | Cl. 8.1 | A.7.9 (security of assets off-premises), A.8.1 | PR.PS-01, RS.MA |
| Physical security while remote/traveling | Art. 21(2)(i) | Cl. 8.1 | A.7.9, A.7.7 (clear desk and clear screen) | PR.PS-01 |
| Network security while remote | Art. 21(2)(j) | Cl. 8.1 | A.8.20 (networks security), A.8.1 | PR.IR-01 |
