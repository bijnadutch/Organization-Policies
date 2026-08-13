# Secure Development Policy
**XXAXX — Policy #6 (Organizational)**

---

## Document Control

| Field | Value |
|---|---|
| Document Title | Secure Development Policy |
| Organization | XXAXX |
| Document Owner | Chief Information Security Officer (CISO) / Head of Engineering |
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

This Policy defines the security requirements applicable to the design, development, testing, deployment, and maintenance of software and systems built or customized by or for XXAXX. It ensures security is addressed throughout the development lifecycle rather than retrofitted after release, reducing the likelihood and impact of exploitable vulnerabilities in XXAXX's products and internal systems.

## 2. Scope

This Policy applies to all software development activity performed by or on behalf of XXAXX, including:

- In-house application and platform development;
- Development performed by contractors or outsourced development partners;
- Significant customization or configuration of third-party/commercial software and platforms;
- Infrastructure-as-code and automation scripts that provision or configure production environments;
- Development, staging, testing, and production environments used in the software development lifecycle (SDLC).

This Policy applies to all developers, DevOps/platform engineers, QA/testing staff, and engineering managers.

## 3. Definitions

- **SDLC**: Software Development Lifecycle — the structured process covering requirements, design, development, testing, deployment, and maintenance of software.
- **Secure Coding Standard**: A defined set of coding practices intended to prevent common classes of vulnerability.
- **SAST**: Static Application Security Testing — automated analysis of source code to identify vulnerabilities without executing the program.
- **DAST**: Dynamic Application Security Testing — automated testing of a running application to identify vulnerabilities.
- **SCA**: Software Composition Analysis — automated identification of known vulnerabilities in third-party and open-source components.
- **Responsible Disclosure**: A process by which external parties can report discovered vulnerabilities to XXAXX in a controlled, coordinated manner.

## 4. Policy Statement

### 4.1 Security by Design and by Default

Security requirements are identified during the design phase of any new system or significant feature, informed by threat modeling proportionate to the system's risk profile and data classification. Systems are designed to be secure by default (e.g., least-privilege service accounts, encrypted storage/transmission by default, secure default configurations) rather than requiring security to be manually enabled.

### 4.2 Secure Coding Standards

Development teams follow a defined secure coding standard aligned with recognized industry guidance (e.g., OWASP Top 10, OWASP ASVS, or language/platform-specific equivalents), covering areas such as input validation, output encoding, authentication and session management, error handling, and secure use of cryptography. The standard is reviewed periodically to reflect emerging threats and is made readily available to all developers.

### 4.3 Environment Separation

Development, testing/staging, and production environments are logically or physically separated, with access to production environments restricted in accordance with the Access Control Policy. Production data is not used in development or testing environments unless it has been anonymized, pseudonymized, or masked appropriately for the classification of the underlying data, per the Data Classification & Handling Policy.

### 4.4 Version Control and Code Review

All source code is maintained in a version-controlled repository with access restricted to authorized personnel. Changes to code destined for production are subject to peer review prior to merge, with particular attention to security-relevant changes (authentication, authorization, cryptography, data handling). Code review outcomes are recorded.

### 4.5 Automated Security Testing

Automated security testing is integrated into the build/deployment pipeline proportionate to the system's risk, including as applicable: static application security testing (SAST), software composition analysis (SCA) to identify known-vulnerable dependencies, and dynamic application security testing (DAST) for web-facing applications. Findings above an agreed severity threshold block progression to production unless a documented, time-bound risk acceptance is granted.

### 4.6 Third-Party and Open-Source Components

Use of third-party libraries, frameworks, and open-source components is tracked through a software bill of materials (SBOM) or equivalent inventory, scanned for known vulnerabilities via SCA tooling, and kept up to date. Components that are unmaintained, unsupported, or carry unresolved critical vulnerabilities are replaced or remediated in line with the Vulnerability Management Policy.

### 4.7 Secrets Management

Credentials, API keys, cryptographic keys, and other secrets are never hard-coded in source code or committed to version control. Secrets are managed through approved secrets management tooling, consistent with the Cryptography & Key Management Policy.

### 4.8 Security Testing Prior to Release

Significant new systems or major releases undergo security testing (which may include penetration testing, proportionate to risk) prior to production release. Findings are risk-rated and remediated in accordance with the Vulnerability Management Policy prior to release, or accepted through a documented exception where remediation is not immediately feasible.

### 4.9 Change and Deployment Management

Deployment of code to production follows the Change Management Policy, including appropriate approval, rollback planning, and post-deployment verification. Emergency changes follow an expedited but still-controlled and logged process.

### 4.10 Vulnerability Disclosure

XXAXX maintains a mechanism (e.g., a published security contact or responsible disclosure program) through which external researchers or users can report suspected vulnerabilities in XXAXX's software or systems. Reports are triaged and handled in accordance with the Vulnerability Management Policy and, where relevant, the Incident Management Policy.

### 4.11 Developer Security Training

Developers and engineering staff receive role-specific secure development training at onboarding and periodically thereafter, covering the secure coding standard, common vulnerability classes, and use of the organization's security tooling.

## 5. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| Head of Engineering | Ensures secure development practices are embedded in engineering processes and tooling; allocates resource for remediation. |
| CISO / Application Security Function | Owns this Policy and the secure coding standard; oversees security testing tooling and results; advises on threat modeling and exceptions. |
| Development Teams | Follow secure coding standards; conduct/participate in code review; remediate identified vulnerabilities within agreed timelines. |
| DevOps / Platform Engineering | Maintain secure CI/CD pipeline configuration, environment separation, and secrets management infrastructure. |
| QA / Testing | Incorporate security test cases into functional testing where applicable; support coordination of security testing prior to release. |
| Product Owners | Ensure security requirements are considered and prioritized alongside functional requirements. |

## 6. Compliance and Enforcement

Release of code to production without required security testing, or with unresolved Critical/High findings absent a documented exception, is a breach of this Policy. Compliance is monitored through CI/CD pipeline security gate metrics, code review records, and periodic audit of the SDLC process.

## 7. Exceptions

Exceptions to security testing gates or secure coding requirements must be approved by the CISO or Application Security Function, documented with business justification, compensating controls, and a remediation deadline, and logged in the risk register.

## 8. Review and Update

This Policy and the secure coding standard are reviewed at least annually and upon significant change to XXAXX's technology stack, development practices, or the external threat landscape.

## 9. Related Documents

- Information Security Policy (Policy #0)
- Risk Management Policy (Policy #1)
- Data Classification & Handling Policy (Policy #3)
- Access Control Policy (Policy #4)
- Vulnerability Management Policy (Policy #7)
- Incident Management Policy (Policy #8)
- Change Management Policy (Policy #13)
- Cryptography & Key Management Policy (Policy #20)
- Secure Coding Standard (supporting document)

---

## Appendix A — Regulatory & Standards Mapping

| Topic / Section | NIS2 Directive | ISO/IEC 27001:2022 | ISO/IEC 27002:2022 | NIST CSF v2.0 |
|---|---|---|---|---|
| Security in the SDLC / secure development lifecycle | Art. 21(2)(e) | Cl. 8.1 | A.8.25 (secure development lifecycle) | PR.PS-06 |
| Security requirements & threat modeling | Art. 21(2)(e)/(a) | Cl. 8.1, 6.1.2 | A.8.26 (application security requirements), A.5.8 (security in project management) | PR.PS-06, ID.RA |
| Secure coding standards | Art. 21(2)(e) | Cl. 8.1 | A.8.28 (secure coding) | PR.PS-06 |
| Environment separation | Art. 21(2)(e) | Cl. 8.1 | A.8.31 (separation of dev/test/production) | PR.PS-06 |
| Secure architecture & engineering principles | Art. 21(2)(e) | Cl. 8.1 | A.8.27 (secure system architecture and engineering) | PR.PS-06 |
| Security testing (SAST/DAST/pen test) | Art. 21(2)(e) | Cl. 8.1 | A.8.29 (security testing in development and acceptance) | PR.PS-06, ID.RA-01 |
| Outsourced development | Art. 21(2)(e)/(d) | Cl. 8.1 | A.8.30 (outsourced development) | GV.SC-06 |
| Change management for releases (cross-ref.) | Art. 21(2)(e) | Cl. 8.1 | A.8.32 (change management) | PR.PS-05 |
| Vulnerability disclosure & handling (cross-ref.) | Art. 21(2)(e)/(b) | Cl. 8.1 | A.8.8 (mgmt. of technical vulnerabilities) | ID.RA-01, RS.MA |
| Developer security training | Art. 21(2)(g) | Cl. 7.2 | A.6.3 | PR.AT-01 |
