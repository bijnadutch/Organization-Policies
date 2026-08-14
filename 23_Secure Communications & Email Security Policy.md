# Secure Communications & Email Security Policy
**XXAXX — Policy #23 (Technological)**

---

## Document Control

| Field | Value |
|---|---|
| Document Title | Secure Communications & Email Security Policy |
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

This Policy defines the technical and procedural controls XXAXX applies to secure its email and other business communication channels, and the arrangements XXAXX maintains for secure communication during emergencies when primary channels may be unavailable or compromised. Email in particular remains one of the most common vectors for phishing, business email compromise, and malware delivery, warranting controls beyond general acceptable use expectations.

## 2. Scope

This Policy applies to XXAXX's email systems, business messaging and collaboration platforms (e.g., chat, video conferencing), and file transfer mechanisms, along with the backup/emergency communication channels used during a major incident or disruption. It applies to all employees, contractors, and third parties using XXAXX-provided communication systems.

## 3. Definitions

- **Business Email Compromise (BEC)**: A form of attack in which a threat actor impersonates a trusted party (e.g., an executive or supplier) via email to induce a fraudulent action, typically a payment or data disclosure.
- **SPF (Sender Policy Framework)**: An email authentication standard that specifies which mail servers are authorized to send email on behalf of a domain.
- **DKIM (DomainKeys Identified Mail)**: An email authentication standard using digital signatures to verify that an email was not altered in transit and originated from an authorized sender.
- **DMARC (Domain-based Message Authentication, Reporting & Conformance)**: An email authentication policy that builds on SPF and DKIM, instructing receiving mail servers how to handle messages that fail authentication.
- **Secondary/Emergency Communication Channel**: A pre-arranged alternative communication method used when primary business communication systems are unavailable or untrusted.

## 4. Policy Statement

### 4.1 Email Authentication

XXAXX implements SPF, DKIM, and DMARC for all domains used to send business email, with DMARC configured at an enforcement policy (reject or quarantine, not merely monitor-only) once monitoring confirms legitimate mail flows are correctly authenticated, to reduce the ability of attackers to spoof XXAXX's domains in phishing and BEC attacks.

### 4.2 Email Filtering and Threat Protection

Inbound and outbound email is scanned by automated filtering technology for malware, phishing indicators, and spam, with attachments and links inspected (e.g., sandboxing, link rewriting/time-of-click analysis) proportionate to risk. External email is clearly labeled to help users identify messages originating outside XXAXX.

### 4.3 Business Email Compromise Controls

Given the financial and data-disclosure risk BEC attacks pose, XXAXX applies additional controls to reduce their likelihood and impact: verification of payment or bank detail change requests through a secondary channel (e.g., a phone call to a previously known number, not one provided in the suspicious email) before action, dual authorization for payment changes above a defined threshold, and specific BEC-scenario coverage in the Security Awareness & Training Policy's training content.

### 4.4 Encryption of Email and Sensitive Content

Email transmission between mail servers is encrypted using TLS by default. Confidential or Restricted information sent via email additionally uses end-to-end or message-level encryption (e.g., S/MIME, a secure email gateway solution, or a secure file-sharing link in place of attaching sensitive files directly) consistent with the Data Classification & Handling Policy and Cryptography & Key Management Policy.

### 4.5 Business Messaging and Collaboration Platforms

XXAXX's approved messaging and collaboration platforms (chat, video conferencing, file sharing) are configured with encryption in transit, access restricted to authorized users, and administrative/security settings (e.g., external sharing controls, guest access restrictions) reviewed periodically. Use of unapproved consumer messaging apps for business communication involving Confidential/Restricted information is prohibited, per the Acceptable Use Policy.

### 4.6 Secure File Transfer

Transfer of Confidential or Restricted files, particularly to external parties, uses approved secure file transfer mechanisms (e.g., an encrypted managed file transfer solution or access-controlled, expiring share links) rather than direct email attachment, consistent with the Data Classification & Handling Policy.

### 4.7 Secure Emergency Communications

XXAXX maintains a secondary/emergency communication channel, independent of its primary corporate email and collaboration infrastructure where feasible, for use when primary systems are unavailable or their integrity is in doubt (e.g., during a significant security incident potentially involving email compromise). This channel is identified in the Incident Management Policy's escalation procedures and the Business Continuity Policy's crisis communication protocols, tested periodically as part of incident and business continuity exercises, and its contact details are kept current for key personnel (Incident Response Team, Crisis Management Team, management body).

### 4.8 Voice and Video Communications

Video conferencing and voice communication tools used for sensitive business discussions are configured with access controls (e.g., meeting passwords/waiting rooms) to prevent unauthorized participation, and participants are reminded not to display Confidential/Restricted information on shared screens or physical backgrounds (cross-referenced to the Clear Desk & Clear Screen Policy).

## 5. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| CISO | Owns this Policy; oversees email authentication configuration and BEC control effectiveness; maintains the emergency communication channel plan. |
| IT / Information Security Team | Implements and maintains email filtering, SPF/DKIM/DMARC configuration, and secure file transfer infrastructure. |
| Finance | Applies secondary-channel verification for payment/bank detail change requests. |
| All Employees | Use approved communication channels for business communication; verify unusual requests through a secondary channel; report suspected phishing/BEC attempts. |
| Incident Response Team / Crisis Management Team | Use the designated emergency communication channel when activated. |

## 6. Compliance and Enforcement

Use of unapproved communication channels for Confidential/Restricted information, or failure to verify a payment change request through a secondary channel where required, is a breach of this Policy. Compliance is monitored through email security tooling metrics (e.g., DMARC reports, phishing simulation results), and internal audit.

## 7. Exceptions

Exceptions (e.g., a specific business need for an otherwise unapproved communication tool) must be approved by the CISO, assessed for security risk consistent with the Supplier & Third-Party Security Policy where a new service is involved.

## 8. Review and Update

This Policy is reviewed at least annually and upon significant change to XXAXX's communication infrastructure or the email threat landscape.

## 9. Related Documents

- Information Security Policy (Policy #0)
- Data Classification & Handling Policy (Policy #3)
- Acceptable Use Policy (Policy #16)
- Security Awareness & Training Policy (Policy #15)
- Incident Management Policy (Policy #8)
- Security Incident Response Procedure (Policy #8a)
- Business Continuity Policy (Policy #10)
- Multi-Factor Authentication Policy (Policy #22)
- Cryptography & Key Management Policy (Policy #20)
- Clear Desk & Clear Screen Policy (Policy #19)
- Emergency Communication Contact List (operational document)

---

## Appendix A — Regulatory & Standards Mapping

| Topic / Section | NIS2 Directive | ISO/IEC 27001:2022 | ISO/IEC 27002:2022 | NIST CSF v2.0 |
|---|---|---|---|---|
| Email authentication (SPF/DKIM/DMARC) | Art. 21(2)(j) | Cl. 8.1 | A.8.20 (networks security), A.5.14 (information transfer) | PR.DS-02, PR.IR-01 |
| Email filtering & threat protection | Art. 21(2)(a)/(j) | Cl. 8.1 | A.8.7 (protection against malware) | DE.CM-02 |
| Business email compromise controls | Art. 21(2)(j) | Cl. 8.1 | A.5.14, A.8.23 (web filtering) | PR.AA, PR.DS-02 |
| Encryption of email / sensitive content (cross-ref.) | Art. 21(2)(h)/(j) | Cl. 8.1 | A.8.24, A.5.14 | PR.DS-02 |
| Business messaging / collaboration platform security | Art. 21(2)(j) | Cl. 8.1 | A.5.14, A.8.20 | PR.DS-02, PR.IR-01 |
| Secure file transfer | Art. 21(2)(h)/(j) | Cl. 8.1 | A.5.14 | PR.DS-02 |
| Secure emergency/backup communications | Art. 21(2)(j) | Cl. 8.1 | A.5.29 (information security during disruption) | RS.CO-01, RC.CO |
| Voice / video conferencing security | Art. 21(2)(j) | Cl. 8.1 | A.5.14, A.8.20 | PR.IR-01 |
