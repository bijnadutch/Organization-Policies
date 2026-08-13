# Incident Management Policy
**XXAXX — Policy #8 (Organizational)**

---

## Document Control

| Field | Value |
|---|---|
| Document Title | Incident Management Policy |
| Organization | XXAXX |
| Document Owner | Chief Information Security Officer (CISO) / Head of IT Operations |
| Approved By | Management Body / Board of Directors |
| Classification | Internal |
| Version | 2.0 |
| Effective Date | [DATE] |
| Next Review Date | [DATE + 12 months] |
| Review Cycle | Annual, or upon material change to risk, regulation, or organization |
| Parent Policy | Information Security Policy (Policy #0) |

### Revision History

| Version | Date | Author | Summary of Changes |
|---|---|---|---|
| 1.0 | [DATE] | CISO | Initial version (security incidents only) |

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

This Policy defines how XXAXX detects, logs, classifies, responds to, resolves, and learns from **incidents** of any kind that disrupt or threaten to disrupt its information, systems, or services. This includes both:

- **Security incidents** — events compromising the confidentiality, integrity, or availability of information or systems as a result of malicious activity, policy violation, or control failure; and
- **Operational incidents** — unplanned interruptions or degradations of service arising from causes such as hardware failure, software defects, capacity exhaustion, failed changes, third-party/utility outages, or human error, that are not necessarily the result of a security compromise.

A single incident management framework ensures consistent detection, escalation, and resolution regardless of root cause, while recognizing that security incidents carry additional requirements (evidence preservation, forensics, regulatory notification) addressed in the companion Security Incident Response Procedure.

## 2. Scope

This Policy applies to any event that disrupts, or threatens to disrupt, the normal operation of XXAXX's information systems or services, including but not limited to:

- Malware infections, unauthorized access, data breaches, denial-of-service attacks, and other security compromises;
- Service outages and degraded performance, whatever the cause;
- Hardware failures (servers, storage, network equipment);
- Software defects or failed/rolled-back changes causing service impact;
- Capacity or resource exhaustion (e.g., storage, compute, network saturation);
- Third-party or cloud service provider outages affecting XXAXX services;
- Utility failures (power, cooling, connectivity) affecting XXAXX facilities or data processing;
- Physical security incidents affecting information assets.

It applies to all employees, contractors, and third parties who detect, report, or are involved in responding to such events, across all environments (on-premises, cloud, hybrid).

## 3. Definitions

- **Event**: An observed occurrence in a system, network, or service that may or may not indicate a disruption or security concern.
- **Incident**: An event (or series of events) that has disrupted, or has a significant probability of disrupting, normal service operation, or that has compromised the confidentiality, integrity, or availability of information or systems.
- **Security Incident**: An incident arising from a security compromise, policy violation, or malicious activity. Handled per this Policy's lifecycle and the Security Incident Response Procedure (Policy #8a).
- **Operational Incident**: An incident arising from non-malicious causes such as hardware failure, software defect, capacity issues, or failed change.
- **Major Incident**: Any incident (security or operational) with severe business impact, requiring cross-functional coordination and heightened management visibility, regardless of root cause.
- **Significant Incident**: The NIS2-specific threshold defined in the Security Incident Response Procedure and NIS2 Incident Reporting Procedure, triggering mandatory external regulatory notification.
- **Incident Manager**: The individual responsible for coordinating the end-to-end response to a specific incident, security or operational.
- **Root Cause Analysis (RCA)**: A structured process to identify the underlying cause of an incident, distinct from its symptoms.

## 4. Policy Statement

### 4.1 Unified Incident Management Lifecycle

All incidents, regardless of type, follow a common lifecycle: **detection and logging → triage and classification → escalation and response → resolution → closure → post-incident review**. This lifecycle is supported by a documented incident management process and, for security incidents specifically, the technical playbooks defined in the Security Incident Response Procedure.

### 4.2 Detection and Logging

Incidents may be detected through automated monitoring and alerting, service desk reports, employee or user reports, supplier/cloud provider notifications, scheduled maintenance failures, or external disclosure. Every incident is logged in XXAXX's incident tracking system with a timestamp, description, affected systems/services, and initial classification (security or operational, or both where a security root cause has caused operational impact). All employees, contractors, and third parties are required to report suspected incidents immediately through defined channels, without fear of blame for good-faith reporting.

### 4.3 Classification and Priority

Every incident is classified along two dimensions:

- **Type**: Security, Operational, or Mixed (an operational disruption later found to have a security root cause, or vice versa — e.g., a service outage caused by a ransomware attack).
- **Priority**: Determined by combining **impact** (scope of users/services affected, data sensitivity involved, financial/operational consequence) and **urgency** (rate of escalation, time-criticality), using a standard P1–P4 priority matrix maintained as an operational annex to this Policy:

| Priority | Description | Examples | Target Response Time |
|---|---|---|---|
| P1 — Critical | Complete loss of an essential/important service, or a confirmed major security compromise | Total outage of customer-facing platform; confirmed ransomware; data breach of Restricted data | Immediate (within 15–30 min) |
| P2 — High | Significant degradation or partial outage; high-confidence security incident with limited scope | Major feature unavailable; unauthorized access to a single system contained | Within 1 hour |
| P3 — Medium | Limited impact, workaround available; suspected security event under investigation | Non-critical service slow; suspicious login flagged for review | Within 4 business hours |
| P4 — Low | Minimal impact; informational security finding | Cosmetic defect; low-severity scan finding | Next business day |

Security incidents are additionally classified using the severity criteria in the Security Incident Response Procedure, which determines whether the NIS2 Significant Incident threshold is met.

### 4.4 Incident Response and Escalation

For P1 and P2 incidents, an Incident Manager is assigned to coordinate response, regardless of whether the incident is operational or security in nature. Where an incident is (or is suspected to be) security-related, the CISO or delegate is engaged immediately and the Security Incident Response Procedure governs the technical response (containment, eradication, evidence handling). Where an incident is purely operational, IT Operations leads response in coordination with the relevant System/Service Owner, following the Change Management Policy for any remediating changes and the Backup & Disaster Recovery Policy where restoration from backup is required.

Major Incidents (P1, regardless of type) trigger a defined major incident process: a coordination bridge/channel is established, a single Incident Manager is designated, stakeholders (including the management body for incidents meeting Critical/Significant thresholds) are kept informed at defined intervals, and a public or customer-facing status update is issued where the incident affects service availability to external parties.

### 4.5 Resolution and Recovery

Incidents are resolved when the immediate disruption or compromise is addressed and normal service is restored, verified by the relevant Service/System Owner. For operational incidents, resolution may involve failover, restoration from backup, hardware replacement, or rollback of a change. For security incidents, resolution follows the eradication and recovery steps defined in the Security Incident Response Procedure, including verification that the root cause has been addressed before systems are returned to service.

### 4.6 Root Cause Analysis and Post-Incident Review

Following resolution of any P1 or P2 incident, and any Medium/High/Critical security incident, a post-incident review is conducted to document the timeline, root cause, effectiveness of the response, and lessons learned. For operational incidents this includes formal root cause analysis; for security incidents this follows the process defined in the Security Incident Response Procedure. Resulting action items are tracked to closure and, where they represent residual risk, logged in the risk register.

### 4.7 Communication

Internal communication during an incident follows a defined escalation path proportionate to priority. External communication — to customers, the public, regulators, or law enforcement — is coordinated through Legal and Communications. Communication regarding confirmed or suspected security incidents additionally follows the notification requirements in the Security Incident Response Procedure and NIS2 Incident Reporting Procedure without exception.

### 4.8 Metrics and Reporting

XXAXX tracks incident management metrics for both operational and security incidents, including volume by priority/type, mean time to detect (MTTD), mean time to respond, mean time to resolve (MTTR), and SLA compliance. Metrics are reported to management on a regular basis and reviewed for trends indicating systemic issues.

### 4.9 Testing and Preparedness

The incident management process, including major incident procedures and security-specific playbooks, is tested at least annually through tabletop exercises or simulations covering both operational scenarios (e.g., data center failure, critical vendor outage) and security scenarios (e.g., ransomware, data breach). Findings from tests are used to update the process and playbooks.

### 4.10 Third-Party and Supplier Incidents

Incidents originating from or reported by a supplier — whether operational (e.g., cloud provider outage) or security-related — are handled through this Policy in coordination with the Supplier & Third-Party Security Policy, including assessment of contractual service credits (for operational impact) or regulatory reporting obligations (for security impact).

## 5. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| CISO | Owns the security-incident track of this Policy; is informed of all P1/P2 security incidents; oversees the Security Incident Response Procedure and its testing. |
| Head of IT Operations | Owns the operational-incident track of this Policy; ensures operational incident response capability and escalation processes are maintained. |
| Incident Manager (per incident) | Coordinates end-to-end response for a specific P1/P2 incident, security or operational; drives status communication and post-incident review. |
| Security Incident Response Team | Cross-functional group activated for security incidents, per the Security Incident Response Procedure. |
| IT Operations / Service Desk | First point of contact for detection and logging of operational incidents; executes technical recovery actions. |
| System / Service Owners | Verify resolution and service restoration for incidents affecting their systems; participate in root cause analysis. |
| Management Body | Informed of Major Incidents and Significant Incidents; makes strategic decisions where major business impact or external notification is involved. |
| All Employees, Contractors & Third Parties | Report suspected incidents (security or operational) immediately through defined channels; cooperate with investigation and recovery activities. |
| Legal & Communications | Advise on and manage external communication and regulatory/contractual obligations arising from an incident. |

## 6. Compliance and Enforcement

Failure to report a suspected incident, failure to follow defined escalation procedures for P1/P2 incidents, or interference with incident response or evidence preservation, is treated as a policy breach. Compliance with this Policy is verified through incident metrics, post-incident review records, testing exercise outcomes, and internal audit.

## 7. Exceptions

Deviations from the standard incident management process (e.g., an abbreviated process for a confirmed false positive or trivial, self-resolving event) must be documented and approved by the relevant Incident Manager, IT Operations lead, or CISO as appropriate to incident type.

## 8. Review and Update

This Policy, the priority matrix, and the overall incident management process are reviewed at least annually, following any Major Incident or Significant Incident, and following each testing exercise.

## 9. Related Documents

- Information Security Policy (Policy #0)
- Risk Management Policy (Policy #1)
- Supplier & Third-Party Security Policy (Policy #5)
- Vulnerability Management Policy (Policy #7)
- **Security Incident Response Procedure (Policy #8a)** — detailed security-specific response, containment, forensics, and evidence handling
- NIS2 Incident Reporting Procedure (Policy #9)
- Business Continuity Policy (Policy #10)
- Backup & Disaster Recovery Policy (Policy #11)
- Change Management Policy (Policy #13)
- Logging & Monitoring Policy (Policy #24)
- Incident Priority Matrix and Playbooks (operational annexes)

---

## Appendix A — Regulatory & Standards Mapping

| Topic / Section | NIS2 Directive | ISO/IEC 27001:2022 | ISO/IEC 27002:2022 | NIST CSF v2.0 |
|---|---|---|---|---|
| Unified incident handling measures (security + operational) | Art. 21(2)(b) | Cl. 8.1 | A.5.24 (incident management planning and preparation) | RS.MA-01 |
| Detection & logging of events | Art. 21(2)(b) | Cl. 8.1 | A.5.25, A.6.8 (event reporting) | DE.AE, RS.MA-02 |
| Classification & priority (security and operational) | Art. 21(2)(b); Art. 23(3) | Cl. 8.1 | A.5.25 | RS.MA-02, RS.AN |
| Incident response & major incident coordination | Art. 21(2)(b)/(c) | Cl. 8.1 | A.5.26 | RS.MA-03, RS.CO |
| Resolution, recovery & restoration (operational) | Art. 21(2)(c) | Cl. 8.1 | A.5.29, A.5.30, A.8.13, A.8.14 | RC.RP |
| Root cause analysis & post-incident review | Art. 21(2)(b)/(f) | Cl. 10.1, 9.1 | A.5.27 (learning from info security incidents) | RC.RP, ID.IM |
| Metrics & management reporting | Art. 21(2)(f) | Cl. 9.1, 9.3 | A.5.24, A.5.35 | GV.OV |
| Testing of incident/major-incident process | Art. 21(2)(b)/(c) | Cl. 8.1, 9.1 | A.5.24 | ID.IM-04 |
| Third-party / supplier incident coordination | Art. 21(2)(b)/(d) | Cl. 8.1 | A.5.24, A.5.20 | RS.MA, GV.SC |
| Security-specific handling (cross-ref. Policy #8a) | Art. 21(2)(b) | Cl. 8.1 | A.5.24–A.5.28 | RS.MA, RS.AN |
