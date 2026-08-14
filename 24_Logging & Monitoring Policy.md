# Logging & Monitoring Policy
**XXAXX — Policy #24 (Technological)**

---

## Document Control

| Field | Value |
|---|---|
| Document Title | Logging & Monitoring Policy |
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

This Policy defines what XXAXX logs, how those logs are protected and retained, and how they are monitored to detect security and operational events in a timely manner. Comprehensive, tamper-resistant logging is foundational to both incident detection and post-incident investigation — without it, XXAXX cannot reliably answer "what happened" during a security incident, an audit, or a regulatory inquiry.

## 2. Scope

This Policy applies to all XXAXX systems, applications, network infrastructure, and cloud services that generate security-relevant or operationally relevant log data. It applies to IT Operations, Information Security, Development teams, and third parties operating systems on XXAXX's behalf where log access is contractually available.

## 3. Definitions

- **Log**: A recorded entry documenting an event that occurred within a system, application, or network.
- **SIEM (Security Information and Event Management)**: A platform that aggregates, correlates, and analyzes log data from multiple sources to support security monitoring and detection.
- **Log Retention**: The period for which log data is stored before deletion or archival.
- **Clock Synchronization**: The alignment of system clocks across an environment to a common, accurate time source, essential for correlating events across systems.
- **Alert**: A notification generated when monitored log data matches a condition indicating a potential security or operational issue.

## 4. Policy Statement

### 4.1 What Is Logged

XXAXX logs security-relevant and operationally relevant events across its environment, including, at minimum: authentication events (successful and failed logins, MFA events, password changes), privileged access and administrative actions, access to Confidential/Restricted data, changes to security configurations (firewalls, access control, logging itself), system and application errors, network traffic at key boundaries, and changes made through the Change Management Policy process. Log content is defined per system/service based on its criticality and data sensitivity, avoiding both under-logging (insufficient visibility) and over-logging (unnecessary capture of sensitive data within logs themselves, e.g., full passwords or full payment card numbers, which must never be logged in clear text).

### 4.2 Log Protection

Logs are protected against unauthorized access, modification, and deletion — including by users with administrative access to the systems generating the logs — through measures such as centralized log aggregation to a separate, access-restricted logging platform, write-once/append-only storage where feasible, and role-based access control limiting who can view or manage log data, consistent with the Access Control Policy. Protecting logs from tampering by an attacker with elevated access is treated with the same rigor as backup immutability under the Backup & Disaster Recovery Policy.

### 4.3 Log Retention

Logs are retained for a defined minimum period proportionate to their purpose — supporting incident investigation, audit, and applicable legal/regulatory requirements — with security-relevant logs for critical systems retained for a minimum of [RETENTION PERIOD, e.g., 12 months] and made readily accessible for a shorter operational window (e.g., 90 days) to support timely investigation, with older logs archived. Retention periods are reviewed against applicable legal, regulatory, and contractual requirements, including any specific evidentiary retention needs identified in the Security Incident Response Procedure.

### 4.4 Clock Synchronization

All systems generating logs synchronize their clocks to a common, accurate time source (e.g., NTP), to ensure log timestamps can be reliably correlated across systems during investigation — a control that is simple to implement but that materially undermines investigation and evidentiary value if neglected.

### 4.5 Monitoring and Alerting

Logs from security-relevant sources are monitored, ideally through a centralized SIEM or equivalent capability, with alerting rules configured to flag indicators of compromise, policy violations, and anomalous behavior in a timely manner. Alert thresholds and rules are tuned periodically to balance timely detection against alert fatigue from excessive false positives.

### 4.6 Monitoring Coverage

Monitoring covers, at minimum: authentication and access anomalies (per the Access Control Policy and Multi-Factor Authentication Policy), network traffic anomalies (per the Network Security Policy), endpoint threat detection (per the Malware & Endpoint Protection Policy), and cloud environment activity (per the Cloud Security Policy), providing visibility across on-premises and cloud environments consistently rather than treating cloud logging as an afterthought.

### 4.7 Alert Triage and Escalation

Alerts are triaged by the Information Security Team within a defined target timeframe proportionate to their severity, with confirmed security-relevant alerts escalated into the Incident Management Policy and Security Incident Response Procedure. Alert triage outcomes (true positive, false positive, benign) are recorded to support ongoing tuning of detection rules.

### 4.8 Log Review

In addition to automated alerting, periodic manual or semi-automated review of logs (e.g., privileged access activity, access to Restricted data) is performed to identify patterns that automated rules may not catch, at a frequency proportionate to risk.

### 4.9 Third-Party and Cloud Service Logging

For cloud and SaaS services, XXAXX enables and retains available audit/activity logs (e.g., cloud provider control-plane logs, SaaS administrative activity logs) to the extent offered by the provider, and factors logging/audit capability into supplier security assessments under the Supplier & Third-Party Security Policy, since limited logging capability in a critical third-party service represents a meaningful visibility gap.

### 4.10 Privacy Considerations

Logging and monitoring activity is conducted proportionately and in compliance with applicable data protection law, with any employee monitoring implications addressed consistent with the notice/consultation requirements referenced in the Acceptable Use Policy.

## 5. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| CISO | Owns this Policy; defines logging/monitoring scope and retention requirements; oversees SIEM/monitoring capability effectiveness. |
| Information Security Team (SOC function) | Monitors alerts, triages and escalates security-relevant events, tunes detection rules, performs periodic log review. |
| IT Operations | Ensures systems are configured to generate and forward required logs; maintains clock synchronization. |
| System / Application Owners | Ensure applications under their ownership log required events without capturing prohibited sensitive data in clear text. |
| Development Teams | Implement appropriate application-level logging per secure development standards. |

## 6. Compliance and Enforcement

Disabling or tampering with logging on any system, or failure to configure required logging for a new system prior to production deployment, is treated as a policy breach and is escalated to the CISO. Compliance is monitored through log coverage audits, log integrity verification, and internal audit.

## 7. Exceptions

Exceptions (e.g., a legacy system with limited logging capability) must be approved by the CISO, documented with compensating monitoring measures and a remediation timeline where feasible.

## 8. Review and Update

This Policy, logging scope, and retention periods are reviewed at least annually and upon significant change to XXAXX's technology environment or applicable legal/regulatory requirements.

## 9. Related Documents

- Information Security Policy (Policy #0)
- Access Control Policy (Policy #4)
- Incident Management Policy (Policy #8)
- Security Incident Response Procedure (Policy #8a)
- Backup & Disaster Recovery Policy (Policy #11)
- Change Management Policy (Policy #13)
- Acceptable Use Policy (Policy #16)
- Network Security Policy (Policy #21)
- Multi-Factor Authentication Policy (Policy #22)
- Malware & Endpoint Protection Policy (Policy #25)
- Cloud Security Policy (Policy #26)
- Logging Standard / Log Source Inventory (supporting document)

---

## Appendix A — Regulatory & Standards Mapping

| Topic / Section | NIS2 Directive | ISO/IEC 27001:2022 | ISO/IEC 27002:2022 | NIST CSF v2.0 |
|---|---|---|---|---|
| Logging of security-relevant events | Art. 21(2)(b) | Cl. 8.1 | A.8.15 (logging) | DE.AE-02, DE.CM |
| Log protection against tampering | Art. 21(2)(a)/(b) | Cl. 8.1 | A.8.15 | PR.DS-01, PR.PS |
| Clock synchronization | Art. 21(2)(b) | Cl. 8.1 | A.8.17 (clock synchronization) | DE.AE-03 |
| Monitoring activities / SIEM | Art. 21(2)(b) | Cl. 8.1 | A.8.16 (monitoring activities) | DE.CM-01 |
| Alert triage & escalation (cross-ref.) | Art. 21(2)(b) | Cl. 8.1 | A.8.16, A.5.25 | DE.AE, RS.MA-02 |
| Log retention | Art. 21(2)(f) | Cl. 7.5 | A.8.15 | ID.IM |
| Cloud / third-party logging (cross-ref.) | Art. 21(2)(d)/(b) | Cl. 8.1 | A.5.23, A.8.15 | GV.SC, DE.CM |
| Privileged/administrator activity logging | Art. 21(2)(b)/(i) | Cl. 8.1 | A.8.15, A.8.2 | PR.AA-05, DE.CM |
