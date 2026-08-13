# Backup & Disaster Recovery Policy
**XXAXX — Policy #11 (Organizational)**

---

## Document Control

| Field | Value |
|---|---|
| Document Title | Backup & Disaster Recovery Policy |
| Organization | XXAXX |
| Document Owner | Chief Information Security Officer (CISO) / Head of IT Operations |
| Approved By | Management Body / Board of Directors |
| Classification | Internal |
| Version | 1.0 |
| Effective Date | [DATE] |
| Next Review Date | [DATE + 12 months] |
| Review Cycle | Annual, or upon material change to risk, regulation, or organization |
| Parent Policy | Business Continuity Policy (Policy #10) |

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

This Policy defines the technical requirements for backing up XXAXX's data and systems, and for recovering IT infrastructure and services following a disruptive event. It is the technical implementation layer supporting the Business Continuity Policy: where that Policy defines *what* RTO/RPO a critical process requires, this Policy defines *how* XXAXX's systems and data are backed up and restored to meet it.

## 2. Scope

This Policy applies to all XXAXX systems, applications, and data — on-premises, cloud-hosted, and SaaS — that support business processes identified as critical in the Business Impact Analysis, as well as other systems and data as determined necessary by their Asset Owner and classification. It applies to IT Operations, Information Security, and any third parties (including cloud/backup service providers) involved in backup or disaster recovery activities.

## 3. Definitions

- **Backup**: A copy of data or system state retained for the purpose of restoration following loss, corruption, or disruption.
- **Disaster Recovery (DR)**: The process, policies, and procedures for recovering or continuing IT infrastructure and systems following a disruptive event.
- **Disaster Recovery Plan (DRP)**: The documented, system-specific plan describing how a given system or service is recovered, distinct from the broader Business Continuity Plan it supports.
- **Full Backup**: A complete copy of all in-scope data at a point in time.
- **Incremental/Differential Backup**: A backup capturing only data changed since the last full or previous backup.
- **Immutable Backup**: A backup stored in a manner that prevents modification or deletion for a defined retention period, including by an attacker with administrative access to production systems.
- **3-2-1 Rule**: A backup strategy principle: at least 3 copies of data, on 2 different media/storage types, with at least 1 copy stored off-site (or logically/physically isolated).

## 4. Policy Statement

### 4.1 Backup Requirements

All systems and data supporting critical business processes, and all Confidential/Restricted data per the Data Classification & Handling Policy, are backed up in accordance with a schedule and retention period proportionate to the RPO defined in the Business Impact Analysis. As a baseline, XXAXX follows the 3-2-1 principle for critical data: at least three copies, on at least two different storage types, with at least one copy isolated from the production environment (off-site, offline, or in a separate cloud account/region with restricted access).

### 4.2 Backup Immutability and Ransomware Resilience

At least one backup copy for critical systems and data is maintained as an immutable or otherwise logically isolated copy, inaccessible for modification or deletion using standard production administrative credentials, to ensure backups remain recoverable in the event of a ransomware attack or an attacker with elevated access to production systems.

### 4.3 Backup Access Control and Encryption

Access to backup systems and repositories is restricted in accordance with the Access Control Policy, with privileged access to backup infrastructure subject to the same enhanced controls (MFA, logging) as other privileged access. Backups containing Confidential or Restricted data are encrypted at rest and in transit, consistent with the Cryptography & Key Management Policy.

### 4.4 Backup Monitoring and Verification

Backup jobs are monitored for successful completion, with failures alerted and investigated promptly. Restoration is tested on a regular basis (at minimum quarterly for critical systems, and following significant system changes) to verify that backups are usable and that recovery meets the required RTO/RPO — a backup that has never been test-restored is not considered a reliable recovery capability.

### 4.5 Disaster Recovery Plans

For each critical system or service, a Disaster Recovery Plan documents: recovery procedures and sequencing, required infrastructure/resources, dependencies on other systems or third parties, designated recovery personnel, and validated RTO/RPO. DRPs are kept current, version-controlled, and accessible in a form usable even if primary systems are unavailable.

### 4.6 Recovery Site and Infrastructure

Where a system's RTO requires it, XXAXX maintains recovery infrastructure (e.g., a secondary data center, cloud region failover, or equivalent) sufficiently isolated from the primary environment that a single event is unlikely to affect both. Recovery infrastructure capacity and configuration are reviewed periodically to ensure they remain adequate as production systems evolve.

### 4.7 Cloud and SaaS Backup Responsibility

For each cloud or SaaS service in use, XXAXX explicitly determines and documents backup responsibility under the shared responsibility model applicable to that service — many SaaS providers do not guarantee point-in-time data recovery by default, and where this is the case, XXAXX implements its own supplementary backup mechanism for data it cannot afford to lose, coordinated with the Cloud Security Policy and Supplier & Third-Party Security Policy.

### 4.8 DR Testing

Disaster recovery capability is tested at least annually for critical systems, through tabletop walkthroughs, component-level failover tests, or full DR exercises, proportionate to system criticality. Test results, including actual recovery times achieved against target RTO/RPO, are documented, and gaps are remediated and tracked to closure.

### 4.9 Activation

DR activation follows defined triggers, coordinated with the Business Continuity Policy's Crisis Management Team activation and the Incident Management Policy's major incident process where the disruption is incident-driven. Recovery actions are logged, and systems are verified as functioning correctly (including confirmation that any security root cause, per the Security Incident Response Procedure, has been addressed) before being returned to normal production use.

## 5. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| Head of IT Operations | Owns this Policy; ensures backup infrastructure and DR capability are implemented and maintained to meet defined RTO/RPO. |
| CISO | Ensures backup and DR controls (access, encryption, immutability) meet security requirements; oversees ransomware resilience of backup architecture. |
| IT Operations / Backup Administrators | Configure, monitor, and maintain backup jobs; perform restoration tests; execute DR plans during activation. |
| System / Application Owners | Confirm RPO/RTO requirements for their systems; validate that DR testing meets business needs. |
| Cloud/Backup Service Providers | Deliver backup/DR services per contractual SLAs; notify XXAXX of any service-affecting issues per the Supplier & Third-Party Security Policy. |
| Crisis Management Team | Authorizes DR activation for major disruptions, in coordination with the Business Continuity Policy. |

## 6. Compliance and Enforcement

Failure to back up critical data per this Policy, failure to complete required restoration/DR testing, or storing all backup copies without isolation from production (defeating the 3-2-1 principle) is logged as a risk under the Risk Management Policy and escalated to the CISO/Head of IT Operations. Compliance is monitored through backup job success/failure metrics, restoration/DR test records, and internal audit.

## 7. Exceptions

Exceptions (e.g., a system temporarily excluded from backup scope, or a deferred DR test) must be approved by the CISO or Head of IT Operations, documented with rationale, compensating measures, and a remediation timeline.

## 8. Review and Update

This Policy, backup schedules, and Disaster Recovery Plans are reviewed at least annually, following any DR activation or major test, and upon significant change to XXAXX's technology environment.

## 9. Related Documents

- Information Security Policy (Policy #0)
- Risk Management Policy (Policy #1)
- Data Classification & Handling Policy (Policy #3)
- Access Control Policy (Policy #4)
- Supplier & Third-Party Security Policy (Policy #5)
- Incident Management Policy (Policy #8)
- Security Incident Response Procedure (Policy #8a)
- **Business Continuity Policy (Policy #10)** — parent policy defining RTO/RPO requirements
- Cryptography & Key Management Policy (Policy #20)
- Cloud Security Policy (Policy #26)
- Disaster Recovery Plans (per critical system; supporting documents)

---

## Appendix A — Regulatory & Standards Mapping

| Topic / Section | NIS2 Directive | ISO/IEC 27001:2022 | ISO/IEC 27002:2022 | NIST CSF v2.0 |
|---|---|---|---|---|
| Backup measures | Art. 21(2)(c) | Cl. 8.1 | A.8.13 (information backup) | PR.DS-11 |
| ICT readiness for business continuity / disaster recovery | Art. 21(2)(c) | Cl. 8.1 | A.5.30 (ICT readiness for business continuity) | RC.RP-01 |
| Redundancy of processing facilities | Art. 21(2)(c) | Cl. 8.1 | A.8.14 (redundancy of information processing facilities) | RC.RP-03 |
| Backup access control & encryption | Art. 21(2)(c)/(h) | Cl. 8.1 | A.8.13, A.8.24 | PR.DS-01, PR.DS-11 |
| Backup verification / restoration testing | Art. 21(2)(c)/(f) | Cl. 9.1, 8.1 | A.8.13 | RC.RP-05, ID.IM-04 |
| DR plans & testing | Art. 21(2)(c) | Cl. 8.1, 9.1 | A.5.29, A.5.30 | RC.RP-02, RC.RP-05 |
| Cloud/SaaS backup responsibility (cross-ref.) | Art. 21(2)(c)/(d) | Cl. 8.1 | A.5.23, A.8.13 | GV.SC, RC.RP |
| DR activation & recovery verification | Art. 21(2)(c) | Cl. 8.1 | A.5.29, A.8.13 | RC.RP-04 |
