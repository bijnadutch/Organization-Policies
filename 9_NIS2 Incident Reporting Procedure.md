# NIS2 Incident Reporting Procedure
**XXAXX — Policy #9 (Organizational)**

---

## Document Control

| Field | Value |
|---|---|
| Document Title | NIS2 Incident Reporting Procedure |
| Organization | XXAXX |
| Document Owner | Chief Information Security Officer (CISO) |
| Approved By | Management Body / Board of Directors |
| Classification | Internal |
| Version | 1.0 |
| Effective Date | [DATE] |
| Next Review Date | [DATE + 12 months] |
| Review Cycle | Annual, or upon material change to risk, regulation, or organization |
| Parent Policy | Incident Management Policy (Policy #8); Security Incident Response Procedure (Policy #8a) |

### Revision History

| Version | Date | Author | Summary of Changes |
|---|---|---|---|
| 1.0 | [DATE] | CISO | Initial version |

---

## Table of Contents

1. [Purpose](#1-purpose)
2. [Scope](#2-scope)
3. [Definitions](#3-definitions)
4. [Procedure](#4-procedure)
5. [Roles and Responsibilities](#5-roles-and-responsibilities)
6. [Compliance and Enforcement](#6-compliance-and-enforcement)
7. [Exceptions](#7-exceptions)
8. [Review and Update](#8-review-and-update)
9. [Related Documents](#9-related-documents)
10. [Appendix A — Regulatory & Standards Mapping](#appendix-a--regulatory--standards-mapping)
11. [Appendix B — Notification Content Checklist](#appendix-b--notification-content-checklist)

---

## 1. Purpose

This Procedure defines how XXAXX identifies, escalates, and reports Significant Incidents to the relevant competent authority and/or national CSIRT within the mandatory timelines set out in Article 23 of the NIS2 Directive, and how it communicates with affected service recipients where required. It operationalizes the handoff point defined in the Security Incident Response Procedure (Section 4.8): the regulatory clock starts when XXAXX becomes aware of a Significant Incident and does not pause for ongoing containment or investigation.

## 2. Scope

This Procedure applies to any incident affecting XXAXX's network and information systems that is assessed as meeting, or potentially meeting, the Significant Incident threshold defined below. It applies to the CISO, the Security Incident Response Team, Legal, and Communications, and covers incidents originating internally or via a supplier/third party.

## 3. Definitions

- **Significant Incident**: Per Article 23(3) NIS2, an incident is significant if it (a) has caused or is capable of causing severe operational disruption of the services or financial loss for XXAXX, or (b) has affected or is capable of affecting other natural or legal persons by causing considerable material or non-material damage.
- **Competent Authority**: The national authority designated under NIS2 responsible for supervising XXAXX's compliance (specific authority to be confirmed based on XXAXX's sector and member state).
- **CSIRT**: Computer Security Incident Response Team — the national body to which incident notifications are made, alongside or via the competent authority depending on the member state's chosen notification model.
- **Early Warning**: The initial notification required within 24 hours of becoming aware of a Significant Incident.
- **Incident Notification**: The follow-up notification required within 72 hours of becoming aware of a Significant Incident.
- **Final Report**: The comprehensive report required no later than one month after the Incident Notification (or after the incident is resolved, if resolution takes longer, per the interim/progress reporting requirement).
- **Intermediate Report**: A status update provided upon request of the competent authority/CSIRT, or proactively where the incident remains ongoing at the one-month mark.

## 4. Procedure

### 4.1 Significant Incident Determination

Immediately upon classification of a security incident under the Security Incident Response Procedure, the CISO assesses it against the Article 23(3) criteria, considering in particular: the number of users/customers affected, the duration of the incident, the geographic spread of the incident, the disruption caused to service functionality, and the economic and societal impact. This assessment is documented regardless of outcome, including the rationale where an incident is determined *not* to meet the threshold, since this record may itself be requested by a competent authority.

Where there is reasonable uncertainty whether the threshold is met, XXAXX errs on the side of notification — a precautionary Early Warning can be submitted and later withdrawn or downgraded if the incident proves not to be significant, whereas a missed notification cannot be corrected retroactively without consequence.

### 4.2 24-Hour Early Warning

Within 24 hours of becoming aware of a Significant Incident, the CISO (or delegate) submits an Early Warning to the competent authority and/or national CSIRT, indicating: whether the incident is suspected to be caused by unlawful or malicious action, and whether it is suspected to have a cross-border impact. The clock starts from the point XXAXX becomes aware of the incident, not from the point of confirmation of severity or root cause — awareness of a credible indication is sufficient to start the countdown.

### 4.3 72-Hour Incident Notification

Within 72 hours of becoming aware, XXAXX submits an Incident Notification updating and, where relevant, superseding the Early Warning, including: an initial assessment of the incident (severity and impact), the indicators of compromise identified to date (where applicable and available), and — where an initial assessment can be made — the nature of the threat or root cause. The full content checklist for this notification is provided in Appendix B.

### 4.4 One-Month Final Report

No later than one month after submission of the Incident Notification, XXAXX submits a Final Report including: a detailed description of the incident, its severity and impact, the threat or root cause that likely triggered it, the mitigation measures applied and ongoing, and, where applicable, the cross-border impact. Where the incident is still ongoing at the one-month mark, XXAXX submits an Intermediate progress report at that point and the Final Report is submitted within one month of the incident being resolved.

### 4.5 Notification Channel and Format

Notifications are submitted through the channel designated by XXAXX's competent authority/national CSIRT (e.g., a dedicated reporting portal), using the format and template they prescribe where one exists. Where XXAXX operates across multiple member states or is uncertain which authority is the lead/coordinating authority for a given incident, Legal is engaged to confirm the correct recipient(s) without delaying the 24-hour clock.

### 4.6 Voluntary Notification

XXAXX may voluntarily notify the competent authority/CSIRT of incidents that do not meet the Significant Incident threshold, near misses, and cyber threats that could have led to a significant incident, where doing so is judged to provide useful threat intelligence value or supports the broader ecosystem, consistent with NIS2's voluntary notification provisions.

### 4.7 Notification to Affected Service Recipients

Where a Significant Incident is likely to adversely affect the provision of XXAXX's service to its recipients, XXAXX informs those recipients of the incident without undue delay, including, where relevant, information on measures or remedies the recipients can take in response to the threat or incident. Where the incident involves a wider cyber threat, XXAXX also informs recipients potentially affected by that threat. Content and timing of recipient communication is coordinated between the CISO, Legal, and Communications, and follows the escalation path in the Incident Management Policy.

### 4.8 Coordination with Data Protection Notification

Where a Significant Incident also constitutes a personal data breach under applicable data protection law, the CISO coordinates with the Data Protection Officer/Privacy Lead to ensure both the NIS2 notification and any separate data protection authority notification are submitted within their respective (and independently running) timelines, using consistent facts across both submissions.

### 4.9 Record-Keeping

All notifications submitted (Early Warning, Incident Notification, Intermediate Reports, Final Report), together with the underlying Significant Incident assessment, are retained as part of the incident record for a minimum of [RETENTION PERIOD], to support audit and any follow-up regulatory inquiry.

### 4.10 Post-Notification Follow-Up

The competent authority or CSIRT may provide feedback, request additional information, or issue guidance following a notification. Such requests are logged and responded to within the timeframe specified by the authority, coordinated by the CISO and Legal.

## 5. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| CISO | Determines Significant Incident status; owns the 24h/72h/1-month notification timeline; submits notifications or delegates submission; liaises with the competent authority/CSIRT. |
| Legal | Confirms the correct competent authority/CSIRT, advises on legal risk and disclosure obligations, coordinates data protection notification alignment. |
| Communications | Prepares and coordinates any communication to affected service recipients or the public alongside regulatory notification. |
| Security Incident Response Team | Provides the technical detail (scope, root cause, indicators of compromise, mitigation status) required to populate each notification stage. |
| Management Body | Informed of all Significant Incidents and associated regulatory notifications; briefed prior to any public statement. |
| Data Protection Officer / Privacy Lead | Coordinates parallel data protection breach notification where applicable. |

## 6. Compliance and Enforcement

Missing a mandatory notification deadline, or submitting materially inaccurate information to a competent authority/CSIRT, is treated as a serious compliance failure given the direct regulatory and financial exposure it creates for XXAXX under NIS2 enforcement provisions. Compliance with this Procedure is verified through notification timeliness tracking (per the metrics in the Security Incident Response Procedure) and internal audit review of the Significant Incident assessment log.

## 7. Exceptions

There are no discretionary exceptions to the statutory 24-hour/72-hour/one-month timelines. Where XXAXX genuinely cannot meet a specific sub-element of the required content within the deadline (e.g., root cause not yet confirmed), the notification is still submitted on time with the information available, clearly marked as preliminary, and supplemented as further detail becomes available.

## 8. Review and Update

This Procedure is reviewed at least annually, following any Significant Incident, and upon any change to the designated competent authority, notification channel, or applicable NIS2 implementing legislation in XXAXX's member state(s) of operation.

## 9. Related Documents

- Incident Management Policy (Policy #8)
- Security Incident Response Procedure (Policy #8a)
- Risk Management Policy (Policy #1)
- Supplier & Third-Party Security Policy (Policy #5)
- Business Continuity Policy (Policy #10)
- Significant Incident Assessment Log (operational record)
- Data Protection Breach Notification Procedure (if maintained separately)

---

## Appendix A — Regulatory & Standards Mapping

| Topic / Section | NIS2 Directive | ISO/IEC 27001:2022 | ISO/IEC 27002:2022 | NIST CSF v2.0 |
|---|---|---|---|---|
| Significant Incident determination | Art. 23(3) | Cl. 8.1 | A.5.25 | RS.MA-02 |
| 24-hour Early Warning | Art. 23(4)(a) | Cl. 8.1 | A.6.8 (event reporting) | RS.CO-02 |
| 72-hour Incident Notification | Art. 23(4)(b) | Cl. 8.1 | A.6.8 | RS.CO-02 |
| One-month Final Report | Art. 23(4)(d) | Cl. 8.1 | A.6.8 | RS.CO-02 |
| Intermediate/progress reporting | Art. 23(4)(c) | Cl. 8.1 | A.6.8 | RS.CO-02 |
| Voluntary notification | Art. 23(9) | Cl. 8.1 | A.5.6 (contact with special interest groups) | RS.CO-05 |
| Notification to affected service recipients | Art. 23(1)-(2) | Cl. 8.1 | A.5.26, A.6.8 | RS.CO-02, RS.CO-03 |
| Coordination with data protection notification | Art. 23; (GDPR Art. 33/34, external) | Cl. 8.1 | A.5.34 (privacy and protection of PII) | RS.CO-02 |
| Record-keeping of notifications | Art. 21(2)(f) | Cl. 7.5, 9.1 | A.5.28 | ID.IM |
| Authority feedback / follow-up | Art. 23(5)-(6) | Cl. 8.1 | A.6.8 | RS.CO-02 |

---

## Appendix B — Notification Content Checklist

### Early Warning (within 24 hours)
- [ ] Whether the incident is suspected to be caused by unlawful or malicious action
- [ ] Whether the incident is suspected to have a cross-border impact
- [ ] Basic identification of XXAXX and point of contact

### Incident Notification (within 72 hours)
- [ ] Updated assessment of the incident, including severity and impact
- [ ] Indicators of compromise, where available
- [ ] Initial assessment of the nature and root cause of the incident, where available
- [ ] Confirmation/update of cross-border impact assessment

### Intermediate Report (upon request, or if incident ongoing at 1 month)
- [ ] Relevant status updates on the points above
- [ ] Any change in severity, scope, or impact assessment

### Final Report (within 1 month of Incident Notification, or of resolution)
- [ ] Detailed description of the incident, including its severity and impact
- [ ] The type of threat or root cause likely to have triggered the incident
- [ ] Applied and ongoing mitigation measures
- [ ] Cross-border impact, where applicable
