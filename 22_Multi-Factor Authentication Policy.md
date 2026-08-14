# Multi-Factor Authentication Policy
**XXAXX — Policy #22 (Technological)**

---

## Document Control

| Field | Value |
|---|---|
| Document Title | Multi-Factor Authentication Policy |
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

This Policy defines where and how XXAXX requires multi-factor authentication (MFA) to reduce the risk that a compromised password alone is sufficient to gain unauthorized access to its systems, applications, and data. Credential theft and reuse remain among the most common initial access vectors in security incidents, and MFA is one of the highest-value controls available to counter it.

## 2. Scope

This Policy applies to authentication to all XXAXX systems, applications, and services — on-premises and cloud/SaaS — by employees, contractors, third parties, and, where applicable, customers accessing XXAXX-provided services. It covers the selection, deployment, and management of MFA methods.

## 3. Definitions

- **Multi-Factor Authentication (MFA)**: Authentication using two or more independent factors from different categories: something you know (password/PIN), something you have (hardware token, mobile device/authenticator app), or something you are (biometric).
- **Authentication Factor**: A single category of credential used to verify identity.
- **Phishing-Resistant MFA**: MFA methods (e.g., FIDO2/WebAuthn security keys, platform authenticators) that are not susceptible to credential relay or real-time phishing (as opposed to SMS or basic push notifications, which can be more easily intercepted or subject to MFA fatigue attacks).
- **MFA Fatigue Attack**: A social engineering technique in which an attacker repeatedly triggers push-based MFA prompts hoping the user will approve one out of frustration or confusion.
- **Single Sign-On (SSO)**: A mechanism allowing a user to authenticate once and gain access to multiple systems without re-authenticating separately.

## 4. Policy Statement

### 4.1 Mandatory MFA Coverage

MFA is required, without exception, for:

- All remote access to XXAXX's network or systems (VPN, zero-trust network access);
- All access to cloud/SaaS administrative consoles and management interfaces;
- All privileged/administrative access to any system, regardless of access location;
- All access to systems or applications processing Confidential or Restricted data;
- All access to email and core collaboration/productivity platforms;
- Single Sign-On (SSO) login, since SSO concentrates access to multiple downstream systems behind a single authentication event.

### 4.2 MFA Method Selection

XXAXX prioritizes phishing-resistant MFA methods (e.g., FIDO2/WebAuthn security keys, platform authenticators/passkeys) for privileged access and access to the most sensitive systems. Authenticator app-based time-based one-time passwords (TOTP) or push notifications with number matching are acceptable for standard user access where phishing-resistant methods are not yet feasible. SMS-based MFA is avoided as a primary method where a stronger alternative is available, given its susceptibility to SIM-swapping and interception, and is permitted only as a fallback/last-resort method.

### 4.3 Protection Against MFA Fatigue and Push-Bombing

Where push-based MFA is used, number matching (requiring the user to enter a displayed number rather than simply approving a prompt) is enabled to reduce susceptibility to MFA fatigue attacks. Users are trained, per the Security Awareness & Training Policy, to reject and report unexpected MFA prompts rather than approving them to make them stop.

### 4.4 MFA Enrollment

Users are enrolled in MFA at account creation, before being granted access to any system requiring it under Section 4.1. Enrollment includes registration of a primary method and, where feasible, a backup method to avoid lockout, both subject to identity verification at enrollment time.

### 4.5 MFA Bypass and Break-Glass Access

Break-glass accounts or emergency access mechanisms that bypass standard MFA are limited to genuine emergencies where standard MFA is unavailable, are subject to the exception process defined in the Access Control Policy, use alternative strong authentication and compensating controls (e.g., physical safe-stored credentials, enhanced logging, immediate post-use review), and are never used as a routine convenience measure.

### 4.6 Lost or Compromised MFA Factors

Loss of an MFA device/factor, or suspected compromise of MFA credentials, is reported to IT/Information Security immediately, consistent with the Incident Management Policy. Re-enrollment following a lost factor requires identity re-verification through an out-of-band process to prevent social-engineering-based account takeover via the MFA reset process itself.

### 4.7 Customer-Facing MFA

Where XXAXX provides authentication to customers/service recipients for its own services, XXAXX offers MFA as a security option and, for services processing sensitive customer data, evaluates making MFA mandatory or default-on, balanced against usability considerations, consistent with the Secure Development Policy's security requirements process.

### 4.8 Monitoring and Anomaly Detection

Authentication events, including MFA successes, failures, and anomalies (e.g., impossible travel, repeated failed MFA attempts), are logged and monitored per the Logging & Monitoring Policy, with alerting configured for patterns indicative of credential compromise or MFA fatigue attack attempts.

## 5. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| CISO | Owns this Policy; defines approved MFA methods and mandatory coverage scope; approves break-glass exceptions. |
| Information Security / IT Team | Implements and maintains MFA infrastructure; manages enrollment and re-enrollment processes; monitors authentication anomalies. |
| System / Application Owners | Ensure systems under their ownership enforce MFA per this Policy's mandatory scope. |
| Line Managers | Support timely MFA enrollment for new team members. |
| All Users | Enroll in and use MFA as required; protect MFA devices/factors; report lost or compromised factors and unexpected MFA prompts immediately. |

## 6. Compliance and Enforcement

Access to in-scope systems without MFA enrollment, sharing of MFA devices or approval of MFA prompts on another user's behalf, or unauthorized use of break-glass access is a breach of this Policy. Compliance is monitored through MFA enrollment coverage reporting, authentication log review, and internal audit.

## 7. Exceptions

Exceptions to mandatory MFA (e.g., a legacy system genuinely unable to support MFA) must be approved by the CISO, documented with compensating controls (e.g., network isolation, enhanced monitoring) and a remediation/replacement timeline, and logged in the risk register.

## 8. Review and Update

This Policy and the list of approved MFA methods are reviewed at least annually and upon significant developments in authentication technology or attack techniques targeting MFA.

## 9. Related Documents

- Information Security Policy (Policy #0)
- Risk Management Policy (Policy #1)
- Access Control Policy (Policy #4)
- Incident Management Policy (Policy #8)
- Security Incident Response Procedure (Policy #8a)
- Security Awareness & Training Policy (Policy #15)
- Remote Working & BYOD Policy (Policy #17)
- Secure Communications & Email Security Policy (Policy #23)
- Logging & Monitoring Policy (Policy #24)

---

## Appendix A — Regulatory & Standards Mapping

| Topic / Section | NIS2 Directive | ISO/IEC 27001:2022 | ISO/IEC 27002:2022 | NIST CSF v2.0 |
|---|---|---|---|---|
| Use of multi-factor authentication | Art. 21(2)(j) | Cl. 8.1 | A.8.5 (secure authentication) | PR.AA-03 |
| MFA for privileged/remote access (cross-ref.) | Art. 21(2)(i)/(j) | Cl. 8.1 | A.8.2 (privileged access rights), A.6.7 (remote working) | PR.AA-03, PR.AA-05 |
| Phishing-resistant authentication methods | Art. 21(2)(j) | Cl. 8.1 | A.8.5 | PR.AA-03 |
| MFA enrollment & identity verification | Art. 21(2)(i)/(j) | Cl. 8.1 | A.5.16 (identity management), A.8.5 | PR.AA-01, PR.AA-02 |
| Break-glass / emergency access | Art. 21(2)(i) | Cl. 8.1 | A.8.2, A.8.5 | PR.AA-05 |
| Authentication monitoring & anomaly detection | Art. 21(2)(b)/(j) | Cl. 8.1 | A.8.16 (monitoring activities) | DE.CM-03 |
