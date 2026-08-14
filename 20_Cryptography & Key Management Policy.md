# Cryptography & Key Management Policy
**XXAXX — Policy #20 (Technological)**

---

## Document Control

| Field | Value |
|---|---|
| Document Title | Cryptography & Key Management Policy |
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

This Policy defines the requirements for the appropriate and effective use of cryptography to protect the confidentiality, integrity, and authenticity of XXAXX's information, and for the secure management of cryptographic keys throughout their lifecycle. Cryptography is only as strong as the key management around it — this Policy ensures both the algorithms XXAXX uses and the way it protects the keys meet a consistent, defensible standard.

## 2. Scope

This Policy applies to all use of cryptography across XXAXX's systems, applications, and services — on-premises and cloud — including encryption of data at rest and in transit, digital signatures, certificate/PKI management, and the generation, storage, distribution, rotation, and destruction of cryptographic keys. It applies to XXAXX-developed systems, procured/commercial systems, and cloud services where XXAXX manages or influences key configuration.

## 3. Definitions

- **Encryption**: The process of converting information into a form unreadable without a corresponding decryption key.
- **Cryptographic Key**: A value used in conjunction with a cryptographic algorithm to encrypt, decrypt, sign, or verify data.
- **Key Management**: The processes for generating, distributing, storing, rotating, revoking, and destroying cryptographic keys.
- **HSM (Hardware Security Module)**: A dedicated hardware device for secure generation, storage, and use of cryptographic keys.
- **KMS (Key Management Service)**: A software or cloud-based service for managing cryptographic keys, which may be backed by an HSM.
- **PKI (Public Key Infrastructure)**: The set of roles, policies, and procedures needed to create, manage, distribute, and revoke digital certificates.
- **Certificate Authority (CA)**: An entity that issues digital certificates, either public/trusted or internal to XXAXX.

## 4. Policy Statement

### 4.1 Approved Cryptographic Standards

XXAXX uses only current, industry-recognized cryptographic algorithms and minimum key lengths, avoiding deprecated or broken algorithms (e.g., MD5, SHA-1 for integrity purposes, DES, RC4). Approved algorithms and minimum parameters (e.g., AES-256 for symmetric encryption, RSA-2048/ECC-256 minimum for asymmetric encryption and signatures, TLS 1.2 minimum — TLS 1.3 preferred — for data in transit, SHA-256 minimum for hashing) are maintained in a supporting Cryptographic Standards document, reviewed periodically to reflect evolving guidance from recognized bodies (e.g., NIST, ENISA) and advances in cryptanalysis, including emerging post-quantum considerations for long-lived sensitive data.

### 4.2 Encryption of Data at Rest

Confidential and Restricted data, per the Data Classification & Handling Policy, is encrypted at rest using approved algorithms, including on servers, endpoints, databases, backups, and removable media. Full-disk encryption is enabled on all laptops and mobile devices as a baseline, consistent with the Asset Management Policy and Remote Working & BYOD Policy.

### 4.3 Encryption of Data in Transit

Confidential and Restricted data transmitted over any network, including the internet and internal networks where warranted by risk, is encrypted in transit using approved protocols (e.g., TLS). Legacy or insecure protocols (e.g., unencrypted FTP, Telnet, SMTP without TLS) are not used for transmitting Confidential/Restricted data.

### 4.4 Key Generation

Cryptographic keys are generated using approved, cryptographically secure methods, with key length and algorithm selection consistent with the Cryptographic Standards document. Where feasible and proportionate to risk, high-value keys (e.g., root/intermediate CA keys, keys protecting Restricted data at scale) are generated and stored within an HSM or equivalent hardware-backed protection.

### 4.5 Key Storage and Access

Cryptographic keys are stored securely, separate from the data they protect wherever architecturally feasible, using an approved KMS or HSM rather than embedded in source code, configuration files, or unencrypted storage. Access to key management systems is restricted per the Access Control Policy's privileged access requirements, with all key management actions logged.

### 4.6 Key Distribution

Where keys must be distributed (e.g., to a new system or a third party), distribution occurs through a secure channel appropriate to the key's sensitivity, with the receiving party's identity and authorization verified before distribution.

### 4.7 Key Rotation

Cryptographic keys are rotated on a defined schedule proportionate to their use and sensitivity, and immediately upon suspected or confirmed compromise, personnel departure with key access, or at the end of a key's defined cryptoperiod. Rotation procedures ensure continuity of access to previously encrypted data where required (e.g., re-encryption or key versioning), coordinated with the Change Management Policy for production-impacting rotations.

### 4.8 Key Revocation and Destruction

Keys are revoked promptly when compromised, when the certificate/key is no longer needed, or when an individual/system's authorization to use the key ends. Keys and their backups are securely destroyed at the end of their lifecycle in a manner appropriate to the sensitivity of the data they protected, with destruction of keys protecting Restricted data logged as evidence.

### 4.9 Certificate and PKI Management

XXAXX maintains an inventory of digital certificates (internal and externally issued) with defined ownership, tracks expiry dates with sufficient lead time to renew before expiration, and uses only certificates issued by a trusted public Certificate Authority for externally facing services, or an appropriately governed internal CA for internal-only use cases. Certificate private keys are protected with the same rigor as other high-value cryptographic keys under this Policy.

### 4.10 Cloud Key Management

For cloud-hosted systems and data, XXAXX uses the cloud provider's native KMS (or an equivalent third-party solution) configured consistent with this Policy, and explicitly determines, per service, whether XXAXX or the provider controls key material (customer-managed vs. provider-managed keys), documenting the choice and its rationale where Restricted data is involved, coordinated with the Cloud Security Policy.

### 4.11 Cryptographic Failures and Incident Handling

Suspected compromise of a cryptographic key, certificate, or the cryptographic implementation protecting Confidential/Restricted data is treated as a security incident and reported per the Incident Management Policy and Security Incident Response Procedure, given the potentially broad exposure a key compromise can create.

## 5. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| CISO | Owns this Policy and the Cryptographic Standards document; approves use of non-standard cryptography; oversees key management architecture. |
| Information Security Team | Maintains KMS/HSM infrastructure; monitors certificate expiry; supports key rotation and incident response for cryptographic compromise. |
| Development Teams | Implement approved cryptographic standards in application code; never hard-code keys, per the Secure Development Policy. |
| IT Operations | Implements encryption at rest/in transit for infrastructure; manages certificate deployment and renewal. |
| System / Application Owners | Ensure systems under their ownership meet this Policy's requirements; flag legacy systems unable to meet current standards for remediation planning. |

## 6. Compliance and Enforcement

Use of deprecated or non-approved cryptographic algorithms, hard-coding of keys/secrets, or failure to rotate/revoke keys as required is a breach of this Policy and is logged as a risk under the Risk Management Policy. Compliance is monitored through configuration scanning (e.g., TLS configuration checks, certificate expiry monitoring), code review/SAST findings related to cryptography, and internal audit.

## 7. Exceptions

Use of non-standard cryptography (e.g., required for interoperability with a legacy system or specific third party) must be approved by the CISO, documented with compensating controls and a remediation timeline where the deviation represents a materially weaker standard.

## 8. Review and Update

This Policy and the Cryptographic Standards document are reviewed at least annually and upon significant developments in cryptographic guidance, cryptanalysis, or regulatory expectations (including post-quantum migration planning).

## 9. Related Documents

- Information Security Policy (Policy #0)
- Risk Management Policy (Policy #1)
- Data Classification & Handling Policy (Policy #3)
- Access Control Policy (Policy #4)
- Secure Development Policy (Policy #6)
- Incident Management Policy (Policy #8)
- Security Incident Response Procedure (Policy #8a)
- Backup & Disaster Recovery Policy (Policy #11)
- Network Security Policy (Policy #21)
- Cloud Security Policy (Policy #26)
- Cryptographic Standards (supporting document)
- Certificate Inventory (operational record)

---

## Appendix A — Regulatory & Standards Mapping

| Topic / Section | NIS2 Directive | ISO/IEC 27001:2022 | ISO/IEC 27002:2022 | NIST CSF v2.0 |
|---|---|---|---|---|
| Policy on the use of cryptographic controls | Art. 21(2)(h) | Cl. 8.1 | A.8.24 (use of cryptography) | PR.DS-01, PR.DS-02 |
| Encryption of data at rest | Art. 21(2)(h) | Cl. 8.1 | A.8.24 | PR.DS-01 |
| Encryption of data in transit | Art. 21(2)(h)/(j) | Cl. 8.1 | A.8.24, A.5.14 (information transfer) | PR.DS-02 |
| Key generation & storage | Art. 21(2)(h) | Cl. 8.1 | A.8.24 | PR.DS-01 |
| Key distribution, rotation, revocation, destruction | Art. 21(2)(h) | Cl. 8.1 | A.8.24 | PR.DS-01 |
| Certificate / PKI management | Art. 21(2)(h)/(j) | Cl. 8.1 | A.8.24 | PR.DS-01, PR.AA-03 |
| Cloud key management (cross-ref.) | Art. 21(2)(h)/(d) | Cl. 8.1 | A.8.24, A.5.23 | PR.DS-01, GV.SC |
| Cryptographic incident handling | Art. 21(2)(b)/(h) | Cl. 8.1 | A.8.24, A.5.24 | RS.MA |
